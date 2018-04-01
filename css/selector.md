# 选择器
> 选择器是CSS规则的一部分且位于CSS声明块前；选择器是决定哪些样式规则会被应用于页面上元素的模式匹配规则

## 选择器分裂
- 简单选择器
- 属性选择器
- 伪类选择器
- 伪元素选择器
- 组合选择器
- 分用选择器

#### 简单选择器
> 通过元素类型、class、id或*匹配一个或多个元素

- 元素类型匹配：标签选择器
  ```
    div {
      color:blue;
      height:200px;
    }
  ```
- class匹配：类选择器
  - 匹配类名，以点开头
  - 字母、数字、-、\_组成
  - 类名必须以字母开头
  - 匹配大小写
  ```
    .special {
      color:blue;
    }

    <p class="special">段落<p>
  ```
- id匹配：id选择器
  - 匹配id名，以#开头
  - 字母、数字、-、\_组成
  - id名必须以字母开头
  - 匹配大小写
  ```
    #special {
      color:blue;
    }

    <p id="special">段落<p>
  ```
- \* 匹配：通配符选择器


#### 属性选择器
- 属性选择器-[att]：当元素设置了"att"属性时匹配，无论该属性的值是什么

```
[disabled] {
  color:blue;
  background:#ccc;
}

<input type="text" disabled />
```
- 属性选择器-[att=val]：当元素的"att"属性值恰好是"val"时匹配

```
[type='button'] {
  color:blue;
}

<input type="text"/>
<input type="button" value="按钮" />
```

- 属性选择器-[att~=val]：代表一个有"att"属性且值是一个由空白字符分隔的单词列表，其中之一恰好是"val"的元素

```
[class~='title'] {
  text-align:center;
  color:rgb(119,25,25);
}

<h1 class="article title">网易简介</h1>
```

- 属性选择器-[att^=val]：选择"att"属性的值val开头的元素

```
[class^='CN'] {
  text-align:center;
  color:rgb(119,25,25);
}

<h1 class="CN-title">你好</h1>
<h1 class="EN-title">hello</h1>
```

- 属性选择器-[att|=val]：选择att属性的值以val（包含val）或val- 开头的元素

```
[class|='CN'] {
  text-align:center;
  color:rgb(119,25,25);
}

<h1 class="CN-title">你好</h1>
<h1 class="EN-title">hello</h1>
```

- 属性选择器-[att$=val]：选择att属性的值以val结尾（包含val）的元素

```
[class$='special'] {
  color:rgb(119,25,25);
}

<h1 class="test-special">你好</h1>

```


#### 伪类与伪元素选择器
伪类：伪类根据元素的特征分类，而不是名字、属性或内容。  
伪元素：伪元素建立了对超出文档语言指定的文档树的抽象。  

注意：  
- 伪元素和伪类不会出现在源文档或者文档树中
- 伪类允许出现在选择器的任何位置，而一个伪元素只能跟在选择器的最后一个简单选择器后面
- 伪元素名和伪类名都是大小写不敏感的
- 有些伪类是互斥的，而其它的可以同时用在一个元素上


** 伪类选择器： :checked **  
匹配可被选中且被选中的元素
```
input:checked {
  height:50px;
  width:50px;
}

<input type="checkbox" value="Car" />是否有汽车
<input type="checkbox" value="Bike" checked="checked" />是否有自行车

```

** 伪类选择器： :empty**  
匹配没有任何子元素（包括text节点）的元素
```
p:empty {
  height:25px;
  border:1px solid #ddd;
  background:#eee;
}

<p>非空的</p>
<p><!-- 空的 --></p>
<p>非空的</p>

```

** 伪类选择器： :optional **  
选择器在表单元素是可选项时设置指定样式  

```
input:optional {
  background-color:yellow;
}

<p>可选input元素：<br/><input></p>
<p>必填input元素：<br/><input required></p>

```

** 伪类选择器： :read-only/:read-write **  
:read-only 选择只读属性的元素属性  
:read-write 选择没有只读属性的元素属性

```
input:read-only {
  background-color:yellow;
}
input:read-write {
  background-color:aqua;
}

<p>只读的input元素:<br/><input readonly></p>
<p>普通的input元素:<br/><input></p>

```  

