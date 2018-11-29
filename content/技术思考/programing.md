---
title: 快速建站技术体系
weight: 2
---

## 起因
在快速建站过程中，以实现开发效率优先，功能全面的项目。在其过程中，需要使用一套完善的技术体系和完整的工作流程。因此有了以下的思考。

## wordpress体系

- 前端技术：icss(构建的class)
- 前端页面：[mdbootstrap](https://mdbootstrap.com) [Now UI](https://demos.creative-tim.com/now-ui-kit/index.html) wordpress现成主题
- 后端技术：wordpress

## react体系

- 前端技术：icss(构建的class)
- 前端页面：[mdbootstrap-react](https://mdbootstrap.com/docs/react/) [飞冰](https://alibaba.github.io/ice)
- 后端技术：调用接口

## 静态页生成器体系

> Hugo Hexo jekyll vuepress Gatsby Grav, 这些建站工具都用过，Hugo用的go语言的一种模板引擎，Hexo可以用ejs和jade，jekyll也是，vuepress用的vue，Gatsby用的React，Grav用的PHP。从效果来说，Hugo是最快的，从功能上来说，Gatsby的思路是最好的。

- 自己用：Hugo 比如这个平台
- 开发用：Gatsby
- 后台：netlify.com 自动生成静态页面，真的非常好。


## 特别新的思路

- 前端用Gatsby 
- 后端用Wordpress
- 前端调用后端的接口，生成全部的静态站部署。数据更新前端页面因为是调用接口，也会全站自动更新。
