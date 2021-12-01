# **NextJs**

## **Assets, Metadata, and CSS**

### **Assets**

Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.

### **Metadata**

What if we wanted to modify the metadata of the page, such as the `<title>` HTML tag?

`<title>` is part of the `<head>` HTML tag, so let's dive into how we can modify the `<head>` tag in a Next.js page.

Open pages/index.js in your editor and find the following lines:

```JS
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```

### **CSS Styling**

Let’s now talk about CSS styling.

As you can see, our index page (http://localhost:3000) already has some styles. If you take a look at pages/index.js, you should see code like this:

<style jsx>{`
  …
`}</style>

This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).

Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.

***

**To know more please [visit this page](https://nextjs.org/learn/basics/assets-metadata-css)**