** 伪类选择器： :required/:valid **  
:required 必填项时设置指定样式  
:valid 选择所有有效值的属性

```
input:required {
  background-color:yellow;
}
input:valid {
  border:1px solid red;
}

<p>必填的input元素:<br/><input required></p>
<p>有效的email元素:<br/><input type="email" value="a@163.com"></p>
<p>非法的email元素:<br/><input type="email" value="a@163@com"></p>

```  

** 伪类选择器： :target **  
:target 选择当前活动元素（点击URL包含锚的名字）  

```
:target {
  border:2px solid #D4D4D4;
  background-color:#e5eecc;
}

<h1>点击到相应内容块</h1>
<p><a href="#newsOne">跳到内容1</a></p>
<p><a href="#newsTwo">跳到内容2</a></p>
<p id="newsOne"><b>内容1...</b></p>
<p id="newsTwo"><b>内容2...</b></p>

```  

![](/css/images/target.png)


** 伪类选择器： :root **  
:root 匹配文档的根元素  
```
:root {
  background-color:#e5eecc;
}  

```

** 伪类选择器： :enabled/:disabled **  
:enabled 匹配用户界面上处于可用状态的元素  
:disabled 匹配用户界面上处于禁用状态的元素  
```
input[type="text":enabled] {
  border:1px solid #090;
  background:#fff;
  color:#000;
}
input[type="text":disabled] {
  border:1px solid #ccc;
  background:#eee;
  color:#ccc;
}

<li><input type="text" value="可用状态"></li>
<li><input type="text" value="禁用状态" disabled="disabled"></li>
```

** 伪类选择器： :first-child/:last-child **  
:first-child伪类匹配一个作为某个元素的第一个子级的元素  
:last-child伪类匹配一个作为某个元素的最后一个子级的元素  
```
<style type="text/css">
	p:first-child {
		color: red;
	}
	p:last-child {
		color:yellow;
	}
</style>
<div>
	<p>第一段</p>
	<p>第二段</p>
</div>
```

** 伪类选择器： E:nth-child(n)/E:nth-last-child(n) **  
E:nth-child(n) 匹配父元素的第n个子元素，假设该子元素不是E，则选择符无效  
E:nth-last-child(n) 匹配父元素的倒数第n个子元素,假设该子元素不是E，则选择符无效  

允许使用一个乘法因子（n）来作为换算方式：  
偶数子元素E:nth-child(2n)  
奇数子元素E:nth-child(2n+1)  

```
<style type="text/css">
	p:nth-child(2) {
		color: red;
	}
	p:nth-last-child(3) {
		color:blue;
	}
</style>
<div>
	<p>第一段</p>
	<p>第二段</p>
    <p>第三段</p>
</div>

```


** 伪类选择器： :link与:visited **  
:link 伪类应用于未被访问过的链接  
:visited 伪类应用于曾被用户访问过的链接  
这两种状态是互斥的

** 伪类选择器： :hover与:focus **  
:hover 应用于鼠标移入元素上时  
:focus 应用于当一个元素拥有焦点  

```
<style type="text/css">
		p:hover {
			color:red;
		}
		input:focus {
			color: red;
		}
</style>

<p>注意观察被选中的颜色</p>
<input type="text">
```

** 伪元素选择器： ::first-letter **  
选择元素的第一个字母
```
p::first-letter {
  color:red;
}
<p>Hello World</p>
```

** 伪元素选择器： ::first-line **  
选择元素的第一行
```
p::first-line {
  color:red;
}
<p>
第一行 <br/>
第二行
</p>
```

** 伪元素选择器： ::before和::after **  
::before 在元素之前插入内容  
::after 在元素之后插入内容  
经测试，两个冒号和一个冒号的都可以

```
<style type="text/css">
		p::before {
			content: "read this - ";
			background-color: yellow;
			color: red;
			font-weight: bold;
		}
</style>

<p>pig</p>
<p>dog</p>
```

** 伪元素选择器： ::selection **  
::selection 用于被用户选中的内容  
```
<style type="text/css">
		p::selection {
			background-color: #ccc;
			color: red;
			font-weight: bold;
		}
</style>

<p>注意观察被选中的颜色</p>

```
