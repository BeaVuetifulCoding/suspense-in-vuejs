# Suspense in [<img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_vue_icon_130078.png" width="30px"/>](https://vuejs.org/)ue 3 <br>

## Description 📜

---

Tutorial about the use of Suspense in Vue 3 with practical examples 🤗

In the tutorial I demonstrated the basic usage of Suspense with nested async child component and loading state (I used the Spinner component that I also created in this tutorial), lazy loading components (created with defineAsincComponent), usage of 3 emitted events: pending, resolve and fallback and some ideas what you can do with this emitted events, onErrorCaptured hook for capturing async errors from descendent component and use of Suspense with other built-in components such as Transition, KeepAlive and "component" which is meta-component.

About Suspense 🚦

Suspense is a built-in component in Vue 3, that can render a loading state while waiting for nested async dependencies to be resolved. The important thing to remember is that Suspense is an experimental feature, but according to the last Vue.js Nation Conference, Vue.js core team members are predicting a stable release for the second quarter of 2023, which is probably going to be released in version 3.4.<br/>

Suspense can wait on two types of dependencies: components with async setup() hook (script setup with the use of top-level await or setup() hook with an async keyword before it) and Async Components (that are used with defineAsyncComponents function).

---

## [Link](https://www.youtube.com/watch?v=IJohEZrLWEA) to YouTube tutorial 🔗

---

## 📖 Resources

---

[JSON Placeholder](https://jsonplaceholder.typicode.com/) - Fake REST API used in this tutorial 🌐

[Guide](https://tailwindcss.com/docs/guides/vite#vue) on how to install [Tailwindcss](https://tailwindcss.com/) in [Vue.js](https://vuejs.org/) project that uses [Vite](https://vitejs.dev/) 📑

## Other resources 📚

---

### Vue.js ⛰️

- https://vuejs.org/guide/built-ins/suspense.html#suspense
- https://vuejs.org/guide/components/async.html#async-components
- https://vuejs.org/api/built-in-special-elements.html#component
- https://vuejs.org/guide/built-ins/keep-alive.html#keepalive
- https://vuejs.org/guide/built-ins/transition.html#transition

### Vue Router 🚧

- https://router.vuejs.org/

### Vite ⚡

- https://vitejs.dev/

### Tailwindcss 🌬️

- https://tailwindcss.com/

### VSCode Extensions 🧩

- https://marketplace.visualstudio.com/items?itemName=Vue.volar
- https://marketplace.visualstudio.com/items?itemName=sdras.vue-vscode-snippets
- https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin
- https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss

---

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
   1. Run `Extensions: Show Built-in Extensions` from VSCode's command palette
   2. Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```
