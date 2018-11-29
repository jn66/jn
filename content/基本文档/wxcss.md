---
date: 2016-04-09T16:50:16+02:00
title: icss开源项目文档
weight: 15
---


# wx-css 

## 简介
wxcss(无线css)是实用优先开箱即用(utility-first)的CSS UI开发框架。借鉴了tailwindcss和tachyons等国外框架的写法，*融合了知网赛事星手机知网的开发需求*。皆在解决后端工程师局部样式修复的问题。

## 原则

- 全部内容响应式设计，多终端呈现
- 可读性强，不论何种设备，内容清晰可读
- 模块化，wxcss不仅是一个整体框架，更是多模块的集合，可以按需使用。
- 无障碍。整个问题提供了许多工具和方法，使得框架最大程度使用
- 优化。代码进行了高度优化。
- 可复用。清晰的文档有助于团队分享和一致使用。大量复用代码减少冗余量。

## 特点

- 轻量级。整个框架少于14KB，如果想要更少，可以压缩和删除不需要的内容。
- 文档化。整个项目有清晰的文档，方便使用理解。
- 函数画。可以容易建立组件，在各种框架中使用。
- 定制化。提供丰富变量，定制框架，他不仅是css工具，更是生态体系。
- 无影响的。开箱即用，无需担心样式覆盖。节约调试时间。
- 低侵入的。大部分权重为10，无需担心影响现有项目风格。可以用在现有项目上。
- 颜色多样的。有480种颜色可以使用。
- 手机优先结构。默认情况下能够被同名class覆盖，方便使用。
- 可组合类。从单一样式到复杂布局，应有尽有。
- 方便调整扩展。能够方便编辑各类名称。


## 全部项目
wx-css 实用优先开箱即用(utility-first)的CSS UI开发框架

wx-sass 非侵入式sass mixins开发库

wx-hexo-starter Hexo静态页生成器主题脚手架

wx-vue 又一套vue前端UI库

wx-npm npm-script启动脚手架 替代gulp和grunt

wx-css-note css学习进步笔记

wx-vue-note vue学习进步笔记

## 使用方法
引入对应css后，加上对应的class即可生效，无需修改和书写任何css内容。
如默认链接下面有下划线，想要重置链接样式，去掉下划线。通过查询下表，得知加上link的class，可以产生此效果，于是：
```html
<a class="link">这是个链接</a>
```

## ELEMENTS 元素工具
链接| 
---|---
link|使链接没有下划线，鼠标交互颜色变化0.15秒

列表 |
--|--
list | 取消list前面的默认原点

表单| 
---|---
input-reset|重置input表单
button-reset|重置表单提交按钮

tabel| 
---|---
collapse|去掉表格之间space，合并表格之间间距
striped--light-silver| 奇数偶数行变色为这种颜色
striped--moon-gray| 奇数偶数行变色为这种颜色
striped--light-gray| 奇数偶数行变色为这种颜色
striped--near-white| 奇数偶数行变色为这种颜色
stripe-light| 修改为 $white-10 颜色
stripe-dark| 修改为 $black-10 颜色

## skin 颜色外观

文字颜色| 
---|---
black-90 black-80 black-70 black-60 black-50 <br/> black-40 black-30 black-20 black-10 black-05|black near-black dark-gray mid-gray gray silver <br/> light-silver moon-gray light-gray near-white white
white-90 white-80 white-70 white-60 white-50 <br/> white-40 white-30 white-20 white-10 white-05|dark-red red light-red orange gold yellow light-yellow <br/>purple light-purple dark-pink hot-pink pink light-pink dark-green  <br/>green light-green navy dark-blue blue light-blue lightest-blue <br/>washed-blue washed-green washed-yellow washed-red color-inherit 

