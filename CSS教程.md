# CSS教程

---

## CSS初步

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>创建CSS</title>
    <link rel="stylesheet" type="text/css" href="a.css">	<!--导入外部css样式,文件名是a.css-->
    <!--文档内嵌样式表,修改效果体现在下面的a标签中-->
    <style type="text/css">		
    a{
        font-size:40px;
        color:#ffffff;
     }
    </style>
<!--font-size与color和下面的效果与用法一样.-->
</head>
<body>
    <a>文字</a>
    <a style=""></a>	<!--元素内嵌样式表--> 
<!--style是一个CSS样式属性，是一个全局的属性-->
</body>
</html>
```

```html
<body>
    <a style="font-size:40px;color:#ffffff">文字</a>	<!--font-size表示修改字体大小,后面的40px代表40像素,多种属性值元素用“;”隔开。color表示字体修改字体颜色,后面的#ffffff代表颜色的数值-->
</body>
```

**外部样式表**

```css
a{
    font-size:40px;
    color:#ffffff;
}
```

**元素内嵌样式表的级别>文档内嵌样式表>外部内嵌样式表**