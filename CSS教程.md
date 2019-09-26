# CSS教程

---

## CSS初步

```css
/*CSS注释,用在style中*/
```



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

```html
<!DOCtype html>
<html>
<head>
  <meta charset="utf-8">
  <title>CSS选择器</title>
  <!--根据属性选择元素-->
  <!--如果要只选择特定网址只需要改成[href = "http://github.com"]-->
  <style type="text/css">
    [href]{			
      font-size: 40px;
      color: #ff582a;
    }
  </style>
</head>
<body>
<p>字体</p>
<a href = "http://baidu.com">字体</a>
<a href = "http://github.com">字体</a>
</body>
</html>
```

```html
<!DOCtype html>
<html>
<head>
  <meta charset="utf-8">
  <title>CSS选择器</title>
  <!--冒号选择器-->
  <!--hover代表鼠标滑过时-->
  <style type="text/css">
    a:hover{
        font-size: 80px;
        color:red;
    }
  </style>
</head>
<body>
<p>字体</p>
<a href = "http://baidu.com">字体</a>
<!--<a href = "http://github.com">字体</a>-->
</body>
</html>
```

## 创建边框和背景

```html
<!--定义简单边框-->
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset="UTF-8">
    <title>创建边框和背景</title>
    <style type = "text/css">
      .class1{
          border-width: 20px ;     /*边框宽度*/
          border-style: solid;    /*边框样式*/
          border-color: red;       /*边框颜色*/
          border-top-color: blue;   /*边框上层颜色*/
      }
    </style>
</head>
<body>
    <p class="class1" >标题</p>
</body>
</html>
```

```html
<!--border的简写-->
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset="UTF-8">
    <title>创建边框和背景</title>
    <style type = "text/css">
      .class1{
            border: 10px solid red;     /*按照宽度,样式，颜色的顺序*/
            border-top: 20px dashed blue;   /*同上*/
      }
    </style>
</head>
<body>
    <p class="class1" >标题</p>
</body>
</html>

```

```html
<!--背景-->
<!DOCTYPE html>
<html lang = "en">
<head>
    <meta charset="UTF-8">
    <title>创建边框和背景</title>
    <style type = "text/css">
      .class1{
          width:800px;  /*选择器的宽度*/
          height: 800px;    /*选择器的高度*/
        /*background-color: greenyellow;  !*背景颜色*!*/
          background-image:
              url("https://mewhz.com/usr/uploads/2019/07/695131174.jpg"); 
          /*设置背景图片,url中放入图片链接*/
          background-size: cover;   /*设置背景的显示方式*/
                                    /*cover平铺整个屏幕*/
          background-attachment: fixed;     /*图片的固定方式*/
                                            /*fixed随着页面的滚动而滚动*/
      }
    </style>
</head>
<body>
    <p class="class1" >文字</p>
</body>
</html>

```

## CSS设置w文本样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS设置文本样式</title>
    <style type="text/css">
        .class1{
            text-align: center;/*文本对齐方式*/
            /*center居中;right右对齐;left左对齐(默认)*/
            direction: ltr;/*文本方向*/
            /*ltr从左边到右边;rtl从右边到左边*/
            letter-spacing: 10px;/*字母间距*/
        }
        .class2{
            word-spacing: 200px;/*单词间距*/
        }
        .class3{
            line-height: 100px;/*行高*/
        }
        .class4{
            text-indent: 200px;/*首行缩进*/
        }
    </style>
</head>
<body>
    <p class="class1">文字</p>
    <p class="class2">hello world</p>
    <p class="class3">hello worldh</p>
    <p class="class4">缩进测试</p>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS设置文本样式</title>
    <style type="text/css">
        .class1{
            text-decoration: overline;/*文本装饰*/
            /*underline是下划线;overline是上划线;line-through中间穿过一条线(删除线)*/
        }
        .class2{
            text-transform: capitalize;/*单词首字母大写*/
            /*uppercase全单词大写;lowercase全单词小写*/
        }
    </style>
</head>
<body>
    <p class="class1">我是文本</p>
    <p class="class2">hello world</p>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS设置文本样式</title>
    <style type="text/css">
        .class1{
            font-family: 楷体;/*设置字体名称*/
            font-size: 40px;/*设置字体大小*/
            font-style: italic;/*设置字体样式*/
            /*italic斜体;*/
            font-weight: bold;/*粗体*/
            text-shadow: 10px 10px 1px red;/*设置字体的阴影样式*/
            /*分别对应着水平偏移，垂直偏移，模糊程度，阴影颜色*/
        }
    </style>
</head>
<body>
    <p class="class1">我是文本</p>
</body>
</html>
```

## CSS使用过渡

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>创建文本过渡</title>
</head>
<style type="text/css">
    p {
        height: 100px;
        width: 100px;
        background-color: lawngreen;
    }
    /*p:hover{*/
    /*    !*直接过渡法*!*/
    /*    width:200px;*/
    /*    height: 200px;*/
    /*    background-color: magenta;*/
    /*}*/
    p:hover{
        width:200px;
        height: 200px;
        background-color: magenta;
        transition-delay: 100ms;/*延迟时间*/
        transition-duration: 1000ms;/*动画反应时间*/
        transition-property: background-color;/*这里面放的属性代表该属性慢慢变化,其余直接变化*/
    }
</style>
<body>
    <p>
    </p>
</body>
</html>
```

