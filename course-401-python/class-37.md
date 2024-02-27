# *Course 401 Python, Entry 37: React 1

**After reading “Tailwind in 15 minutes,” can you describe the purpose of utility classes in Tailwind CSS and provide an example of how to use them to style an HTML element?**

Traditional

```
<div class="chat-notification">
  <div class="chat-notification-logo-wrapper">
    <img class="chat-notification-logo" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div class="chat-notification-content">
    <h4 class="chat-notification-title">ChitChat</h4>
    <p class="chat-notification-message">You have a new message!</p>
  </div>
</div>

<style>
  .chat-notification {
    display: flex;
    max-width: 24rem;
    margin: 0 auto;
    padding: 1.5rem;
    border-radius: 0.5rem;
    background-color: #fff;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  .chat-notification-logo-wrapper {
    flex-shrink: 0;
  }
  .chat-notification-logo {
    height: 3rem;
    width: 3rem;
  }
  .chat-notification-content {
    margin-left: 1.5rem;
    padding-top: 0.25rem;
  }
  .chat-notification-title {
    color: #1a202c;
    font-size: 1.25rem;
    line-height: 1.25;
  }
  .chat-notification-message {
    color: #718096;
    font-size: 1rem;
    line-height: 1.5;
  }
</style>
```

TailwindCSS

```
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
  </div>
</div>
```

Examples via tailwindcss.com

As can be seen, TailwindCSS is much more concise. Noted, it won't always be the case that TailwindCSS is more efficient, but for most applications, the simple limited nature of any CSS lends well to using TailwindCSS. TailwindCSS allows for standardization in things like React, but with much more flexibility.

**Based on “Why to use Next.js,” explain the main advantages of using Next.js for web development, and provide a brief comparison between traditional client-side rendering and Next.js’s server-side rendering approach.**

Next.js is a merger from client-side and server-side, allowing for flexibility between the two, leaning one way or the other depending on needs. This allows for flexibility in scaling.

- React Fast Refresh allows for preserving state during component changes.
- Error codes are identified by the line via modal.
- Images and script files are easy to add.
- Image optimization and internationalization is automatically added.
- Next export allows to export a static site. 
- Redirects and re-writes are allowed, making it easy to rollup and legacy site.

## Things I want to know more about

How Next.js being optionally client-side is relevant. 
