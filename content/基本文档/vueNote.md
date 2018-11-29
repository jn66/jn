---
date: 2016-04-09T16:50:16+02:00
title: Vue笔记
weight: 15
---


# Vue 笔记

## 引入子组件

* 写好子组件 包含template script 和style标签
* 父组件中在script标签中导入 
```javascript  
    import footer from './components/footer.vue'
```
* 父组件中初始化
```javascript
    export default{
        components: {
            'w-footer': footer
        }
    }
```
* 父组件中使用w-footer标签使用
  
## 与后端交互
* 安装axios 
* 在main.js中引入 
```javascript
import axios from 'axios'
```
* 在原型上挂载axios
```javascript
Vue.prototype.$http = axios
```
* 在任何页面使用
```javascript 
export default{
    mounted () {
        this.$http.get('http://192.168.21.110/jiegou.php', {
        params: {
                a: 'blog'
            }
        }
        ).then((res) => {
            console.log(res, '请求成功')
            this.blog = res.data.data
        }, (err) => {
            console.log(err, '请求失败')
        })
    }
}
```

## 数组截取

```javascript
[1,2,3,4,5,6] => [[1,2],[3,4],[5,6]]

function chunk (arr, size) {
  return Array.from({ length: Math.ceil(arr.length / size) }, (v, i) => arr.slice(i * size, i * size + size))
}
```

## 绑定背景图片
```javascript
v-bind:style="{backgroundImage:'url('+mydata.imageURL+')'}"
```

## 直接引入css

在App.vue中的style标签
```javascript 
@import "./assets/css/style.css";
```

## 如何引入bulma，并修改其中的变量

* 安装node
* 替换淘宝源：npm install -g cnpm --registry=https://registry.npm.taobao.org
* 安装vue-cli：cnpm install -g @vue/cli
* 启动vue ui: vue ui
* 打开localhost:8000 在vue ui中创建一个项目
* 在vue ui中安装依赖：bumla   node-sass   sass-loader
* 在src/assets/custom.sass 中可以引入变量，修改变量，然后引入剩余的部分

```javascript
@import '../../node_modules/bulma/sass/utilities/initial-variables.sass';
@import '../../node_modules/bulma/sass/utilities/functions.sass';

$primary: lightblue; /* changes primary color to pink */
@import '../../node_modules/bulma/bulma.sass';
```
* 在main.js 中顶部，引入全局的修改好的bulma的 css文件
```javascript
import './assets/style.sass'
```
