# 文本样式

### font-size  
font-size：<length> | <percentage> | <absolute-size> | <relative-size>  

```
<style type="text/css">
p{margin:10px;background:#ddd;}
p+p{margin-left:40px;}

.m-demo{font-size:12px;}
.m-demo .p1{font-size:16px;}
.m-demo .p2{font-size:2em;}
.m-demo .p3{font-size:200%;}
</style>

<div class="m-demo">
	<p>文字大小：font-size:12px;</p>
	<p class="p1">文字大小：font-size:16px;</p>
	<p class="p2">文字大小：font-size:2em;</p>
	<p class="p3">文字大小：font-size:200%;</p>
</div>
```

![](/css/images/font-size.png)

### font-family  
font-family：[<family-name> | <generic-family>]#  
<generic-family> = serif | sans-serif | cursive | fantasy | monospace  

```
<style type="text/css">
p{margin:10px;background:#ddd;}
p+p{margin-left:40px;}

.m-demo{font-family:arial;}
.m-demo .p1{font-family:arial, Verdana, sans-serif;}
.m-demo .p2{font-family:Verdana, "microsoft yahei";}
.m-demo .p3{font-family:"宋体", serif;}
</style>


<div class="m-demo">
	<p>字体系列：font-family:arial;</p>
	<p class="p1">字体系列：font-family:arial, Verdana, sans-serif;</p>
	<p class="p2">字体系列：font-family:Verdana, "microsoft yahei";</p>
	<p class="p3">字体系列：font-family:"宋体", serif;</p>
</div>
```

![](/css/images/font-family-ex.png)

### font-weight  
font-weight:normal | bold | bolder | lighter |100|200|300|400|500|600|700|800|900  

![](/css/images/font-weight.png)

### font-style  
font-style:nomal | italic | oblique  

![](/css/images/font-style.png)  

### line-height  
line-height:nomal | <number> | <lenght> | <percentage>  

```
<style type="text/css">
p{margin:10px;background:#ddd;}
p+p{margin-left:40px;}

body{font-size:30px;}

.m-demo{line-height:40px;}
.m-demo p{background:#ddd;}
.m-demo .p1{line-height:3em;}
.m-demo .p2{line-height:300%;}
.m-demo .p3{line-height:3;}

.m-demo2{line-height:300%;}
.m-demo2 p{background:#fbb;}
.m-demo2 .p1{font-size:16px;}

.m-demo3{line-height:3;}
.m-demo3 p{background:#0dd;}
.m-demo3 .p1{font-size:16px;}
</style>

<div class="m-demo">
	<p>行高：line-height:40px;</p>
	<p class="p1">行高：line-height:3em;</p>
	<p class="p2">行高：line-height:300%;</p>
	<p class="p3">行高：line-height:3;</p>
</div>


<div class="m-demo2">
	<p>行高：line-height:300%(百分比为先计算再继承，即300%*30px = 90px再继承90px行高);</p>
	<p class="p1">字体大小：font-size:16px;先计算再继承：300%*30px = 90px(此处30px为继承body的font-size的值)，先计算出了90px这个结果值，再继承这个值</p>
</div>
<div class="m-demo3">
	<p>行高：line-height:3（Number为先继承再计算，即先把3倍行高继承下来，在乘以字体大小）;</p>
	<p class="p1">字体大小：font-size:16px;先继承再计算：先继承了行高的值：3，再计算结果3*16px = 48px</p>
</div>
```

![](/css/images/line-height.png)  

### font   
font：[ [ <' font-style '> || <' font-variant '> || <' font-weight '> ]? <' font-size '> [ / <' line-height '> ]? <' font-family '> ] | caption | icon | menu | message-box | small-caption | status-bar

```
<style type="text/css">
p{margin:10px;background:#ddd;}
p+p{margin-left:40px;}

.m-demo{font:30px/2 "Consolas",monospace;}
.m-demo .p1{font:italic bold 20px/1.5 arial,serif;}
.m-demo .p2{font:20px arial,serif;}
.m-demo .p3{font:100px;}
.m-demo .p4{font:'microsoft yahei';}
</style>


<div class="m-demo">
	<p>缩写：font:30px/2 "Consolas",monospace;</p>
	<p class="p1">缩写：font:italic bold 20px/1.5 arial,serif;</p>
	<p class="p2">缩写：font:20px arial,serif;</p>
	<p class="p3">缩写：font:100px;</p>
	<p class="p4">缩写：font:'microsoft yahei';</p>
</div>
```
![](/css/images/font.png)

