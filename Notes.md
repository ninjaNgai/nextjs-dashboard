## Colocation

What is colocation?
In Next.js, you can't access a route unless you add a special file (like page.js/page.tsx) to the right folder.

### Pros and Cons

The pros and cons of colocation in Next.js App Router:

Pros:

1. Safe colocation by default: Even though route structure is defined through folders, a route is not publicly accessible until a page.js or route.js file is added to a route segment. This means project files can be safely colocated inside route segments in the app directory without accidentally being routable [2].

2. Flexibility in project organization: Next.js is unopinionated about how you organize and colocate your project files apart from routing folder and file conventions [2].

3. Ability to keep components organized: You can group related components together under route segments, making it easier to manage and maintain your codebase [4].

4. Server-side rendering: Components placed inside the /app directory will render on the server by default, which can improve initial page loading times and SEO [4].

5. Route groups: Next.js allows you to create route groups using parentheses, which helps organize routes without affecting the URL structure [4].

Cons:

1. Complexity: Colocation requires careful planning to avoid accidentally creating routable pages. It's important to understand the difference between the app directory and the pages directory [2].

2. Potential for confusion: Without proper organization, colocation can lead to confusion about what constitutes a route and what doesn't [4].

3. Performance considerations: While server-side rendering can improve performance, it also means that some components will be rendered on the server, potentially slowing down interactive elements [4].

4. Learning curve: Understanding how to properly utilize colocation in Next.js App Router requires knowledge of its specific features and limitations [2][4].

In conclusion, colocation in Next.js App Router offers flexibility in project organization but requires careful management to avoid unintended consequences. It's particularly useful for organizing components and leveraging server-side rendering, but it demands attention to detail and understanding of Next.js routing principles.

Citations:
[1] https://www.reddit.com/r/nextjs/comments/148d4p7/what_are_your_experiences_with_the_app_router_by/
[2] https://nextjs.org/docs/app/building-your-application/routing/colocation
[3] https://github.com/vercel/next.js/discussions/59373
[4] https://stackoverflow.com/questions/76214501/nextjs-13-folder-structure-best-practice
[5] https://jc1175.medium.com/a-crash-course-in-next-js-8d320f12a3c6
[6] https://www.liquidweb.com/blog/managed-colocation-pros-and-cons/
[7] https://medium.com/@shavaizali159/next-js-api-routes-vs-server-actions-which-one-to-use-and-why-809f09d5069b
[8] https://www.inngest.com/blog/5-lessons-learned-from-taking-next-js-app-router-to-production
[9] https://dev.to/jonathan-dev/nextjs-best-way-to-organize-your-project-structure-25o6
[10] https://pagepro.co/blog/whats-next-14/

## Next.js 13 Page Router differences

Next.js 13 does not have colocation support. Instead, when a file is added to the `pages` directory, it's automatically available as a route.
