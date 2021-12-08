## 项目演示：[点击链接查看项目演示](http://8.217.9.69:3000/)（不要使用代理，否则网站将无法正常访问）

这是基于 Nextjs 重构的 react-travel SSR 项目，从 CSR 客户端渲染重构为 SSR 服务端渲染，加快了首屏渲染速度（[react-travel客户端渲染项目请点击此链接查看](https://github.com/jsdegithub/react-travel)）。

### 技术栈： Nextjs+React+Hooks+Antd+Redux+React-redux+ReduxToolkit

### 部署方案：Docker+阿里云ECS+阿里云容器镜像服务
编写 Dockerfile 制作镜像，推送到阿里云镜像仓库，再从ECS服务器拉取镜像。
