## 针对 Insta360 优化的 Typo.css

目标：一致化浏览器排版效果，构建最适合中文阅读的网页排版。包括桌面和移动平台。

预览：[typo.css][1]

### 一、目录结构  
    .
	├── README.md           --- 使用帮助
	├── license.txt         --- 许可证
	├── less                --- 将应用于你的项目
	├───── typo.less        --- 排版核心文件
	├───── colors.less      --- Insta360 品牌颜色库
	├───── style.less       --- 用于支持预览页面
	├── js
	├───── less.min.js      --- less
	└── index.html          --- Demo/预览


### 二、Typo.less 使用指南  

####1. 一般 reset.css 所需的内容  
 
将元素默认样式清零重设。  
  
  
####2. 正文排版设置  

在承载大段可阅读文章的容器上，添加 `.typo` 这个 class，让你的排版像 [http://typo.sofi.sh][2] 一样，让用户阅读起来更舒服。  
  
  
####3. Web UI 字体设置 （待做）   
  

####4. 辅助类：   
主要是一些需要中文日常排版需要的元素和语文对应样式的增强，目前包括:  
1. 强制换行：添加 `.textwrap` 到文本所在的容器，如果是 `table` 测还需要 `.textwrap-table` 
2. 衬线字体：添加 `.serif`  
  

### 三、针对 Typo.css 做出的调整

1. 用 less 改写 Typo.css
2. 去除 `class="typo-标签"`、`.clearfix`、`.borderbox`的用法
3. 重新设计了 `<p>`、`<h1>-<h6>` 的字号、行距、字重、间距
4. 借鉴 [font.css][3] 重设了衬线和非衬线字体，引入 Roboto 字体
5. 依照 Insta360 品牌配色重设了链接、高亮、引用、`::selection`等的颜色
6. 让文字适配 4pt 栅格（待完善）
7. 优化了 `<ul>`、`<ol>`、`<blockquote>` 嵌套进其他元素时的样式
8. 设置了 `<img>` 标签在文中的间距

### 四、开源许可
基于 [MIT License][4] 开源，使用代码只需说明来源，或者引用 [license.txt][5] 即可。

[1]:	https://arashivision.github.io/typo.less
[2]:	https://arashivision.github.io/typo.less
[3]:	https://github.com/zenozeng/fonts.css "Font.css"
[4]:	http://zh.wikipedia.org/wiki/MIT_License
[5]:	https://github.com/sofish/typo.css/blob/master/license.txt
