**1.水平居中**
1. 对于行内元素
> 1. ```text-align:center;```
2. 对于确定宽度的块级元素
> 1. margin和width实现水平居中  

```CSS
.content{
    margin-left:auto;
    margin-right:auto;
}
```

> 2. 绝对定位，left为50%以及设置元素margin-left为其宽度的一半

```CSS
.content{
    width: 200px;
    position: absolute;
    left: 50%;
    margin-left: -100px; //该元素宽度的一半，即100px
    background-color: aqua;
}
```  

> 3. 绝对定位和margin:auto

```CSS
.content{
    position: absolute;
    width: 200px;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
}
```

3. 对于宽度不确定的块级元素
> 1. 通过给要居中显示的元素，设置display:table，然后设置margin:0 auto来实现

```CSS
.content{
    display:table;
    margin:0 auto;
    border:1px solid red;
}
```

> 2. 多个块状元素时，子元素设置inline-block，同时父元素设置text-align:center

```HTML
<div class="center">
    <div class="inlineblock-div">1</div>
    <div class="inlineblock-div">2</div>
</div>
```

```CSS
.center{
    text-align:center;
}
.inlineblock-div{
    display:inline-block;
}
```
