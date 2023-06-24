# Notes

Current place in [video](https://www.youtube.com/watch?v=2aeMRB8LL4o): 2:02

This is a running document of notes taken during the creation of this React project. This project is adapted from the video above.

**"How does `SidebarItem` inherit icons?"** <br>
`SidebarItem` is a functional component that receives props based on the interface `SidebarItemProps`. It returns a JSX element that represents a single sidebar item. We need to specify the type of Icon in the interface so that we can render the Icon in the return statement. In `Sidebar.tsx`, the `map` function iterates over the `routes` array and renders `SidebarItem` components based on the data provided.

**"What is `useMemo`?"** <br>
This is a hook in React that memoizes results of a function call and caches it for subsequent renders. In plain english, Memoization helps React remember results of previous renders so that it does not need to rerender commonly rendered components.
In `SidebarItem.tsx`, `routes` holds the result of invoking the `useMemo` hook, which is a `routes` array that is later accessed to render components.

**"What is `usePathname`?"** <br>
The pathname variable represents the current path or URL pathname of the page. It provides information about the current route or location within your application. In Next.js, the usePathname hook is specifically designed for retrieving the current pathname within a component. By invoking `usePathname()`, the pathname variable will be assigned the current pathname value. It is then used within the useMemo hook to compute and memoize the routes array based on the value of pathname.

**"What is `twMerge`?"** <br>
`twMerge` is a custom utility imported from `tailwind-merge` that lets us merge multiple Tailwind CSS classes or class strings together. Tailwind CSS provides pre-built CSS classes to style web apps. It follows a utility-first approach where we can apply small, single-purpose utility classes directly in HTML markup to style elements.
