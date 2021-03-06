# vnote-solarized-theme
适用于 VNote 3 的 solarized 主题

# 截图
Solarized-dark
![Solarized-dark](./solarized-dark/cover.png)

Solarized-light
![Solarized-light](./solarized-light/cover.png)

# 安装方法
把文件夹放到vnote的主题文件夹里, 比如linux是 `~/.local/share/VNote/VNote/themes/`.
如果不清楚路径，可以在VNote设置内找到`外观-主题`, 选中任意主题，点击`打开路径`就会打开相关的文件夹了.

# 自定义主题
改下颜色
这个网站有[渐变色](https://atool.vip/color/)生成

修改 `~/.local/share/VNote/VNote/themes/solarized-dark/palette.json`

# 注意几个主要的颜色
bg1_5 是主界面的底色 （bg1_1到bg1_5渐变 bg1_51到fg1_10渐变）  
bg10_5 左侧文件树的背景色 搜索结果的背景色 选项的背景色 选中按钮的背景色  
bg2_5 是鼠标悬停在左侧笔记树的弹窗背景色 (bg2_2到bg2_9渐变)  

web.css  
body的background-color 是查看模式下笔记的背景色  
::-webkit-scrollbar的background-color 是查看模式下滚动条背景  
还有 ::-webkit-scrollbar-corner的background-color 和 ::-webkit-scrollbar-button 的 background-color 也是一样的  
::-webkit-scrollbar-track的background-color 是查看模式下右侧滚动条的背景  
"editor-styles" 的 "IndicatorsBorder" 是编辑器行号的背景色  
最好取编辑器背的背景色kit-scrollbar-button的background-color 是查看模式下滚动条上下按钮的颜色，注意普通状态，鼠标悬浮，鼠标点击等状态的颜色也要修改  
::-webkit-scrollbar-thumb的background-color 是查看模式下鼠标和滚动条交互的颜色  
table tr的background-color 是查看模式下表格的颜色，注意hover状态的颜色也要修改  

text-editor.theme  
"editor-styles" 的 "background-color"  
"markdown-editor-styles" 的 "background-color"  
这两个是编辑器的背景色  

"editor-styles" 的 "IndicatorsBorder" 是编辑器行号的背景色  
最好取编辑器背的背景色和左侧文件树的背景色中间的颜色  

"editor-styles" 的 "CursorLine" 是编辑模式下当前行的背景

## 其它颜色和对应界面

### bg1_51
悬浮框title的背景颜色，可以稍微做的有辨识度一点，让边界分明

### bg1_8
开启，关闭原地预览按钮的背景

### bg2_5
查找框，关键字高亮背景  
悬浮框文字背景

### fg1_5
左上菜单，设置文字，设置选项的文字颜色

### fg1_8
左侧文件树，下方搜索结果，上方当前选中的笔记标题文字颜色  
设置菜单内文件树和部分设置的文字颜色

### fg1_9
左侧菜单鼠标悬浮框文字颜色  
菜单按钮鼠标悬浮上去后的文字颜色

## solarized-dark 转 light
073642 替换成 FDF6E3  
需要注意的是dark主题渐变色由深到浅  
light应该是由浅到深  

文字主要颜色  
ccd1d8 改成 657B83  
文字选中背景  
0c7bff 改成 EEE8D5  

其它的对应修改就行

# 文字颜色
大体界面UI的颜色调好之后，可以修改一下文字的颜色了
以下基于vnote月夜主题的文字颜色修改
由于颜色用的地方很多，这里不一一列出来了，只记录颜色替换结果

## 深色主题

### 查看模式的颜色 text-editor.theme
标题 红色 `#e06c75` 改成黄色 `#CA4A17`  
链接 蓝色 `#61afef` 改绿色 `#2AA198`  
代码颜色 绿色 `#98c379` 改成黄色 `#D7BA7D`  

### 编辑模式的颜色 web.css
标题 红色 `#e06c75` 改成黄色 `#CA4A17`  
链接 蓝色 `#61afef` 改绿色 `#2AA198`  
代码颜色 绿色 `#98c379` 改成黄色 `#D7BA7D`  


## 浅色主题

### 查看模式的颜色 text-editor.theme
标题 红色 `#e06c75` 改成黄色 `#CA4A17`  
链接 蓝色 `#61afef` 改绿色 `#2AA198`  
代码颜色 绿色 `#98c379` 改成黄色 `#D7BA7D`  

### 编辑模式的颜色 web.css
标题 红色 `#e06c75` 改成土黄色 `#CA8465`  
链接 蓝色 `#61afef` 改绿色 `#2AA198`  
代码颜色 绿色 `#98c379` 改成黄色 `#D7BA7D`  

浅色主题需要额外修改  
表格分隔符`|`的背景色 `#444b58` 改成 和主背景相近的颜色 `#E4DECC`  
选中文字的背景色 "selected-background-color" 注意有2个 都换成 `#b0bec5`  

# 代码高亮

## 编辑模式代码高亮
修改palette.json  
代码高亮主题 "editor-highlight-theme" 和 "markdown-editor-highlight-theme" 改成 Light 或 dark 主题  

## 查看模式代码高亮
修改highlight.css  
可以直接去 https://prismjs.com/download.html 生成  

里面有现成的 solarized-light 主题的高亮，也可以用到 solarized-dark主题上，注意修改这个背景色  
```
:not(pre) > code[class*="language-"],
pre[class*="language-"] {
    background-color: #073642; /* base3 */
}
```

# 声明
本主题由VNote3的内置主题`月夜`修改而来.
