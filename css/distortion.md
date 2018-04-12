# 变形  

### transform  
transform:none | \<transform-function\>+  
eg:`<body style="transform: rotate(180deg);">`   


** rotate() **  
语法：rotate(<angle>)   
eg：  
transform: rotate(46deg);  
transform: rotate(-60deg);


** translate() **  
语法：`translate(<translation-value> [,<translation-value>]?)  `  
eg:   
translateX(<translation-value\>)  
translateY(<translation-value\>)  

transform:translate(50px);   
transform:translate(50px,20%);     

![](/css/images/transform.png)

** scale() **  
语法：`scale( <number> [, number]? )`  
eg:  
scaleX( <number\> )  
scaleY( <number\> )  

transform:scale(1.2);  
transform:scale(1,1.2);  
transform:scaleX(1.2);  
transform:scaleY(1.2);  

![](/css/images/scale.png)

** skew() **  
语法：`skew( <angle> [, <angle>]? )`  
eg:  
skewX( <angle\> )  
skewY( <angle\> )  

transform:skew(30deg)   
transform:skew(30deg,30deg)   
transform:skewX(30deg)  
transform:skewY(30deg)  

![](/css/images/skew.png)

** 多重效果 **  
![](/css/images/transform2.png)

### transform-origin  
![](/css/images/transform-origin.png)  

### perspective  
![](/css/images/perspective.png)  

### perspective-origin  
![](/css/images/perspective-origin.png)  

### translate3d()  
![](/css/images/translate3d.png)  

### scale3d()  
![](/css/images/scale3d.png)  

### rotate3d()  
![](/css/images/rotate3d.png)  

### transform-style  
![](/css/images/transform-style.png)  

### backface-visibility  
![](/css/images/backface-visibility.png)  
