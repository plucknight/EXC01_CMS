# CMS

  该项目是一个基于 Vue3 框架的前端应用，使用 Element-Plus UI 框架、Pinner 状态管理、Echart5× 可视化工具，以及 @vueuse/core、dayjs、countup.js 等工具库，同时采用了 Git Hook 工具 husky、Axios HTTP 工具、Vue Router 4.x 路由工具。项目采用 TypeScript4.x+JavaScript 编程语言，Vue 3.x+setup 前端框架。
	
  练习此项目，推荐的速成学习路线：html+css，js，node.js,包管理工具（npm、cnpm、npx、pnpm），webpack打包工具，git，Vue3，ts，前端可视化，VueCLI和Vite。
		
  本项目学习自coderwhy，只是为了记录，也可用于学习分享。
	
  项目目录：
  ```
CMS
├── README.md
├── auto-imports.d.ts
├── components.d.ts //element-plus导入的文件
├── env.d.ts //vite配置全局变量
├── index.html 
├── package-lock.json //node_modules的包结构快照 实际安装包的版本
├── package.json //安装包的版本范围
├── public 
│   └── favicon.ico
├── src
│   ├── App.vue
│   ├── assets	
│   │   ├── css
│   │   │   ├── common.less
│   │   │   ├── index.less
│   │   │   └── reset.less
│   │   └── img
│   │       ├── login-bg.svg
│   │       └── logo.svg
│   ├── base-ui
│   ├── **components** 	//组件
│   │   ├── main-header //头框架
│   │   │   ├── c-cpns
│   │   │   │   ├── header-crumb.vue
│   │   │   │   └── header-info.vue //面包屑实现
│   │   │   └── main-header.vue
│   │   ├── main-menu //菜单框架
│   │   │   └── main-menu.vue
│   │   ├── page-content //内容框架
│   │   │   └── page-content.vue 
│   │   ├── page-echarts //echart组件
│   │   │   ├── data
│   │   │   │   └── china.json
│   │   │   ├── index.ts //统一出口
│   │   │   ├── src //封装echarts 统一使用
│   │   │   │   ├── bar-echart.vue
│   │   │   │   ├── base-echart.vue //基本
│   │   │   │   ├── line-echart.vue
│   │   │   │   ├── map-echart.vue
│   │   │   │   ├── pie-echart.vue
│   │   │   │   └── rose-echart.vue
│   │   │   ├── types
│   │   │   │   └── index.ts
│   │   │   └── utils
│   │   │       ├── convert-data.ts //格式化数据
│   │   │       └── coordinate-data.ts //数据
│   │   ├── page-modal 
│   │   │   ├── page-modal.vue 
│   │   │   └── type.ts
│   │   └── page-search  
│   │       └── page-search.vue 
│   ├── **global**  //全局
│   │   ├── constants.ts  //常量
│   │   └── register-icons.ts	//图标抽离成单独的文件
│   ├── **hooks**//回调函数
│   │   ├── usePageContent.ts	//选择重置按钮
│   │   ├── usePageModal.ts //获取数据 实现权限分配
│   │   └── usePermissions.ts //实现按钮权限
│   ├── main.ts 
│   ├── **router**//路由 映射
│   │   ├── index.ts //路由配置 导航守卫
│   │   ├── login
│   │   └── main //添加路由对象
│   │       ├── analysis 
│   │       │   ├── dashboard
│   │       │   │   └── dashboard.ts
│   │       │   └── overview
│   │       │       └── overview.ts 
│   │       ├── product
│   │       │   ├── category
│   │       │   │   └── category.ts
│   │       │   └── goods
│   │       │       └── goods.ts
│   │       ├── story
│   │       │   ├── chat
│   │       │   │   └── chat.ts
│   │       │   └── list
│   │       │       └── list.ts
│   │       └── system
│   │           ├── department
│   │           │   └── department.ts
│   │           ├── menu
│   │           │   └── menu.ts
│   │           ├── role
│   │           │   └── role.ts
│   │           └── user
│   │               └── user.ts
│   ├── **service**
│   │   ├── config
│   │   │   └── index.ts	//封装axios请求 配置开发环境和生产环境
│   │   ├── index.ts //拦截：拦截器的执行顺序为实例请求→类请求→实例响应→类响应 处理登录 token
│   │   ├── login
│   │   │   └── login.ts  //登录网络请求
│   │   ├── main
│   │   │   ├── analysis //对应的 商品统计页面网络请求
│   │   │   │   └── analysis.ts
│   │   │   ├── main.ts //获取所有角色和所有部门的请求
│   │   │   └── system
│   │   │       └── system.ts //封装用户管理页部门管理等  网络请求 增删改
│   │   └── request
│   │       ├── index.ts //接口 封装类
│   │       └── type.ts	//实例拦截器
│   ├── **store** //状态管理配置 本项目里发送请求全部封装在**对应**的状态管理器的actions里
│   │   ├── index.ts //导出接口
│   │   ├── login	//动态添加路由
│   │   │   └── login.ts	//状态管理-获取信息（菜单信息） 加载本地数据
│   │   └── main
│   │       ├── analysis	// 对应的 商品统计页面 状态管理
│   │       │   └── analysis.ts
│   │       ├── main.ts 
│   │       └── system //对应的 用户管理页部门管理等 状态管理
│   │           ├── system.ts  //增删改
│   │           └── type.ts
│   ├── **types** //网络请求->service/login/login.ts
│   │   ├── index.ts 
│   │   └── login.ts
│   ├── **utils** //封装工具
│   │   ├── cache.ts //封装本地存储工具
│   │   ├── format.ts //格式话
│   │   └── map-menus.ts //封装菜单动态的添加路由对象 映射权限
│   └── **views** //基本布局
│       ├── login 
│       │   ├── Login.vue
│       │   └── c-cpns
│       │       ├── login-panel.vue
│       │       ├── pane-account.vue
│       │       └── pane-phone.vue
│       ├── main
│       │   ├── analysis
│       │   │   ├── dashboard //商品统计页面
│       │   │   │   ├── c-cpns
│       │   │   │   │   ├── chart-card
│       │   │   │   │   │   └── chart-card.vue //echart组件可视化
│       │   │   │   │   └── count-card
│       │   │   │   │       └── count-card.vue //引入countup.js创建动画
│       │   │   │   └── dashboard.vue
│       │   │   └── overview
│       │   │       └── overview.vue
│       │   ├── main.vue //home页面
│       │   ├── product
│       │   │   ├── category
│       │   │   │   └── category.vue
│       │   │   └── goods
│       │   │       └── goods.vue
│       │   ├── story
│       │   │   ├── chat
│       │   │   │   └── chat.vue
│       │   │   └── list
│       │   │       └── list.vue
│       │   └── system
│       │       ├── department	//部门管理
│       │       │   ├── c-cpns
│       │       │   │   ├── page-content.vue
│       │       │   │   ├── page-modal.vue //编辑新建部门
│       │       │   │   └── page-search.vue 
│       │       │   ├── config //配置文件
│       │       │   │   ├── content.config.ts
│       │       │   │   ├── modal.config.ts
│       │       │   │   └── search.config.ts //抽取封装pageSearch
│       │       │   ├── department.vue	//界面实现
│       │       │   └── department_v1.vue
│       │       ├── menu
│       │       │   ├── config
│       │       │   │   └── content.config.ts //配置文件
│       │       │   └── menu.vue //直接传入配置文件
│       │       ├── role //角色管理 利用组件快速搭建
│       │       │   ├── config
│       │       │   │   ├── content.config.ts
│       │       │   │   ├── modal.config.ts //增加树形控件
│       │       │   │   └── search.config.ts
│       │       │   └── role.vue
│       │       └── user //用户管理
│       │           ├── c-cpns
│       │           │   ├── user-content.vue //数据展示 作用域插槽
│       │           │   ├── user-modal.vue //新增功能封装模态框 修改回显
│       │           │   └── user-search.vue
│       │           └── user.vue //基本页面结构
│       └── not-found
│           └── NotFound.vue //404配置
├── tsconfig.json	//TypeScript 使用 tsconfig.json 文件作为其配置文件,该目录为 TypeScript 项目的根目录类型提示
├── tsconfig.node.json	//指定ts编译所需根文件和编译器选项
└── vite.config.ts //vite项目配置
```
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
