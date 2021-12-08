### 基于Nextjs重构的react-travel([react-travel项目请点击此链接查看](https://github.com/jsdegithub/react-travel))项目，从CSR客户端渲染重构为SSR服务端渲染，加快了首屏渲染速度

### 项目演示：[点击链接查看项目演示](http://8.217.9.69:3000/)（不要使用代理访问网站，否则会被拦截）

### 技术栈： Nextjs+React+Hooks+Antd+ReactRouter+Redux+React-redux+ReduxToolkit

### 部署方案：Docker+阿里云ECS+阿里云容器镜像服务+阿里云SSL单域名证书+nginx接口代理
编写Dockerfile制作镜像，推送到阿里云镜像仓库，再从ECS服务器拉取镜像；

### 优化方案：
1、lazy+Suspense路由懒加载，大大减少了白屏时间（路由系统放在App.js中）；

2、TreeShaking去除引用库中没有使用的代码，减少了白屏时间和首屏加载时间；

3、CodeSplitting代码分割，减少了白屏时间和首屏加载时间；

4、全站图片懒加载，大大减少了各组件加载时间（使用了react-lazy-load-image-component）；

5、TinyPNG本地图片压缩，减少了首屏加载时间；

6、最大化压缩了index.js和App.js的体积，大大缩短了白屏时间；

7、React.memo+useMemo+useCallback子组件性能优化；

8、经测试，白屏时间:0.7s，TimeToInteractive:1.8s，DOMContentLoaded:3s，首屏完全加载时间8s；

9、服务器图片资源未经压缩，对首屏加载速度影响较大。
