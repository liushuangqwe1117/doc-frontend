# 布局
> 布局是将元素以正确的大小摆放在正确的位置上。CSS页面布局允许我们拾取网页中的元素，并且控制它们先对正常布局流、周边元素、父容器或主视窗口的位置


### display  
指定用于元素的呈现框的类型。display属性值取决于HTML规范所描述的行为或浏览器默认样式  
语法：  
```
display：none | inline | block | list-item | inline-block | table | inline-table | table-caption | table-cell | table-row | table-row-group | table-column | table-column-group | table-footer-group | table-header-group | run-in | box | inline-box | flexbox | inline-flexbox | flex | inline-flex
```
取值：   
```
none：隐藏对象。与visibility属性的hidden值不同，其不为被隐藏的对象保留其物理空间
inline：指定对象为内联元素。
block：指定对象为块元素。
list-item：指定对象为列表项目。
inline-block：指定对象为内联块元素。（CSS2）
table：指定对象作为块元素级的表格。类同于html标签<table>（CSS2）
inline-table：指定对象作为内联元素级的表格。类同于html标签<table>（CSS2）
table-caption：指定对象作为表格标题。类同于html标签<caption>（CSS2）
table-cell：指定对象作为表格单元格。类同于html标签<td>（CSS2）
table-row：指定对象作为表格行。类同于html标签<tr>（CSS2）
table-row-group：指定对象作为表格行组。类同于html标签<tbody>（CSS2）
table-column：指定对象作为表格列。类同于html标签<col>（CSS2）
table-column-group：指定对象作为表格列组显示。类同于html标签<colgroup>（CSS2）
table-header-group：指定对象作为表格标题组。类同于html标签<thead>（CSS2）
table-footer-group：指定对象作为表格脚注组。类同于html标签<tfoot>（CSS2）
run-in：根据上下文决定对象是内联对象还是块级对象。（CSS3）
box：将对象作为弹性伸缩盒显示。（伸缩盒最老版本）（CSS3）
inline-box：将对象作为内联块级弹性伸缩盒显示。（伸缩盒最老版本）（CSS3）
flexbox：将对象作为弹性伸缩盒显示。（伸缩盒过渡版本）（CSS3）
inline-flexbox：将对象作为内联块级弹性伸缩盒显示。（伸缩盒过渡版本）（CSS3）
flex：将对象作为弹性伸缩盒显示。（伸缩盒最新版本）（CSS3）
inline-flex：将对象作为内联块级弹性伸缩盒显示。（伸缩盒最新版本）（CSS3）
```

** display:block **  
此元素将显示为块级元素，此元素前后会带有换行符；当前元素设置为block时默认为父元素的宽度，可设置宽高并换行显示。  
块级元素：会新开始一行并且尽可能撑满容器  例如：p h1 div  
行内元素：只占据它对应标签的边框所包含对的空间  例如：span button  

** display:inline **   
当元素设置为inline时默认为内容宽度，不可设置宽高并同行显示  

** display:inline-block **   
当元素设置为inline-block时默认为内容宽度但可设置宽高并同行显示   

** display:none **   
隐藏对象，并不保留物理空间  

** display:hidden **   
隐藏对象，并保留物理空间  


### 水平居中  
-  利用`margin: 0 auto;`水平居中
```
<style type="text/css">
		.container {
			height: 80px;
			border: 1px solid black;
		}
		.special {
			margin: 0 auto;
			width: 200px;
			height: 100%;
			background: orange;
		}
</style>

	<div class="container">
		<p class="special"></p>
	</div>
```

- 利用inline-block 可以使块级元素水平居中  

```
<style>  
		.container {
			text-align: center;
			border: 1px solid black;
      height: 200px;
		}
	.sub {
		display: inline-block;
		text-align: initial;
		width: 400px;
		height: 100%;
		background: red;
	}    
</style>  

<div class="container">
	<div class="sub">inline-block布局</div>
</div>
```


### 定位布局  

** position **    
该属性用于指定一个元素在文档中的定位方式  
语法：  
position：static | relative | absolute | fixed | center | page | sticky    
top/right/bottom/left: auto | length | percentage  

取值：  
static：对象遵循常规流。此时4个定位偏移属性不会被应用。  

relative：对象遵循常规流，并且参照自身在常规流中的位置通过top，right，bottom，left这4个定位偏移属性进行偏移时不会影响常规流中的任何元素。  

absolute：对象脱离常规流，此时偏移属性参照的是离自身最近的定位祖先元素，如果没有定位的祖先元素，则一直回溯到body元素。盒子的偏移位置不影响常规流中的任何元素，其margin不与其他任何margin折叠。  

fixed：与absolute一致，但偏移定位是以窗口为参考。当出现滚动条时，对象不会随着滚动。  

center：与absolute一致，但偏移定位是以定位祖先元素的中心点为参考。盒子在其包含容器垂直水平居中。（CSS3）  

