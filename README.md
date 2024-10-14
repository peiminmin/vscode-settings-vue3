# VSCode 配置：Vue3 项目开发环境

---

## 说明：

本项目是为了统一 VSCode 前端在开发 Vue3 项目时所使用的格式化配置和 Lint 规则，规范代码风格，提升代码质量。

如果你的项目是基于 `Vue 2.x` 的，请移步 [vscode-settings-vue2](https://github.com/fudiwei/vscode-settings-vue2)。

包括如下功能：

-   基于 `Vue 3.x` + `Vue-CLI 5` / `Vite 2`。

-   解决了 `Prettier`、`ESlint`、`Volar` 等几个插件冲突问题。

-   提供了主流前端项目的通用 `Git` 忽略项。

-   提供了 `TypeScript` 的支持。

其中有关格式化的配置作出了如下统一：

-   统一文件字符集：无 BOM 的 UTF-8；

-   统一文本缩进方式：4 个空格；

-   统一文本单行长度：120 个字符；

-   统一文本换行格式：CRLF（Windows）；

-   统一文本结尾空行：1 个；

-   统一 JavaScript 分号风格：强制包含结尾分号；

-   统一 JavaScript 引号风格：强制使用单引号；

-   其余未列出事项遵循各插件的默认值。

---

## 使用步骤：

### 安装 VSCode 插件

> 注意：以下插件在 VSCode 插件商店中可能存在多个同名搜索结果，请以括号内的插件名为准。

-   **EditorConfig for VS Code**（插件名：`editorconfig.editorconfig`）

-   **Prettier - Code formatter**（插件名：`esbenp.prettier-vscode`）

-   **ESLint**（插件名：`dbaeumer.vscode-eslint`）

-   **Vue Language Features (Volar)**（插件名：`Vue.volar`）
-   **Stylelint**（插件名：`stylelint.vscode-stylelint`）


如果你有曾安装过 **Vetur**，请先禁用，否则可能与 **Volar** 存在潜在的冲突。

### 配置 VSCode

使用 `pnpm create vite` 脚手架初始化项目后，将本项目根目录下 `settings` 文件夹中的全部文件，拷贝到对应开发项目的根目录中，覆盖同名文件。

### 安装 npm 依赖

> 注意：为了避免因版本问题造成的配置冲突，安装时请务必指定特定版本号。

```shell
# 以 npm 为例，使用 yarn 等其他包管理工具的请自行替换成相应命令。

pnpm install --save-dev @babel/core@7.23
pnpm install --save-dev @rushstack/eslint-patch@1.5
pnpm install --save-dev @vue/eslint-config-prettier@8.0
pnpm install --save-dev @vue/eslint-config-typescript@12.0
# eslint javascript代码检测工具
pnpm install --save-dev eslint@8.15
pnpm install --save-dev eslint-plugin-vue@9.17
# prettier  代码格式化工具
pnpm install --save-dev prettier@3.0
pnpm install --save-dev tslib@latest
pnpm install --save-dev typescript@latest
pnpm install --save-dev stylelint@latest
pnpm install --save-dev stylelint-config-standard@latest
pnpm install --save-dev stylint-scss@latest
pnpm install --save-dev stylelint-config-prettier@latest
pnpm install --save-dev stylelint-order@latest
pnpm install --save-dev typescript @vue/tsconfig
pnpm install --save-dev @types/node
```


-   使用 Vite 的项目还需额外安装：

```shell
pnpm install --save-dev @vue/tsconfig@latest
pnpm install --save-dev vite@latest
pnpm install --save-dev vue-tsc@latest
```

### 开发

在 VSCode 内开始开发吧！

按 `Ctrl + S` 时文件就会自动格式化并执行 Lint 操作。
