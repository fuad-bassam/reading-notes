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

1. (IRS) server side render at run time
1. (SSG)(CSR) pre-rendered as static content
1. (SSR) ƒ (Dynamic) server-rendered on demand

```
Page                              Size     First Load JS
┌ ○ /                            2.5 kB          80 kB (SSG) {Static Generation with and without Data}
├ ● /blog/[slug]                 1.8 kB          78 kB (SSG with getStaticProps) {Static but have data fetch so ( get the data Dynamic at  pre-rendered the build time )} using getStaticProps
├ λ /dashboard                   5.1 kB          82 kB (SSR)
├ ● /products/[id] (ISR: 60s)    2.1 kB          79 kB (ISR)
└ ○ /about                       1.2 kB          77 kB (Static)
```

#### Server Components & Rendering Strategies

SSR (Server-Side Rendering):

Server Components: Rendered on the server on every request, fetching fresh data for dynamic content (e.g., user-specific pages).

Use Case: Ideal for highly dynamic content requiring real-time data (e.g., dashboards).

Trade-off: Higher server load and latency but ensures up-to-date content.

SSG (Static Site Generation):

Server Components: Rendered at build time, generating static HTML. Data is pre-fetched once (e.g., blog posts).

Use Case: Content that rarely changes (e.g., documentation, marketing sites).

Trade-off: Blazing-fast performance but requires rebuilds for updates.

ISR (Incremental Static Regeneration):

Server Components: Rendered at build time and revalidated on-demand or at intervals. Combines SSG’s speed with dynamic updates (e.g., product pages).

Use Case: Semi-dynamic content needing periodic updates without full rebuilds.

Trade-off: Balances freshness and performance via revalidation (e.g., revalidate: 60 seconds).

#### Client Components

Role: Handle interactivity (e.g., forms, animations) and browser APIs (e.g., localStorage).

Hydration: After server-rendered HTML (from server components) is sent, client components "hydrate" the page, attaching event listeners.

Data Fetching: Can fetch client-side data (e.g., using useEffect or libraries like SWR) but benefit from reduced load when paired with server components.

### hooks

1. usePathname

### random note

- async/await for server component, use hook for client component
- **layout.tsx** only have access to params (there is no searchParams)

```

```

![alt text](image.png)
[NPM Library Used In the Demo](NPMLibraryUsedIntheDemo.md)