背景颜色| 
---|---
bg-black-90 bg-black-80 bg-black-70 bg-black-60 bg-black-50 <br/> bg-black-40 bg-black-30 bg-black-20 bg-black-10 bg-black-05|bg-black bg-near-black bg-dark-gray bg-mid-gray bg-gray bg-silver <br/> bg-light-silver bg-moon-gray bg-light-gray bg-near-white bg-white
bg-white-90 bg-white-80 bg-white-70 bg-white-60 bg-white-50 <br/> bg-white-40 bg-white-30 bg-white-20 bg-white-10 bg-white-05|bg-dark-red bg-red bg-light-red bg-orange bg-gold bg-yellow bg-light-yellow <br/>bg-purple bg-light-purple bg-dark-pink bg-hot-pink pink bg-light-pink bg-dark-green  <br/>bg-green bg-light-green bg-navy bg-dark-blue bg-blue bg-light-blue bg-lightest-blue <br/>bg-washed-blue bg-washed-green bg-washed-yellow bg-washed-red bg-color-inherit 

鼠标移入文字颜色|
---|---
文字颜色一栏查到class前面加上hover-即可|如black-90变成hover-black-90

鼠标移入背景颜色|
---|---
文字颜色一栏查到class前面加上hover-bg-即可|如black-90变成hover-bg-black-90，还要另外加上bg-animate的class

鼠标移动上变化|
---|---
dim| 透明度50%变淡
glow | 默认自己定义好，然后透明度变成1
hide-child child | 父元素 hide-child , 子元素child，子元素在鼠标移动上去才显示
underline-hover | 鼠标移动上去显示下划线
grow | 鼠标移动上去105%变大
grow-large | 鼠标移动上去 120%变大
pointer | 鼠标移动上去变成手
shadow-hover | 鼠标移动上去有阴影
bg-animate | 背景色加上动画渐变但不设置颜色

background-size |
---|---
cover| background-size: cover!important
contain | background-size: contain!important

borders |
---|---
ba | 1像素边框
bt | 1像素顶部边框
br | 1像素右侧边框
bb | 1像素底部边框
bl | 1像素左侧边框
bn | 没有边框
---|---
边框宽度 | 
bw0 | 边框无宽度
bw1 bw2 bw3 bw4 bw5 |  预定义1-5宽度
bt-0 br-0 bb-0 bl-0  | 上右下左边框无宽度重置
---|---
边框颜色 | 
b--颜色后缀 | 如要文字颜色为black-80的边框同样颜色，b--black-80
b--transparent | 边框透明色
b--inherit | 边框继承色
边框圆角 | 
br0 br1 br2 br3 br4 | 圆角1-4的角度
br-100 | 100%角度
br-pill | 9999px
br--bottom br--top br--right br--left | 某个地方有圆角

盒子阴影 |
--- | ---
shadow-1 shadow-2 shadow-3 shadow-4 shadow-5 | 盒子阴影1-5

透明度 |
--- | ---
o-100 o-90 o-80 o-70 o-60 o-50  o-40 <br/> o-30 o-20 o-10 o-05 o-025 o-0 | 透明度100% - 0%

## layout 布局方式
flex |
--- | ---
flex | display: flex;
inline-flex | display: inline-flex;
flex-auto  | 修复chrome44的错误
--- | ---
flex-column flex-row flex-column-reverse flex-row-reverse | 对于flex-direction的对应修饰
flex-wrap flex-nowrap flex-wrap-reverse | 对于flex-wrap的修饰
--- | ---
items-start items-end items-center items-baseline items-stretch | 对于align-items的修饰
--- | ---
self-start  self-end self-center self-baseline self-stretch | 对于align-self的修饰 
--- | ---
justify-start justify-end justify-center<br/>justify-between justify-around |  justify-contentd的修饰
--- | ---
content-start  content-end  content-center <br/> content-between content-around content-stretch | 对于align-content的修饰
--- | ---
order-0 order-1 order-2 order-3 order-4 order-5 <br/> order-6 order-7 order-8 order-last | order:0 到 order:99999 的修饰
--- | ---
flex-grow-0 flex-grow-1 | 对于flex-grow的修饰
flex-shrink-0  flex-shrink-1 | 对于flex-shrink的修饰

box-sizing|
--- | ---
border-box | box-sizing: border-box <br/>全部页面元素也都是borderbox

