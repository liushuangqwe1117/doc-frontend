# CSS盒模型  
每个盒子都有：外边距、边框、填充、内容四个属性  

 ![](/css/images/box1.png)

margin、border、padding都有top、right、bottom、left四部分
 ![](/css/images/box2.png)

 ### 元素分类：
 - 块级元素block：
    ```
    div,p,h1...h6,ol,ul,dl,table,address,blockquote,form
    ```
 - 行内元素inline：
    ```
    a,span,br,i,em,strong,label,q,var,cite,code
    ```
 - 内联块元素inline-block：
    ```
    img,input,textarea,select,button,caption
    ```

### max-width与min-width  
max-width:<length> | <percentage> | none  
min-width:<length> | <percentage> | none  
给元素设置最大宽度，避免width设置过大  
注意：max-width会覆盖width设置，但是min-width优先级高于max-width  


### max-height与min-height  
max-height:<length> | <percentage> | none  
min-height:<length> | <percentage> | none  
给元素设置最大高度，避免height设置过大  
注意：max-height会覆盖height设置，但是min-height优先级高于max-height  


### padding  
padding:[<lenght> | <percentage>]{1,4}  

** padding值 **  
 ![](/css/images/padding.png)

** 缩写值 **  
 ![](/css/images/padding2.png)

 ### margin  
 margin:[<lenght> | <percentage> | auto]{1,4}  

 ** margin合并 **  
 margin合并:两个垂直外边距相遇时它们将形成一个外边距。合并后的外边距高度为较大者  
 - 上下相邻元素margin合并
     ![](/css/images/margin.png)

 - 父子元素margin合并  
     ![](/css/images/margin2.png)
     说明：DIV1的magin-top不是相对父容器DIV2，而是相对与DIV2相邻的上面的元素，与DIV2的margin-top参考一样，所以合并取最大的margin-top

### border  
border：设置对象边框的特性  
语法：  
`border：<line-width> || <line-style> || <color>`

border-width：设置或检索对象边框宽度  
语法：  
`border-width：<line-width>{1,4}`  
`<line-width> = <length> | thin | medium | thick`

border-style：设置或检索对象边框样式  
语法：  
`border-style：<line-style>{1,4}`  
`<line-style> = none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset`

border-color：设置或检索对象边框颜色  
语法：  
`border-color：<color>{1,4}`

### border-radius  
border-radius用来设置边框圆角  
语法：  
`border-radius：[ <length> | <percentage> ]{1,4} [ / [ <length> | <percentage> ]{1,4} ]?`

示例：  
![](/css/images/border-radius.png)

![](/css/images/border-radius2.png)

![](/css/images/border-radius3.png)

![](/css/images/border-radius4.png)

![](/css/images/border-radius5.png)


### overflow  
该属性指定了块容器元素的内容从该元素的盒中溢出时是否需要剪裁。它会影响元素内所有
内容的裁剪，包括该元素的所有后代元素的内容及其后代  
语法：  
`overflow： visible | hidden | scroll | auto | inherit`  

** visible **   
visible:对溢出内容不做处理，内容可能会超出容器  
![](/css/images/overflow.png)

** hidden **   
visible:隐藏溢出容器的内容且不出现滚动条  
![](/css/images/overflow2.png)

** scroll **   
scroll:隐藏溢出容器的内容，始终有保持可见的滚动机制  
![](/css/images/overflow3.png)

** auto **   
auto:按需出现滚动条  
![](/css/images/overflow4.png)

### box-sizing  
更改用于计算元素宽度和高度的默认的CSS盒模型  
![](/css/images/box-sizing.png)

语法：  
`box-sizing：content-box： | border-box`  

content-box：是默认值  
&emsp;&emsp;paddding+border+width=盒子的实际宽度  
&emsp;&emsp;paddding+border+height=盒子的实际高度  

border-box：  
&emsp;&emsp;width=盒子的实际宽度  
&emsp;&emsp;height=盒子的实际高度  

![](/css/images/box-sizing2.png)  

![](/css/images/box-sizing3.png)  


### box-shadow/outline  
为元素设置阴影，以逗号分割列表来描述一个或多个阴影效果  
语法：  
`box-shadow：none | <shadow> [ , <shadow> ]*`  
`<shadow> = inset? && <length>{2,4} && <color>?`

![](/css/images/box-shadow.png)  

![](/css/images/box-shadow2.png)  

![](/css/images/box-shadow3.png)  

### outline  
用来设置一个或多个单独的轮廓属性的简写属性   
轮廓与边框的区别：
- 轮廓不占据空间，不影响布局，它们被描绘于内容之上  

语法：  
`outline：<' outline-width '> || <' outline-style '> || <' outline-color '>`  
`outline-width：<length> | thin | medium | thick`  
`outline-style：none | dotted | dashed | solid | double | groove | ridge | inset | outset`  
`outline-color：<color> | invert`  

![](/css/images/outline.png)  

![](/css/images/outline2.png)  



### 水平居中  
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
