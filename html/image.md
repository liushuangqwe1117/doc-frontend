## img元素介绍

### 属性
- src：图片的地址
- alt：图片不存在时显示的文字
- with：图片显示宽度
- height：图片显示高度
- usemap：图片热点
- ismap
- referrerpolicy
- crossorigin
- longdesc
- srcset：[参考内容](https://www.jianshu.com/p/607567e488fc)
  - 宽度描述符
  ```
  <img srcset=“
        http://placehold.it/2000 2000w,
        http://placehold.it/1500 1500w,
        http://placehold.it/1000 1000w,
        http://placehold.it/500 500w
    "
    sizes=“
        (max-width: 500px) 500px,
        (max-width: 1000px) 1000px,
        (max-width: 1500px) 1500px,
        2000px
    "
    src="http://placehold.it/500/abc"
/>
  ```
  述例子的意思是：对于 viewport 在 500px 及以下的使用 500w 的图片，以此类推

  - 像素密度描述符
  ```
  <img srcset=“
        http://placehold.it/2500 5x,
        http://placehold.it/1500 3x,
        http://placehold.it/1000 2x,
        http://placehold.it/500 1x
    "
    src="http://placehold.it/500/abc"
    />
  ```
  上面代码的意思就是：5像素比（现在很多安卓手机比如小米、华为的所谓高清2k屏就是5像素比以上的）的设备使用2500x2500像素的图片，3像素比的设备使用1500x1500像素的图片，2像素比的设备使用1000x1000像素的图片，1像素比（普通的笔记本电脑显示屏就是1像素比的）的设备使用500x500像素比的图片。我们的PC机一般为1像素比

- sizes：必须和srcset属性配合使用且srcset属性为宽度描述符

### 图片热点
- map
  - name
- area
  - alt
  - href
  - shape
  - coords
  - download
  - hreflang
  - rel
  - target
  - type
  - referrerpolicy
  ![](/html/images/image1.png)