### color   
![](/css/images/color.png)

### text-decoration  
text-decoration:none | [underline || overline || line-through]

```
<style type="text/css">
p{margin:10px;background:#ddd;}

.m-demo .p1{text-decoration:underline;}
.m-demo .p2{text-decoration:underline overline;}
.m-demo .p3{text-decoration:line-through;}
</style>


<div class="m-demo">
	<p class="p1">text-decoration:underline;</p>
	<p class="p2">text-decoration:underline overline;</p>
	<p class="p3">text-decoration:line-through;</p>
</div>
```

![](/css/images/text-decoration-ex.png)

### text-align  
text-align:left | right | center | justify  

```
<style type="text/css">
p{margin:10px;background:#ddd;word-break:break-all;}
p+p{margin-left:40px;}

.m-demo{text-align:left;}
.m-demo .p1{text-align:right;}
.m-demo .p2{text-align:center;}
.m-demo .p3{text-align:justify;}
</style>


<div class="m-demo">
	<p>文本对齐：text-align: left;</p>
	<p class="p1">文本对齐：text-align: right;</p>
	<p class="p2">文本对齐：text-align: center;</p>
	<p class="p3">文本对齐：text-align: justify;文本对齐文本对齐</p>
</div>
```
![](/css/images/text-align.png)

### vertical-align  
vertical-align：baseline | sub | super | top | text-top | middle | bottom | text-bottom | <percentage> | <length>  
```
<style type="text/css">
p{margin:10px;background:#ddd;font-size:30px;line-height:200%;}
.m-demo .p1{font-size:50px;}
.m-demo span.va{font-size:20px;}
.m-demo .va-1{vertical-align:middle;}
.m-demo .va-2{vertical-align:20px;}
.m-demo .va-3{vertical-align:sub;}
.m-demo .va-4{vertical-align:super;}
</style>


<div class="m-demo">
	<p class="p1">文字<img src="icon.png" class="va"><span>文字</span><img src="icon.png" class="va va-1">文字</p>
	<p>普通文字<span class="va">普通</span><span>普通文字</span><span class="va va-2">对齐20px</span>普通文字</p>
	<p>普通文字<span class="va">普通</span><span>普通文字</span><span class="va va-3">对齐sub</span>普通文字</p>
	<p>普通文字<span class="va">普通</span><span>普通文字</span><span class="va va-4">对齐super</span>普通文字</p>
</div>
```

![](/css/images/vertical-align.png)  


### text-indent  
text-indent:<length> | <percentage>  

```
<style type="text/css">
p{margin:10px;background:#ddd;}

.m-demo .p1{text-indent:2em;}
.m-demo .p2{text-indent:10px;}
.m-demo .p3{text-indent:20%;}
.m-demo .p4{text-indent:-2em;}
.m-demo .p5{text-indent:-9999px;}
</style>

<div class="m-demo">
	<p class="p1">首行缩进：text-indent:2em;首行缩进首行缩进首行缩进首行缩进</p>
	<p class="p2">首行缩进：text-indent:10px;首行缩进首行缩进首行缩进首行缩进</p>
	<p class="p3">首行缩进：text-indent:20%;首行缩进首行缩进首行缩进首行缩进</p>
	<p class="p4">首行缩进：text-indent:-2em;首行缩进首行缩进首行缩进首行缩进</p>
	<p class="p5">首行缩进：text-indent:-9999px;首行缩进首行缩进首行缩进首行缩进</p>
</div>
```
![](/css/images/text-indent.png)


### white-space  
white-space：normal | pre | nowrap | pre | pre-wrap | pre-line  
![](/css/images/white-space.png)

```
<style type="text/css">
p{margin:10px;background:#ddd;}

.m-demo .p1{white-space:normal;}
.m-demo .p2{white-space:pre;}
.m-demo .p3{white-space:pre-wrap;}
.m-demo .p4{white-space:pre-line;}
.m-demo .p5{white-space:nowrap;}
.m-demo .p6{white-space:pre-wrap;}
</style>


<div class="m-demo">
	<p class="p1">white-space:normal; 左边1个空格  左边2个空格   左边3个空格
左边一个换行
	左边一个换行加一个Tab</p>
	<p class="p2">white-space:pre; 左边1个空格  左边2个空格   左边3个空格
左边一个换行
	左边一个换行加一个Tab</p>
	<p class="p3">white-space:pre-wrap; 左边1个空格  左边2个空格   左边3个空格
左边一个换行
	左边一个换行加一个Tab</p>
	<p class="p4">white-space:pre-line; 左边1个空格  左边2个空格   左边3个空格
左边一个换行
	左边一个换行加一个Tab</p>
	<p class="p5">white-space:nowrap; 左边1个空格  左边2个空格   左边3个空格
左边一个换行
	左边一个换行加一个Tab</p>

	<p class="p6">
	.m-demo .p6{
	    text-indent: 2em;
	}
	</p>
</div>
```
![](/css/images/white-space-ex.png)


