## 项目演示：[点击链接查看项目演示](http://travel.aeeternity.com:3000/)（不要使用代理，否则网站将无法正常访问）

这是基于 Nextjs 重构的 react-travel SSR 项目，从 CSR 客户端渲染重构为 SSR 服务端渲染，大大加快了首屏渲染速度（[react-travel客户端渲染项目请点击此链接查看](https://github.com/jsdegithub/react-travel)）；

经测试，白屏时间仅有0.4s，首屏加载时间2.8s。

### 技术栈： Nextjs+React+Hooks+Antd+Redux+React-redux+ReduxToolkit

### 部署方案：Docker+阿里云ECS+阿里云容器镜像服务
编写 Dockerfile 制作镜像，推送到阿里云镜像仓库，再从ECS服务器拉取镜像。

### 性能报告：
First Contentful Paint => 0.4s

Time to Interactive => 1.2s

Speed Index => 2.5

Total Blocking Time => 30ms

Largest Contentful Paint => 2.3s

Cumulative Layout Shift => 0.006
