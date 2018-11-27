---
title: 基本功能和用法
weight: 10
disableToc: true
---

## 基本用法

- 下载上hugo的安装包，把hugo放到path路径下，能够直接运行hugo
- 初始化网站
```
hugo new site <xgwx>
```
- 把主题解压到xgwx/theme路径下
- 修改config.toml 文件
```
theme = "hugo-theme-name"
```
- 启动服务器
```
hugo server
```
- 建立静态页
```
hugo
```

## 新建页面

章节页面新建 
```
hugo new --kind chapter basics/_index.md
```
普通页面新建
```
hugo new basics/second-content/_index.md
```

## 设置文件
```toml
[params]
  # Prefix URL to edit current page. Will display an "Edit this page" button on top right hand corner of every page. 
  # Useful to give opportunity to people to create merge request for your doc.
  # See the config.toml file from this documentation site to have an example.
  editURL = ""
  # Author of the site, will be used in meta information
  author = ""
  # Description of the site, will be used in meta information
  description = ""
  # Shows a checkmark for visited pages on the menu
  showVisitedLinks = false
  # Disable search function. It will hide search bar
  disableSearch = false
  # Javascript and CSS cache are automatically busted when new version of site is generated. 
  # Set this to true to disable this behavior (some proxies don't handle well this optimization)
  disableAssetsBusting = false
  # Set this to true to disable copy-to-clipboard button for inline code.
  disableInlineCopyToClipBoard = false
  # A title for shortcuts in menu is set by default. Set this to true to disable it. 
  disableShortcutsTitle = false
  # When using mulitlingual website, disable the switch language button.
  disableLanguageSwitchingButton = false
  # Hide breadcrumbs in the header and only show the current page title
  disableBreadcrumb = true
  # Hide Next and Previous page buttons normally displayed full height beside content
  disableNextPrev = true
  # Order sections in menu by "weight" or "title". Default to "weight"
  ordersectionsby = "weight"
  # Change default color scheme with a variant one. Can be "red", "blue", "green".
  themeVariant = ""
```
开启搜索
```toml
[outputs]
home = [ "HTML", "RSS", "JSON"]
```

## 修改样式

themes/hugo-theme-learn/layouts/partials/ 的文件通过hugo网站目录 layouts/partials 直接覆盖

## 文章头部
```toml
+++
# Table of content (toc) is enabled by default. Set this parameter to true to disable it.
# Note: Toc is always disabled for chapter pages
disableToc = "false"
# If set, this will be used for the page's menu entry (instead of the `title` attribute)
menuTitle = ""
# The title of the page in menu will be prefixed by this HTML content
pre = ""
# The title of the page in menu will be postfixed by this HTML content
post = ""
# Set the page as a chapter, changing the way it's displayed
chapter = false
# Hide a menu entry by setting this to true
hidden = false
# Display name of this page modifier. If set, it will be displayed in the footer.
LastModifierDisplayName = ""
# Email of this page modifier. If set with LastModifierDisplayName, it will be displayed in the footer
LastModifierEmail = ""
+++
```

增加小图标
```toml
+++
title = "Github repo"
pre = "<i class='fab fa-github'></i> "
+++
```

排序
```toml
+++
title = "My page"
weight = 5
menuTitle = "Linux"  这个是在菜单显示的不同名称
+++
```

## 首页自定义
- content 下面新建_index.md
- 新建index.html，在static 文件夹

## 在markdown中使用小图标
```
Built with <i class="fas fa-heart"></i> from Grav and Hugo
```


## 显示一些markdown里的弹窗
{{% notice note %}}
A notice disclaimer
{{% /notice %}}
note换成info是橙黄色 tip绿色 Warning 红色

## 可以展开的内容
{{%expand "Is this learn theme rocks ?" %}}Yes !.{{% /expand%}}

## 一个按钮
{{% button href="https://getgrav.org/" icon="fas fa-download" %}}Get Grav with icon{{% /button %}}

附件 子页面，多国语言详见文档