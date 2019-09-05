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

需要创建新的CSS文档

```css
a{
    font-size:40px;
    color:#ffffff;
}
```

**元素内嵌样式表的级别>文档内嵌样式表>外部内嵌样式表**

## CSS选择器

选择器一般只出现在**文档内嵌样式表**和**外部内嵌样式表**

```html
<!DOCtype html>
<html>
      <head>
        <meta charset  = "utf-8">
        <title>CSS选择器</title>	
          <!--根据类型选择元素-->
        <style type = "text/css">	   
          p{	
            font-size:40px;
            color: #ff582a;
          }
        </style>
      </head>
      <body>
		<p>字体</p>
        <a>字体</a>
        <h2>字体</h2>
      </body>
</html>
```

```html
<!DOCtype html>
<html>
    <head>
        <meta charset = "utf-8">
        <title>CSS选择器</title>
        <!--选择所有元素-->
        <style type = "text/css">
        	*{
        		font-size:40px;
        		color: #ff582a;
        	}
        </style>
    </head>
    <body>
		<p>字体</p>
        <a>字体</a>
        <h2>字体</h2>
    </body>
</html>
```

```html
<!DOCtype html>
<html>
<head>
  <meta charset="utf-8">
  <title>CSS选择器</title>
  <!--根据类选择元素-->
  <style type="text/css">
     .class2{
      font-size: 40px;
      color: #ff582a;
    }
  </style>
</head>
<body>
<p class = "class2">字体</p>	<!--class是一个全局标签,即所有的元素都有class标签.class后面的名字可以是任意名字-->
<a class = "class2">字体</a>
<h2>字体</h2>
</body>
</html>

```

```html
<!DOCtype html>
<html>
<head>
  <meta charset="utf-8">
  <title>CSS选择器</title>
  <!--根据ID选择元素-->
  <style type="text/css">
     #id2{
      font-size: 40px;
      color: #ff582a;
    }
  </style>
</head>
<body>
<p id = id2 >字体</p>		<!--id标签后面的名字只能附加给一个元素,唯一性-->
<a>字体</a>
<h2>字体</h2>
</body>
</html>
```

