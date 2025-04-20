# Next js

## random note

### Routing

#### Routing pages info

1.  **[id]** for dynamic routing
2.  **[...slug]** Catch all Segments for all dynamic routing
3.  **\_folderName** for private folder
4.  **(groupName)** for Route Groups **without** change the route
5.  **Link**: to move between routes
6.  **params/searchParams**: to get the data form the url there are two cases:

    1. Server Component

       ```tsx
       "use server";
       export default async function Home({
         params,
         searchParams,
       }: {
         params: Promise<{ id: string }>;
         searchParams: Promise<{ lang: "en" | "ar" | "fr" }>;
       }) {
         const id = (await params).id;
         const lang = (await searchParams).lang;
         return (
           <h1>
             hi from home {id},lang = {lang}
           </h1>
         );
       }
       ```

    2. client Component

    **Note:** can use useRouter() to do the client Component as will.

    **Note:** layout.tsx only have access to params (there is no searchParams)

    ```tsx
    "use client";

    import { useParams, useSearchParams } from "next/navigation";
    export default function Home() {
      const { id } = useParams();
      const lang = useSearchParams();
      return (
        <h1>
          hi from home {id}, lang = {lang}
        </h1>
      );
    }
    ```

    ```tsx
    "use client";

    import { use } from "react";
    export default function Home({
      params,
      searchParams,
    }: {
      params: Promise<{ id: string }>;
      searchParams: Promise<{ lang: "en" | "ar" | "fr" }>;
    }) {
      const { id } = use(params);
      const { lang } = use(searchParams);
      return (
        <h1>
          hi from home {id},lang = {lang}
        </h1>
      );
    }
    ```

#### Metadata

1.  Static Metadata in page.tsx

```tsx
export const metadata = {
  title: "page title",
  description: "page description",
};
```

2.  Metadata in Layouts

```tsx
export const metadata = {
  title: {
    default: "My App",
    template: "%s | My App",
    absolute: "no template",
  },
  description: "The best online shopping experience.",
};
```

3.  Dynamic Metadata using **generateMetadata**

#### page types

- **page.tsx**: page for create the main page that rerender for the route
- **layout.tsx**: page for creating a layout for the pages in his scoop
- **not-found.tsx**: page for create a custom not found page
- **template.tsx** the same as the layout but it re-render each time(use to reset the state (useState)).
- **loading.tsx** : for loading state
- **error.tsx**: for error handling

### Rendering Strategies

[next js learn page](https://nextjs.org/learn/pages-router/data-fetching-two-forms)

1.  ○ (Static) prerendered as static content
1.  ● (SSG) prerendered as static HTML (uses getStaticProps)
1.  ƒ (Dynamic) server-rendered on demand
1.  server side render at run time

#### Server Components & Rendering Strategies

SSR (Server-Side Rendering):

Server Components: Rendered on the server on every request, fetching fresh data for dynamic content (e.g., user-specific pages).

Use Case: Ideal for highly dynamic content requiring real-time data (e.g., dashboards).

Trade-off: Higher server load and latency but ensures up-to-date content.

SSG (Static Site Generation): (`generateStaticParams`)

Server Components: Rendered at build time, generating static HTML. Data is pre-fetched once (e.g., blog posts).

Use Case: Content that rarely changes (e.g., documentation, marketing sites).

Trade-off: Blazing-fast performance but requires rebuilds for updates.

ISR (Incremental Static Regeneration):

Server Components: Rendered at build time and revalidated on-demand or at intervals. Combines SSG’s speed with dynamic updates (e.g., product pages).

Use Case: Semi-dynamic content needing periodic updates without full rebuilds.

Trade-off: Balances freshness and performance via revalidation (e.g., revalidate: 60 seconds).

##### Notes:

1. **generateStaticParams**: Data fetching functions like `getServerSideProps` and `getStaticProps` have been replaced with a new API inside `app`. `getStaticPaths` has been replaced with `generateStaticParams`.

1. **Static VS SSG**: [link](https://nextjs.org/docs/pages/building-your-application/rendering/static-site-generation)

```
It’s all static HTML at the end of the day in both cases. Not much practical difference, both are generated at build time.

A static page that has no data fetching components is just rendered straight to HTML by Next. Next caches this HTML so that there is less generation happening when a static page loads. When you rebuild, this HTML gets regenerated.

With SSG you can fetch some data and bake it into your statically generated HTML. When you run build Next goes and fetches data via getStaticProps, hydrates your HTML with the data, then caches it all just like before. Rerun build to refetch the data.

```

| Feature       | ○ (Static)                  | ● (SSG)                               |
| ------------- | --------------------------- | ------------------------------------- |
| Data Fetching | ❌ None                     | ✅ getStaticProps                     |
| Use Case      | Hardcoded pages (e.g., FAQ) | Dynamic-but-pre-rendered (e.g., blog) |
| Performance   | ⚡ Fastest                  | ⚡ Fast (but slower than ○)           |

#### **Summary**

```
Page                              Size     First Load JS
┌ ○ /                            2.5 kB          80 kB (SSG) {Static Generation with and without Data}
├ ● /item/[id]                 1.8 kB          78 kB (SSG with getStaticProps)
├ ● /blog/[slug]                 1.8 kB          78 kB (SSG with getStaticProps) {Static but have data fetch so ( get the data Dynamic at pre-rendered the build time )} using getStaticProps
├ λ /dashboard                   5.1 kB          82 kB (SSR)
├ ● /products/[id] (ISR: 60s)    2.1 kB          79 kB (ISR)
└ ○ /about                       1.2 kB          77 kB (Static)
```

| Symbol  | Rendering Strategy                     | Example Page   | How to Identify in Code                  | When to Use                                  |
| ------- | -------------------------------------- | -------------- | ---------------------------------------- | -------------------------------------------- |
| ○       | Static (No Data Fetching)              | /, /about      | No getStaticProps/getServerSideProps     | Pure static pages (e.g., marketing).         |
| ●       | SSG (Pre-rendered with getStaticProps) | /blog/[slug]   | Uses getStaticProps                      | Content known at build time (e.g., blogs).   |
| ● (ISR) | ISR (Revalidated Static)               | /products/[id] | getStaticProps + revalidate: 60          | Semi-dynamic content (e.g., e-commerce).     |
| λ       | SSR (Server-Side Rendered)             | /dashboard     | Uses getServerSideProps                  | Real-time data (e.g., auth-protected pages). |
| ƒ       | Dynamic SSR (On-Demand)                | /profile/[id]  | Uses getServerSideProps + dynamic routes | User-specific content (e.g., profiles).      |

#### Client Components

Role: Handle interactivity (e.g., forms, animations) and browser APIs (e.g., localStorage).

Hydration: After server-rendered HTML (from server components) is sent, client components "hydrate" the page, attaching event listeners.

Data Fetching: Can fetch client-side data (e.g., using useEffect or libraries like SWR) but benefit from reduced load when paired with server components.

### hooks

1. usePathname

### random note

- async/await for server component, use hook for client component
- **layout.tsx** only have access to params (there is no searchParams)

![alt text](image.png)

[NPM Library Used In the Demo](NPMLibraryUsedIntheDemo.md)