### word-wrap  
word-wrap:normal | break-word  

```
<style type="text/css">
p{margin:10px;padding:0 10px;background:#ddd;}

.m-demo .p1{word-wrap:normal;}
.m-demo .p2{word-wrap:break-word;}
</style>

<div class="m-demo">
	<p class="p1">Hello World Hello World Hello World Hello World
	xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
	Hello World Hello World Hello World Hello World
	</p>
	<p class="p2">Hello World Hello World Hello World Hello World
	xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
	Hello World Hello World Hello World Hello World
	</p>
</div>
```

![](/css/images/word-wrap.png)

### word-break  
word-break:normal | keep-all | break-all  

```
<style type="text/css">
p{margin:10px;padding:0 10px;background:#ddd;}

.m-demo .p1{word-wrap:break-word;}
.m-demo .p2{word-break:break-all;}
</style>


<div class="m-demo">
	<p class="p1">Hello World Hello World Hello World Hello World
	xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
	Hello World Hello World Hello World Hello World
	</p>
	<p class="p2">word-break: break-all; Hello World Hello World
	xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
	Hello World Hello World Hello World Hello World
	</p>
</div>
```
![](/css/images/word-break.png)  


### text-shadow  
`text-shadow：none | <shadow> [ , <shadow> ]*  `  
`<shadow> = <length>{2,3} && <color>? `  

```
<style type="text/css">
p{margin:10px;background:#ddd;}

.m-demo{color:#000;}
.m-demo .p1{text-shadow:1px 2px #f00;}
.m-demo .p2{text-shadow:1px 2px 3px #f00;}
.m-demo .p3{text-shadow:1px 2px 3px;}
.m-demo .p4{text-shadow:1px 2px rgba(255,0,0,0.5);}
.m-demo .p5{text-shadow:1px 2px #f00, 1px 2px 3px;}
</style>

<div class="m-demo">
	<p class="p1">文字阴影：text-shadow:1px 2px #f00;</p>
	<p class="p2">文字阴影：text-shadow:1px 2px 3px #f00;</p>
	<p class="p3">文字阴影：text-shadow:1px 2px 3px;</p>
	<p class="p4">文字阴影：text-shadow:1px 2px rgba(255,0,0,0.5);</p>
	<p class="p5">文字阴影：text-shadow:1px 2px #f00, 1px 2px 3px;</p>
</div>
```
![](/css/images/text-shadow.png)  

### text-overflow  
text-overflow:clip | ellipsis  

```
<style type="text/css">
p{margin:10px;background:#ddd;}
.m-demo p{height:60px;line-height:60px;overflow:hidden;}
.m-demo .p1{text-overflow:ellipsis;}
.m-demo .p2{text-overflow:ellipsis;white-space:nowrap;}
</style>


<div class="m-demo">
	<p class="p1">文本溢出：text-overflow:ellipsis;文本溢出文本溢出文本溢出文本溢出文本溢出文本溢出文本溢出</p>
	<p class="p2">文本溢出：text-overflow:ellipsis;文本溢出文本溢出文本溢出文本溢出文本溢出文本溢出文本溢出</p>
</div>
```

![](/css/images/text-overflow.png)


### cursor
```
cursor：[<url> [<x> <y>]?,]*[ auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | zoom-in | zoom-out | grab | grabbing]
```

