# ReportBro Designer（报表设计器）

一个用于创建 PDF 和 XLSX 报表模板的 JavaScript 插件。

ReportBro Designer 可以轻松集成到你的 Web 应用中。任何人都可以设计和编辑文档模板，并在浏览器中直接预览。报表可通过服务器端的 [ReportBro Lib](https://github.com/jobsta/reportbro-lib)（Python 包）进行生成。

完整文档和演示请访问项目官网：https://www.reportbro.com

<p align="center">
  <img alt="ReportBro Designer 使用截图" src="https://www.reportbro.com/static/images/reportbro_designer_screenshot.png">
</p>

## 安装

+ 从 https://github.com/jobsta/reportbro-designer/releases 下载 ReportBro Designer（`reportbro-designer-<version>.tgz`）
+ 解压 .tgz 文件并将 `dist` 文件夹移动到你的应用目录
+ 在 HTML 文档中引用 reportbro.js 和 reportbro.css，参考下方基本用法

### 通过 npm 安装：

`npm install reportbro-designer --save`

## 基本用法

更多信息请参考 [开发文档](https://www.reportbro.com/framework/api)。不同场景的演示见：https://www.reportbro.com/demo/invoice

在页面 `<head>` 部分引入 ReportBro 的 JS 和 CSS：

```html
<link rel="stylesheet" href="reportbro/reportbro.css"/>
<script src="reportbro/reportbro.js"></script>
```

在 `<body>` 中放置一个空的 div：
```html
<div id="reportbro"></div>
```

初始化 ReportBro：
```html
<script type="text/javascript">
    const rb = new ReportBro(document.getElementById('reportbro'));
</script>
```

## 构建

### 前置条件：

需先安装 Node.js 和 npm。

Ubuntu/Linux 如遇到 "usr/bin/env: node: No such file or directory" 错误，可用以下命令修复：

`ln -s /usr/bin/nodejs /usr/bin/node`

进入 reportbro-designer 根目录，安装依赖：

`npm install`

### 开发环境构建：

`npm run build`

此命令可快速构建并调试，生成的 dist/reportbro.js 可在支持 ES6 的现代浏览器中直接使用。

### 生产环境构建：

`npm run build-prod`

此命令会将 JS 代码从 ES6 转译为 ES5，兼容老旧浏览器，并压缩生成的 js 文件。用于生产环境部署。

## 说明

### 本地运行演示

首次本地运行演示前，需先执行：

`npm run build-prod`

该命令会在 `dist` 目录下生成 ReportBro Designer，供演示页面引用。

## 许可证

### 商业授权

如需将 ReportBro 用于商业项目，请购买商业授权。该授权允许你的源码保持私有。购买地址：https://www.reportbro.com/framework/license

商业授权包含 ReportBro PLUS 及更多高级功能。

### 开源协议

如你的项目采用与 [GNU AGPL v3](https://www.gnu.org/licenses/agpl-3.0.html) 兼容的开源协议，可按 AGPLv3 协议免费使用 ReportBro。

更多授权说明详见：https://www.reportbro.com/framework/license 