page：与absolute一致。元素在分页媒体或者区域块内，元素的包含块始终是初始包含块，否则取决于每个absolute模式。（CSS3）  

sticky：对象在常态时遵循常规流。它就像是relative和fixed的合体，当在屏幕中时按常规流排版，当卷动到屏幕外时则表现如fixed。该属性的表现是现实中你见到的吸附效果。（CSS3）  

top，right，bottom，left属性决定了该元素的最终位置：  
![](/css/images/position.png)


** position:relative **  
relative相对定位，设置之后根据top，left等相对自身偏移。原本空间会被保留  
![](/css/images/position2.png)


** position:absolute **  
relative绝对定位，设置之后默认宽度为内容宽度，脱离文档流，参照物为第一个定位祖先/根元素  
![](/css/images/position3.png)


** position:fixed **  
fixed相对于浏览器窗口进行偏移  
![](/css/images/position4.png)

** z-index **  
当元素叠加时，z-index值较大的会覆盖在较小的上面  
![](/css/images/zindex.png)


** 遮罩层实现 **  

```
<style>  
	.mask {
		position: fixed;
		top: 0;
		left: 0;
		z-index: 999;
		width: 100%;
		height: 100%;
		background: #000;
		opacity: 0.4;
	}
</style>  

<div>这是遮罩层下的网站内容</div>
<div class="mask"></div>
```

** 弹出层实现 **  
```
<style>  
	.model {
		position: absolute;
		top: 0px;
		left: 120px;
		z-index: 999;
		width: 300px;
		height: 200px;
		background: red;
	}
  </style>  

   	<div>这是遮罩层下的网站内容</div>
   	<div class="model">弹出层内容</div>
```


### 浮动布局  

** float **  
指定元素沿其容器的左侧或右侧放置，允许文本和内联元素环绕它。使用float之后元素从文档流中移除但会保持部分的流动性  

语法：  
float：left | right | none  


** float:left **  
```
<style>  
	.container {
		border: 1px solid black;
	}
	.container div {
		width: 100px;
		height: 100px;
		float: left;
	}
	.box1 {
		background:blue;
	}
	.box2 {
		background:yellow;
	}
	.box3 {
		background:red;
	}
  </style>  

   	<div class="container">
   		<div class="box1">box1</div>
     	<div class="box2">box2</div>
     	<div class="box3">box3</div>
   	</div>
```
![](/css/images/float.png)  
说明：半脱离了文档流但会相互影响，不会重叠。父元素没有设置高度，若子元素脱离文档流后会导致父元素因没有内容而收缩。

** float:clear **  
clear属性指定元素是否跟随之前浮动的元素   
clear:none | left | right | both
- none：允许两边都可以有浮动  
- both：不允许两边有浮动  
- left：不允许左边有浮动  
- right：不允许右边有浮动  

```
<style>  
	.container {
		border: 1px solid black;
	}
  .container:after {
			content: '';
			display: block;
			clear: both;
	}
	.container div {
		width: 100px;
		height: 100px;
		float: left;
	}
	.box1 {
		background:blue;
	}
	.box2 {
		background:yellow;
	}
	.box3 {
		background:red;
	}
  </style>  

   	<div class="container">
   		<div class="box1">box1</div>
     	<div class="box2">box2</div>
     	<div class="box3">box3</div>
   	</div>
```
![](/css/images/float2.png)  

** 图文布局 **  
```
  <style>  
		.head {
			border: 1px dashed blue;
			padding: 10px;
			width: 400px;
		}
		.box1 {
			background: orange;
			width: 60px;
			height: 60px;
			float: left;
		}
		.box2 {

		}
    </style>  

     	<div class="head">
     		<div class="box1"></div>
	     	<div class="box2">
	     	反映比较集中的是无房户的比例问题，细则规定，公证摇号，应对“无房家庭”给予倾斜，提供一定比例的房源保障。至于比例是多少，倾斜到什么程度，方案没说。那么，问题来了，如果由开发商来确定，开发商会充分顾及无房户的利益吗？这个恐怕也很难，一个按揭一个一次性付款，开发商喜欢哪一个，不言自明。如此，无房户优先的意义自然会大打折扣。于是，各种口水都来了，纷纷猜测细则之后还有没有补丁。
	     </div>
     	</div>

```
![](/css/images/float3.png)  

** 定宽+自适应布局 **  
```
<style>  
		.slide {
			float: left;
			width: 200px;
			height: 200px;
			background: yellow;
		}
		.content {
			width: 100%;
			height: 200px;
			margin-left: 220px;
			background: orange;
		}
    </style>  

     	<div>
     		<div class="slide">
     			<p>左侧定宽-导航栏</p>
     		</div>
     		<div class="content">
     			<p>左侧自适应-内容区域</p>
     		</div>
     	</div>

```
![](/css/images/float4.png)  


