# *Course 401 Python, Entry 41: React 4

**Explain the concept of dynamic routes in Next.js and how they differ from static routes.**

Unlike static routes, dynamic routes have URLs which are generated, dependent on external data. Dynamic routes begin and end with square brackets.

Additionally, an asynchronous function called "getStaticPaths" will be exported. This is for the id values.

A getStaticProps function with fed in params will be implemented to fetch the data for the page.

A `[id].js` file is needed for the canvas for the generated code.

APIs can be used to fetch data from.

Note:

"In development (npm run dev or yarn dev), getStaticPaths runs on every request.
In production, getStaticPaths runs at build time."

For unexpected errors, see [https://nextjs.org/learn-pages-router/basics/dynamic-routes/dynamic-routes-details](https://nextjs.org/learn-pages-router/basics/dynamic-routes/dynamic-routes-details)

**Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?**

Starter code:

`npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/main/basics/basics-final"`

1. Push to GitHub.
2. Signup with Vercel. Import the nextjs-blog repository created in previous steps. Settings don't need changed as they are automatically optimal set. [https://vercel.com/import/git.](https://vercel.com/import/git)
3. Go to your live site!

Other hosts can be used. Reference the package.json file for usefull information. Run `npm run build` once. The run script is `npm run start`.

**How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application.**

Static files are served via the "public" folder. When referencing a file location, "public" can be left off from the directory.

An example of implementation:

```
export function Avatar({ id, alt }) {
  return <Image src={`/avatars/${id}.png`} alt={alt} width="64" height="64" />
}
 
export function AvatarOfMe() {
  return <Avatar id="me" alt="A portrait of me" />
}
```

Caching can not occur in the public folder and is by default turned off.

This is also a good folder for robots.txt and favicon.ico files.

## Things I want to know more about

I would like to learn how to automate indexing for generated pages.