```
<style type="text/css">
p{margin:10px;background:#ddd;}

.m-demo .p1{cursor:auto;}
.m-demo .p2{cursor:default;}
.m-demo .p3{cursor:pointer;}
.m-demo .p4{cursor:help;}
.m-demo .p5{cursor:move;}
.m-demo .p6{cursor:none;}
.m-demo .p7{cursor:url(cur.cur),pointer;}
</style>

<div class="m-demo">
	<p class="p1">指针：cursor:auto;</p>
	<p class="p2">指针：cursor:default;</p>
	<p class="p3">指针：cursor:pointer;</p>
	<p class="p4">指针：cursor:help;</p>
	<p class="p5">指针：cursor:move;</p>
	<p class="p6">指针：cursor:none;</p>
	<p class="p7">指针：cursor:url(cur.cur),pointer;</p>
</div>
```
cur.cur文件
```
0000 0200 0100 2020 0000 0000 0000 a810
0000 1600 0000 2800 0000 2000 0000 4000
0000 0100 2000 0000 0000 8010 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0001 0000
0002 0000 0004 0000 0006 0000 0007 0000
0007 0000 0007 0000 0007 0000 0007 0000
0007 0000 0007 0000 0007 0000 0006 0000
0004 0000 0002 0000 0001 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0001 0000 0004 0000
000a 0000 000f 0000 0013 0000 0015 0000
0016 0000 0016 0000 0016 0000 0016 0000
0016 0000 0016 0000 0015 0000 0013 0000
000f 0000 000a 0000 0004 0000 0001 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0001 0000 0004 0000 000c 0000
0017 0000 0021 0000 0028 0000 002b 0000
002c 0000 002c 0000 002c 0000 002c 0000
002c 0000 002c 0000 002b 0000 0028 0000
0021 0000 0017 0000 000c 0000 0004 0000
0001 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0002 0000 000a 0000 0017 4f5c
2347 849a 3abd 8ea6 3ff5 90a8 40ff 90a8
40ff 90a8 40ff 90a8 40ff 90a8 40ff 90a8
40ff 90a8 40ff 90a8 40ff 8ea6 3ff5 849a
3abd 4f5c 2347 0000 0017 0000 000a 0000
0002 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0004 0000 000f 5563 2644 8ea6
3ff2 9db7 46ff a6c2 49ff a7c3 4aff a7c3
4aff a7c3 4aff a7c3 4aff a7c3 4aff a7c3
4aff a7c3 4aff a7c3 4aff a6c2 49ff 9db7
46ff 8ea6 3ff2 5563 2644 0000 000f 0000
0004 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0006 0000 0013 869c 3bba 9db7
46ff a7c3 4aff a7c3 4aff a7c3 4aff a7c3
4aff a7c3 4aff a7c3 4aff a7c3 4aff a7c3
4aff a7c3 4aff a7c3 4aff a7c3 4aff a7c3
4aff 9db7 46ff 869c 3bba 0000 0013 0000
0006 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0007 0000 0015 8fa7 3ff3 a7c2
4aff a8c4 4bff a8c4 4bff a8c4 4bff a8c4
4bff a8c4 4bff a8c4 4bff a8c4 4bff a8c4
4bff a8c4 4bff a8c4 4bff a8c4 4bff a8c4
4bff a7c3 4aff 8fa7 3ff5 0000 0015 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0007 0000 0016 90a8 40ff a9c5
4bff a9c5 4bff a9c5 4bff a9c5 4bff a9c5
4bff a9c5 4bff a9c5 4bff a9c5 4bff a9c5
4bff a9c5 4bff a9c5 4bff a9c5 4bff a9c5
4bff a9c5 4bff 90a8 40ff 0000 0016 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0007 0000 0016 90a8 40ff a9c6
4bff a0bb 47ff 96af 43ff 96af 43ff a0bb
47ff a0bb 47ff 96af 43ff 96af 43ff a0bb
47ff a0bb 47ff 96af 43ff 96af 43ff a0bb
47ff a9c6 4bff 90a8 40ff 0000 0016 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0007 0000 0016 90a8 40ff aac7
4cff 96af 43ff e5eb d2ff e5eb d3ff 96af
43ff 96af 43ff e5eb d2ff e5eb d3ff 96af
43ff 96af 43ff e5eb d2ff e5eb d3ff 96af
43ff aac7 4cff 90a8 40ff 0000 0016 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0007 0000 0016 90a8 40ff abc8
4cff 96b0 43ff e5eb d2ff e5eb d2ff 96b0
43ff 96b0 43ff e5eb d2ff e5eb d2ff 96b0
43ff 96b0 43ff e5eb d2ff e5eb d2ff 96b0
43ff abc8 4cff 90a8 40ff 0000 0016 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0008 0000 0016 90a8 40ff acc9
4cff a2bd 48ff 97b0 43ff 97b0 43ff a2bd
48ff a2bd 48ff 97b0 43ff 97b0 43ff a2bd
48ff a2bd 48ff 97b0 43ff 97b0 43ff a2bd
48ff acc9 4cff 90a8 40ff 0000 0015 0000
0007 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0001 0000 0009 0000 0018 90a8 40ff acca
4dff acca 4dff acca 4dff acca 4dff acca
4dff acca 4dff acca 4dff acca 4dff acca
4dff acca 4dff acca 4dff acca 4dff acca
4dff acca 4dff 90a8 40ff 0000 0013 0000
0006 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0002 0000 000b 0000 001a 90a8 40ff adca
4dff adca 4dff adca 4dff adca 4dff adca
4dff adca 4dff adca 4dff adca 4dff adca
4dff adca 4dff adca 4dff adca 4dff adca
4dff acc8 4dff 8fa7 3ff5 0000 000f 0000
0004 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0004 0000 000c 4550 1f2c 93ab 42ff b2ce
57ff b0cc 51ff aecb 4eff aecb 4dff aecb
4dff aecb 4dff aecb 4dff aecb 4dff aecb
4dff aecb 4dff aecb 4dff aecb 4eff b0cc
51ff a4bd 4dff 8aa1 3db4 0000 000a 0000
0002 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0004 0000 000b 879d 3c8e 9fb8 4bff 97b0
45ff a6c0 50ff b2ce 59ff b4d0 5aff b4d0
5aff b4d0 5aff b4d0 5aff b4d0 5aff b4d0
5aff b4d0 5aff b4d0 5aff b2ce 59ff a4be
4eff 8fa7 40f0 7386 3331 0000 0004 0000
0001 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0003 89a0 3d57 8ea5 3fb0 879d 3c6f 768a
343d 8ca3 3eb2 8fa7 40f2 90a8 40ff 90a8
40ff 90a8 40ff 90a8 40ff 90a8 40ff 90a8
40ff 90a8 40ff 90a8 40ff 8fa7 40f2 8ca3
3eb2 778a 352d 0000 0004 0000 0001 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0001 0000 0002 0000 0003 0000 0003 0000
0004 0000 0005 0000 0006 0000 0007 0000
0007 0000 0007 0000 0007 0000 0007 0000
0007 0000 0007 0000 0007 0000 0006 0000
0004 0000 0002 0000 0001 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 0000
0000 0000 0000 0000 0000 0000 0000 ffff
ffff ffff ffff ffff ffff ffff ffff ffff
ffff ffff ffff ffff ffff ffff ffff ffff
ffff ffff ffff ffff ffff ffff ffff ffff
ffff ffff ffff e000 1fff c000 0fff 8000
07ff 8000 07ff 8000 07ff 8000 07ff 8000
07ff 8000 07ff 8000 07ff 8000 07ff 8000
07ff 8000 07ff 0000 07ff 0000 07ff 0000
07ff 0000 07ff 0000 0fff 0000 1fff
```