** 定宽+自适应+定宽 布局 **  
```
<style>  
.slide {
	float: left;
	width: 200px;
	height: 200px;
	background: yellow;
}
.slide2 {
	float: right;
	width: 200px;
	height: 200px;
	background: blue;
}
.content {
	height: 200px;
	margin-left: 220px;
	margin-right: 220px;
	background: orange;
}
</style>  

<div>
	<div class="slide">
		<p>左侧定宽-导航栏</p>
	</div>
	<div class="slide2">
		<p>右侧定宽-相关信息</p>
	</div>
	<div class="content">
		<p>中间自适应-内容区域</p>
	</div>
</div>
```
![](/css/images/float5.png)  

### flex布局  
flex布局是W3C提出的新方案，可以更方便、完整、响应式实现页面布局，给盒模型提供了更大的灵活性。  

![](/css/images/flex.png)  

使用display:flex 可以指定容器为flex布局  

![](/css/images/flex2.png)  

flex包含以下几个部分：
- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

** flex-direction **  
flex-direction属性决定主轴的方向  
语法：  
flex-direction：row|row-reverse|column|column-reverse   

![](/css/images/flex3.png)  
![](/css/images/flex4.png)  
![](/css/images/flex5.png)  


** flex-wrap **  
flex-wrap控制flex容器是单行或者多行，同时决定新行堆叠的方向  
语法：  
flex-wrap:nowrap | wrap | wrap-reverse  

![](/css/images/flex6.png)  
![](/css/images/flex7.png)  
![](/css/images/flex8.png)

** flex-flow **  
flex-flow是flow-direction和flex-wrap属性的简写   
语法：  
`flex-flow: <flow-direction> || <flex-wrap>`  

** justify-content **  
justify-content属性定义了项目在主轴上的对齐方式  
语法：  
justify-content：flex-start | flex-end | center | space-between | space-around  

flex-start：开始位置对齐  
flex-end：结束位置对齐  
center：居中  
space-between：两端对齐，项目之间的间隔都相等  
space-around：每个项目两侧的间隔相等  

![](/css/images/justify-content.png)  
![](/css/images/justify-content2.png)  
![](/css/images/justify-content3.png)  
![](/css/images/justify-content4.png)  
![](/css/images/justify-content5.png)  
![](/css/images/justify-content6.png)  


** align-items **  
align-items属性定义项目在交叉轴上如何对齐  

语法：  
align-items:flex-start | flex-end | center | baseline | stretch  
flex-start:交叉轴的起点对齐  
flex-end:交叉轴的终点对齐  
center:交叉轴的中点对齐  
baseline:项目的第一行文字的基线对齐   
stretch:如果项目未设置高度或设为auto，将占满整个容器的高度  

![](/css/images/align-items.png)  
![](/css/images/align-items2.png)  
![](/css/images/align-items3.png)  
![](/css/images/align-items4.png)  
![](/css/images/align-items5.png)  

** order **  
order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0.
语法：`order:<number>`  
![](/css/images/order.png)  

** flex-grow **  
flex-grow属性定义项目的放大比例，默认为0，即存在剩余空间也不放大。  
语法：`flex-grow:<number>`  
![](/css/images/flex-grow.png)  

** flex-shrink **  
flex-shink属性定义项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。  
语法：`flex-shrink:<number>`  
![](/css/images/flex-shrink.png)  

** flex-basic **  
flex-basic属性定义了在分配多余空间之前，项目占据的主轴空间  
语法：`flex-basic:<length> | auto`  

** align-self **  
align-self属性允许单个项目有不一样的对齐方式，会覆盖  
语法：`auto | flex-start | flex-end | center | baseline | stretch`  

auto：如果'align-self'的值为'auto'，则其计算值为元素的父元素的'align-items'值，如果其没有父元素，则计算值为'stretch'。  
flex-start：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。  
flex-end：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。  
center：弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。  
baseline：如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。  
stretch：如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制。  

![](/css/images/align-self.png)  


** flex **  
flex属性是flex-grow,flex-shrink和flex-basic的缩写，默认为0 1 auto
语法：`flex：none | <' flex-grow '> <' flex-shrink >'? || <' flex-basis '>`


** 三行自适应+两列自适应 **  
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>  
		html,body {
			height: 100%;
			margin: 0px;
			padding: 0px;
		}
		body {
			display: flex;
			flex-flow: column;
		}
		.head,.foot {
			height: 100px;
			border: 1px dashed blue;
		}
		.body {
			flex: 1;
			flex-grow: 1;
			display: flex;
		}
		.side {
			width: 200px;
			border: 1px dashed blue;
		}
		.main {
			flex: 1;
			border: 1px dashed blue;
		}
    </style>  
    </head>  
    <body>  
     	<div class="head">head</div>
     	<div class="body">
     		<div class="side">side</div>
     		<div class="main">main</div>
     	</div>
     	<div class="foot">foot</div>
    </body>
</html>
```
![](/css/images/layout-flex.png)  
  
