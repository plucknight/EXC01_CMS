# CMS

This template should help get you started developing with Vue 3 in Vite.
该项目是一个基于 Vue3 框架的前端应用，使用 Element-Plus UI 框架、Pinner 状态管理、Echart5× 可视化工具，以及 @vueuse/core、dayjs、countup.js 等工具库，同时采用了 Git Hook 工具 husky、Axios HTTP 工具、Vue Router 4.x 路由工具。项目采用 TypeScript4.x+JavaScript 编程语言，Vue 3.x+setup 前端框架。
练习此项目，推荐的速成学习路线：html+css，js，node.js,包管理工具（npm、cnpm、npx、pnpm），webpack打包工具，git，Vue3，ts，前端可视化，VueCLI和Vite。
本项目只是为了记录，也可用于学习分享。
项目笔记还再整理，下周再放这里。

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
    1) Run `Extensions: Show Built-in Extensions` from VSCode's command palette
    2) Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
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

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
