# Next js

## random note

### Routing

#### Routing pages info

1.  **[id]** for dynamic routing
2.  **[...slug]**
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

#### rendering types

1. (IRS) server side render at run time
1. (SSG)(CSR) pre-rendered as static content
1. (SSR) ƒ (Dynamic) server-rendered on demand

### hooks

1. usePathname

### random note

- async/await for server component, use hook for client component
- **layout.tsx** only have access to params (there is no searchParams)

```

```

![alt text](image.png)
[NPM Library Used In the Demo](NPMLibraryUsedIntheDemo.md)
