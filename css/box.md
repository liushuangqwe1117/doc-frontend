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