![](/css/images/cursor.png)

### inherit  
![](/css/images/inherit-ex.png)  

```
<style type="text/css">
p{margin:10px;background:#ddd;}
p+p{margin-left:40px;}

.m-demo{font-family:"Consolas";color:black;}
.m-demo .p1{font-family:"microsoft yahei";color:red;}
.m-demo .p1-1{font-family:inherit;color:inherit;}
</style>

<div class="m-demo">
	<p>字体系列：font-family:"Consolas";</p>
	<p class="p1">字体系列：font-family:"microsoft yahei";</p>
	<p class="p1 p1-1">字体系列：font-family:inherit;</p>
</div>
```
![](/css/images/inherit2.png)  


### 练习  
```
<style type="text/css">
body{margin: 0;}
.m-demo{
	width:100%;/* ie6/7 */
	color:#000;
	background:#ddd;
	text-shadow:1px 1px #000;
	font:20px/3 arial "microsoft yahei";
	overflow:hidden;
	white-space:nowrap;
	text-overflow:ellipsis;
	text-indent:2em;
}
.m-demo em{font-weight:bold;}
.m-demo sup{vertical-align:super;font-size:12px;}
.m-demo del{text-decoration:line-through;}
</style>

<div class="m-demo">
方程：<em>x<sup>2</sup>+y<sup>2</sup>=128</em>，求x、y的值，请写出解题过程<del>请写出解题过程</del>
</div>
```
![](/css/images/practice.png)  