spacing |
--- | ---
pa0 pa1 pa2 pa3 pa4 pa5 pa6 pa7 | padding all 四个方向的padding 
pl0 pl1 pl2 pl3 pl4 pl5 pl6 pl7 | padding-left 7种程度
pr0 pr1 pr2 pr3 pr4 pr5 pr6 pr7 | padding-right 
pb0 pb1 pb2 pb3 pb4 pb5 pb6 pb7 | padding-bottom 
pt0 pt1 pt2 pt3 pt4 pt5 pt6 pt7 | padding-top
pv0 pv1 pv2 pv3 pv4 pv5 pv6 pv7 | vertical 垂直方向包含上下
ph0 ph1 ph2 ph3 ph4 ph5 ph6 ph7 | 水平方向包含左右
--- | ---
ma0 ma1 ma2 ma3 ma4 ma5 ma6 ma7 | margin all 四个方向的madding 
ml0 ml1 ml2 ml3 ml4 ml5 ml6 ml7 | margin-left 7种程度
mr0 mr1 mr2 mr3 mr4 mr5 mr6 mr7 | margin-right 
mb0 mb1 mb2 mb3 mb4 mb5 mb6 mb7 | margin-bottom 
mt0 mt1 mt2 mt3 mt4 mt5 mt6 mt7 | margin-top
mv0 mv1 mv2 mv3 mv4 mv5 mv6 mv7 | vertical 垂直方向包含上下
mh0 mh1 mh2 mh3 mh4 mh5 mh6 mh7 | 水平方向包含左右

浮动和清除浮动 |
--- | ---
fl  fl  fn| 左浮动 ;右浮动;没有浮动none
cf | 清除浮动
cl cr cb bn | 清除左浮动、右浮动、两侧浮动、不清除浮动

display |
--- | ---
dn |  display:none
di |  inline
db  |  block
dib  | inline-block
dit  |   inline-table
dt   |  table
dtc   |  table-cell
dt-row |  table-row
dt-row-group | table-row-group
dt-column   |   table-column
dt-column-group | table-column-group;
dt--fixed | table-layout: fixed;width: 100%;<br/>图表最大宽度，所有列等宽

宽度 | 
--- | ---
w1 w2 w3 w4 w5 | 宽度为物种
w-10 w-20 w-25 w-30 <br/>w-33 w-34 w-40 w-50 <br/>w-60 w-70 w-75 w-80 <br/>w-90 w-100 | 百分比宽度 
w-third  w-two-thirds | 1/3、1/1.5 宽度
w-auto | 自动 
mw-100 | 最大宽度100%
mw1 mw2 mw3 mw4 mw5 <br/> mw6 mw7 mw8 mw9 | 最大宽度9种程度
mw-none | 最大宽度none

高度 |
--- | ---
h1 h2 h3 h4 h5 | 5种高度
h-25 h-50 h-75 h-100 | 高度百分比
min-h-100 | min-height: 100%
h-auto |  height: auto
h-inherit | height: inherit
vh-25 vh-50 vh-75 vh-100 |height:  25vh 以此类推
min-vh-100 | min-height: 100vh

位置 |
--- | ---
static relative absolute fixed | positon为对应的左侧值

## 文本
type-scale 字号 |
--- | ---
f1 f2 f3 f4 f5 f6 f7 | 为对应字号
f-6 f-headline, f-5 f-subheadline | 前两个一样大 后两个一样大

typography 字号 |
--- | ---
measure  measure-wide  measure-narrow | 文字宽度中大小
indent | text-indent缩进1em
small-caps | small-caps
truncate | 超出显示点点点，配合宽度使用

line-height |
--- | ---
lh-solid lh-title lh-copy  |  三种行高

letter-spacing |
--- | ---
tracked tracked-tight tracked-mega | 字间距1 窄 2

letter-spacing |
--- | ---
normal b | 正常 加粗
fw1 fw2 fw3 fw4 fw5 <br/> fw6 fw7 fw8 fw9 | 粗100-900

font-style |
--- | ---
i fs-normal | italic normal

vertical-align |
--- | ---
v-base v-mid v-top v-btm | baseline middle top bottom

text-align |
--- | ---
tl tr tc tj  | left right center justify 

text-transform |
--- | ---
ttc ttl ttu ttn | capitalize lowercase uppercase none

text-decoration |
-- | --
strike underline no-underline | line-throuth underline none

white-space |
-- | --
ws-normal  nowrap pre | normal nowrap pre

font-family |
-- | --
sans-serif serif system-sans-serif system-serif | 都不认识
.code times | 不认识
