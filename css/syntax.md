# CSS语法

### 引入CSS三种方式
1. 内联方式
2. 内部样式块
3. 外链样式

![](/css/images/leadin.png)

### CSS基本语法
- 样式定义：选择器{属性声明列表}
- 属性声明：属性名:属性值;
- 注释：/\* 多行注释内容 \*/

```
/* 样式定义例子 */
h2 {
  color:red;
  font-size:16px;
}
```

### 规则集
- CSS：由一个个规则集组成
- 规则集：选择器和一个声明块组成
- 选择器：一串用连接符分隔的一个或多个简单选择器
- 声明块：以 { 开始，以 } 结束，包含一个或多个属性声明

![](/css/images/rule.png)

### 注释
- 以 /\* 开始，以 \*/ 结束
- 注释不能嵌套
- 注释内容对渲染没有影响

### 选择器语法
![](/css/images/selector.png)

### 属性语法
![](/css/images/property.png)

### 属性名
属性名是一个标识符
```
/*
  color和font-size就是属性名
 */
h2 {
  color:red;
  font-size:16px;
}
```
** 浏览器私有属性 **
- chrome,safari：-webkit-
- firefox：-moz-
- IE：-ms-
- opera：-o-
```
div {
	-webkit-border-radius:40px 10px;
	-moz-border-radius:40px 10px;
	-ms-border-radius:40px 10px;
	-o-border-radius:40px 10px;
	border-radius:40px 10px;
}
```

### 属性值
属性值中可以出现任何token。圆括号、单引号、双引号等，其中引号必须成对出现
```
/* 以下三种写法都对 */
div {
	background: url(163.jpg);
	background: url('163.jpg');
	background: url("163.jpg");
}
```
![](/css/images/after.png)

** 属性值语法 **  
- 关键字  
  auto,solid,bold,ease-in...  
  inherit,initial(特殊关键字)
- 类型  
  基本类型：<length>,<percentage>,<color>...  
  其他类型：<padding-width>,<color-stop>
- 符号(/,)  
  border-radius:10px 20px 30px 40px/5px 10px 15px 20px;  
  font-family:"Times New Roman",Georgia,Serif  
- 值类型  
  - 整数<integer>和实数<number>：number包含integer
  - 长度<length>：相对或绝对值  
    格式：<number>后面紧跟着一个单位标识符  
    ```
      h1 {margin:0.5em;}
      h1 {margin:0;}
      p {font-size:10px;}
      p {line-height:120%;}/* 120% of 'font-size' */
    ```
  - 百分比  
    格式：一个<number>后面紧跟着'%'  
  - URL与URI  
    格式：用来指定属性值中URI的函数标记是"url()"
    ```
      body {background:url(./mail.png);}
    ```
  - 计数器（counter-increment）  
    说明：对部分和子部分进行编号（比如 "Section 1"、"1.1"、"1.2"）的方法
    ```
    <!DOCTYPE html>
    <html lang="en">
    <meta charset="utf-8">
    <head>
    <style type="text/css">
    body {counter-reset:section;}
    h1 {counter-reset:subsection;}
    h1:before
    {
    counter-increment:section;
    content:"Section " counter(section) ". ";
    }
    h2:before
    {
    counter-increment:subsection;
    content:counter(section) "." counter(subsection) " ";
    }
    </style>
    </head>

    <body>

    <p><b>注释：</b>如果已规定 !DOCTYPE，那么 Internet Explorer 8 （以及更高版本）支持 counter-increment 属性。</p>

    <h1>HTML tutorials</h1>
    <h2>HTML Tutorial</h2>
    <h2>XHTML Tutorial</h2>
    <h2>CSS Tutorial</h2>

    <h1>Scripting tutorials</h1>
    <h2>JavaScript</h2>
    <h2>VBScript</h2>

    <h1>XML tutorials</h1>
    <h2>XML</h2>
    <h2>XSL</h2>

    </body>
    </html>
    ```
    效果图如下：
    ![](/css/images/counter.png)
    可以配置为罗马字符排序
    ![](/css/images/counter2.png)

  - 颜色  
    格式：关键字(red,blue,green...)、RGB规范的值、16进制颜色值
    ```
      body {
        color:red;
        color:white;
        color:rgb(255,0,0);
        color:rgb(255,0,0,0.2);
        color:#FF0000;
        color:#F00;
      }
    ```
  - 字符串
    ```
      a[title="news"] {

      }
    ```

### 组合符号  
- "与"组合符号（&&）：连接各个部分，但是顺序任意  
  ```
  text-shadow:none|<shadow>[,<shadow>]*
  <shadow>=<length>{2,3}&&<color>?
  ```
  以上格式说明：text-shadow属性值要么为none，要么为length值且length值最小2个值，最大2个值，且颜色可以有可无
  ![](/css/images/and.png)

- "或"组合符号（||）：表示其连接的所有组成元素是可选的，次序任意，但是至少要出现一个  
  [text-decoration参考](http://www.css88.com/book/css/properties/text-decoration/text-decoration.htm)
  ```
  text-decoration:<' text-decoration-line '> || <' text-decoration-style'> || <' text-decoration-color'>
  ```
  ![](/css/images/text-decoration.png)

- "互斥"组合符号（|）：表示只能出现一个值  
  ```
    width:<length>|<percentage>|auto
  ```
  ![](/css/images/width.png)


### 数量符号  
数量符号：用来描述一个元素可以出现多少次。若不标注，则表示这个元素只出现一次

- 无标注：表示这个元素只出现一次
  ```
    width:<length>|<percentage>|auto
  ```  
- \* 标注：表示可以出现零次、一次、多次
  ```
    background-image:<bg-image>[,<bg-image>]*
  ```
  ```
    background-image:url("1.jpg"),url("2.jpg")
  ```
- ? 标注：表示可以出现零次或一次，不能出现多次  
  ```
  [ <' font-style '> || <' font-variant '> || <' font-weight '> ]? <' font-size '>
  ```
- {} 标注：包含两个以逗号分隔的整数A与B，表示最少出现A次，且最多出现B次
  ```
  margin:[<length>|<percentage>|auto]{1,4}
  ```
- \# 标注：表示可以出现一次或多次但是其多次出现必须以逗号分隔
  ```
  font-family：[ <family-name> | <generic-family> ] #
  ```
  ![](/css/images/font-family.png)


### @规则语法
语法：@标识符 xxx;@标识符 xxx {}
```
@import 'custom.css';
@media(min-width:801) {
  body {
    margin:0 auto;
    width:800px;
  }
}
```
主要有如下规则：
- @media
- @keyframes
- @font-face
- @import
- @charset
- @namespace
- @page
- @supports
- @document  
示例：
  ![](/css/images/media.png)
