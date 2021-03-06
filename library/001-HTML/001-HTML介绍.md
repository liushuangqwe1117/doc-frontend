### HTML发展历史
![](assets/html/images/history.png)

### HTML文档声明
- 首行、顶格
- <!DOCTYPE 声明内容>
- HTML4.0.1
  - strict.dtd
  - loose.dtd
  - frameset.dtd
- HTML5
  - <!DOCTYPE html>

查看各元素在不同文档类型中的支持情况：
1. http://www.w3school.com.cn/tags/html_ref_dtd.asp
2. https://caniuse.com/


### 元素分类
- 根元素  
  html

- 文档元数据  
  head,
  title,
  base,
  link,
  [meta](/html/meta.md),
  [style](/html/style.md)

- 内容分区  
  body,
  [article](/html/article.md),
  [section](/html/section.md),
  [nav](/html/nav.md),
  [aside](/html/aside.md),
  h1~h6,
  [header](/html/header.md),
  [footer](/html/footer.md),

  ![](assets/html/images/section.png)

- 分组内容  
  p,address,hr,pre,blockquote,main,div,
  [ol,ul,li,dl,dt,dd](/html/list.md),
  figure,figcaption

- 文本级语意  
  [a](/html/a.md),
  span,em,strong,cite,q,br,i,b,u,code,small,s,sub,sup  
  var,samp,kbd,mark,dfn,abbr,time,bdi,bdo,wbr,ruby,rb,rt,rtc,rp  

- 嵌入内容  
  [picture](/html/picture.md)
  source,
  [img](/html/image.md),
  [iframe](/html/iframe.md),
  embed,object,param  
  [video](/html/video.md),
  [audio](/html/audio.md),
  track,map,area,template,canvas

- 表格  
  table,caption,colgroup,col,tbody,thead,tfoot,tr,td,th

- 表单  
  [form](/html/form.md),
  label,input,button,select,datalist,optgroup,option  
  textarea,output,progress,meter,fieldset,legend

- 脚本  
  [script](/html/script.md) , noscript

- 交互  
  details,summary,dialog

- 编辑  
  ins,del


### 元素属性
- 全局属性  
  比如：id,class属性，每个元素都有，所以属于去全局属性  

- 元素属性   
  比如：`<input disabled="disabled">`中disabled不是每个元素都有的属性

- 自定义属性：以`data-`为前缀，避免与HTML未来属性名冲突    
  比如：`<input data-creator="admin">`  


参考书籍：
1. 《Head First HTML与CSS 第2版》O'Reilly出版，中国电力出版社
2. 《HTML5权威指南》图灵程序设计丛书，人民邮电出版社

参考网址：
1. http://www.w3school.com.cn/tags/html_ref_urlencode.html
2. https://www.w3.org/TR/html/
3. https://developer.mozilla.org/zh-CN/
