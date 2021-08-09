# Routify Notus Svelte Starter

![Notus Svelte](https://github.com/creativetimofficial/public-assets/blob/master/notus-svelte/notus-svelte.jpg?raw=true)

Starter template for [Notus Svelte](https://github.com/creativetimofficial/notus-svelte) using [Routify](https://github.com/roxiness/routify).

### Installation

```bash
npx degit azlkiniue/routify-notus folder-name
cd folder-name
npm install
npm run dev
```

### npm scripts

| Syntax           | Description                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------|
| `dev`            | Development (port 5000)                                                                                 |
| `dev:nollup`     | Development with crazy fast rebuilds (port 5000)                                                        |
| `dev-dynamic`    | Development with dynamic imports                                                                        |
| `build`          | Build a bundled app with SSR + prerendering and dynamic imports                                         |
| `serve`          | Run after a build to preview. Serves SPA on 5000 and SSR on 5005                                        |
| `deploy:*`       | Deploy to netlify or now, [more info](https://github.com/roxiness/routify-starter#ssr-and-pre-rendering)|
| `export`         | Create static pages from content in dist folder (used by `npm run build`)                               |

### Features
- Using Tailwind JIT Mode for faster build times.
- Updated Chart.js (from 2.x to 3.x) and other dependencies.

### Why
<details>
  <summary>Short Answer</summary>

  Why not?
</details>

<details>
  <summary>Long Answer</summary>

  I really like file-based router for this template since it's easier to maintain. At first, I want to use <a href="https://sapper.svelte.dev">Sapper</a>. But, since it was no longer updated because it will be replaced with <a href="https://kit.svelte.dev/">SvelteKit</a> - which is still in heavy development, my choice goes to <a href="https://routify.dev">Routify</a>.
</details>

### Resources
- [Routify Starter Template](https://github.com/roxiness/routify-starter)
- [Notus Svelte Documentation](https://www.creative-tim.com/learning-lab/tailwind/svelte/overview/notus)