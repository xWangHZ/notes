# html教程

---

## 创建html文档



``` html
<!doctype html> <!--告诉浏览器使用的是html的内容,可不写.-->
<!---->			<!--html文档的注释,注释掉时再浏览器查看源代码依然可以看到.-->
<html lang=”en“>  <!--根元素,表示文档中html部分的开始.其中lang代表语言,”en“代表文档为英文,"zh"代表中文.lang可删掉不写.-->
	<head>	<!--头元素,里面包含的是源数据.用来提供文档有关内容和标注信息-->
        <meta charset="UTF-8">	<!--代表以UTF-8的形式编码整个文档-->
        <title>		<!--标题的意思,<title>与</title>之间的字符为网页标题-->
            Hello	<!--Hello为网页标题-->
        </title>	<!--代表<title>元素结束-->
    </head>		<!--代表<head>元素结束-->
    <body>		<!--再该元素中写入的内容都会在网页中输出.-->
        
    </body>		<!--代表<body>元素结束-->
</html>		<!--代表<html>部分的结束-->
```

## html的基本元素(初步)

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>标题</title>
    </head>
    <body>
        <a href="链接" target="链接属性">	
<!--代表超链接,链接处放网址或本地html的文档.<a>与</a>之间为链接名称.最后一项target为链接属性,”_blank“为新建窗口打开链接;"_self"为覆盖原窗口打开新链接.什么都不加默认为"_self"-->
			链接名称	<!--链接名称-->
        </a>	<!--结束<a>元素-->
        <b>		<!--中间的字符以加粗在网页中显示-->
        	我是文字	<!--加粗的字符-->
        </b>	<!--结束<b>元素-->
        <em>	<!--中间的字符以斜体在网页中显示-->
        	我是文字	<!--斜体的字符-->
        </em>	<!--结束<em>元素-->
        <u>		<!--中间的字符以带下划线的形式在网页中显示-->
        	我是文字	<!--带下划线文字-->
        </u>	<!--结束<u>元素-->
        <s>		<!--中间的字符中放上删除线-->
        	我是文字	<!--字符上面显示删除线-->
        </s>	<!--结束<u>元素-->
    </body>
</html>
```

## html5表格元素

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>标题</title>
    </head>
    <body>
        <table>		<!--表格元素-->
            <tr>	<!--代表一个单元行,多个<td>元素代表每行单元行-->
            	<th>单元格元素(表头)</th>		<!--<th>中代表每个单元格的表头,以加粗居中形式存在,多个<th>元素并列-->
        	</tr>
            <tr>    
        		<td colspan=“合并的数量”>单元格元素</td>		<!--<tr>中代表每个单元格数据,左对齐,多个<tr>元素并列.colspan代表合并单元格,合并时需要删除被合并的其余单元格,只保留一个单元格,colspan="数量",数量代表一共合并多少单元格-->
                <td rowpan="合并数量">单元格元素</td>	<!--rowpan代表合并列单元格,合并时需要删除被合并的其余单元格,只保留一个单元格,rowpan="数量",数量代表一共合并多少单元格-->
            </tr>	
        </table>
        <br>	<!--换行-->
    </body>
</html>
```

## html5列表元素

```html
<!doctype html>
<html>
	<head>
        <meta charset="utf-8">
        <title>标题</title>
    </head>
    <body>
        <ol reversed>	<!--代表有序列表,即以1,2排列的列表.属性:reversed代表降序,不加默认是升序;type=”字符“代表按照什么字符顺序向下排列,支持”a,A,I,i,1“不加默认按照1排列-->
            <ol>	<!--在<ol>元素中在新建<ol>代表次级列表,默认缩进一个Tab-->
                
            </ol>
            <li>列表元素</li>	<!--代表列表中的每个元素,多个<li>元素时依次按照1,2,3向下排列-->
        </ol>
        <ul>	<!--无序列表,即没有任何字符顺序,全部按照小圆点向下排列-->
            <li>列表元素</li>
        </ul>
    </body>
</html>
```

## html5表单元素

### 定义

> **表单是HTML中获取用户输入的手段**

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>标题</title>
    </head>
    <body>
        <form>	<!--表单元素-->
            <input >		<!--单行文本框,表单元素的输入字段,其中包含很多元素,不需要</input>.-->
            <textarea rows="行距离" cols="列距离">文本框文本</textarea>		<!--多行文本框,中间放置文本框文本,“rows”为行距离数量,“cols”为列距离数量-->
            <button>文本</button>		<!--按钮元素,中间的文本为按钮的文本.通常与js合作并且绑定事件-->
            <select>	<!--有多选值的下拉框-->
                <option>选项一</option>	<!--下拉框的选项,中间的文本为选项的内容-->
                <option>选项二</option>
                <option>选项三</option>
            </select>
            <input type="text" list="data">	<!--list属性,可以将id为data的下拉框关联起来-->
    			<datalist id="data">	<!--再不关联的时候是不显示的,id中的内容,可以在list中关联,关联后可以再输入框中输入或选择以下选项-->
        			<option>苹果</option>
        			<option>香蕉</option>
    			</datalist>
        </form>
    </body>
</html>
```

```html
<input type="text">   <!--type指定input元素的类型,什么都不写默认为“text”-->
<input type="text" value="文本">	<!--value中的文本指定输入框的文本,占文本框的位置,再次输入时,在该文本后方输入,文本框的文字可删除-->
<input type="text" placeholder=“文本”>	<!--placeholder中的文本在输入框的后面,即不占文本框的,在输入框输入文字时,该文本自动消失--> 	
<input type="text" placeholder="文本" maxlength="数量">		<!--maxlength中的数量限制了输入的字符数,不能超过规定的字符数量-->
<input type="text" placeholder="文本" size="数量">		<!--max中的数量可以拓宽输入文本框的大小,使文本框显示规定的长度-->
<input type="text" value="文本" readonly>		<!--使文本在输入框只读,无法修改与填充-->
<input type="password" placehoder="文本">		<!--password类型,代表密码类型，此时在输入框中输入的数据为小黑点-->
<input type="button" value="按钮">		<!--button按钮属性,后面不追加属性时,按钮上什么都不会出现,value后面的文本为按钮上的文字-->
<input type="submit" value="按钮">	<!--与上一个功能类似,通常用作提交表单-->
<input type="range">	<!--滑动长条的特效,不用浏览器中显示不用的样子-->
<input type="range" min="数值" max="数值">		<!--min规定滑动长条的最小值,max规定滑动长块的最大值-->
<input type="range" min="数值" max="数值" step="数值">	<!--step规定了每次滑动的长度-->
<input type="range" min="数值" max="数值" step="数值" value="数值">
<!--value规定了打开网页时候的起始值,当没有value时默认从中间开始-->
<input type="number" min="数值" max="数值" value="数值">		
<!--number属性显示单行输入框,拥有上下数值调节键,min规定最小值,max规定最大值,value规定初始值-->
<input type="checkbox">文本	<!--checkbox选择框属性,文本中的内容为选择栏旁边的文本内容,选中区为方块,并且选中后可取消-->
<input type="radio">文本		<!--radio选择框属性,文本中的内容为选择栏旁边的文本内容,选中区为圆圈,并且选中后不可取消,通常用来生成固定选项-->
<input type="radio" name="a">文本		<!--name中如果为a则该选项只能选择一个,b时只能选择两个,以此类推-->
<input type="radio" name="a" checked>文本		<!--拥有checked属性的选择框,打开网页时默认选择-->
<input type="email">		<!--利用输入框获取电子邮件,只有在提交表单时才会检查数据-->
<input type="url">			<!--利用输入框获取网址,只有在提交表单时才会检查数据-->
<input type="tel">			<!--利用输入框获取电话号码,只有在提交表单时才会检查数据-->
<input type="date">			<!--利用输入框获取时间,拥有下拉框可以调出日历选择-->
<input type="color">		<!--获取颜色-->
<input type="hidden" value="数据">		<!--生成隐藏的数据项-->
<input type="image" src="图片路径" width="80px">	<!--生成图片按钮,src后面接图片路径,width后面接图片的像素大小,例如80px,代表80像素-->
<input type="file" multiple>	<!--上传文件,代表上传多个-->
<input type="file" required>	<!--代表上传一个,默认上传一个-->
```

## html5嵌入图片与创建分区相应图

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>标题</title>
</head>
<body>
	<img src="地址" width="宽度" height=“高度” alt="文字">		
<!--图片元素,src后面接图片地址,width中写入代表宽度,当只有width时,高度变成与宽度一样,height代表高度,当图片地址错误时,在浏览器上显示alt的内容-->
</body>
</html>
```

### 如何点击图片进入超链接

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>标题</title>
</head>
<body>
	<a href="链接">	<!--<a>中可以放任何东西,此时的链接为点击图片进入的链接-->
    	<img src="地址" width="宽度" height=“高度” alt="文字">
    </a>   
</body>
```

### 创建分区相应图

```html
<!doctype html>
<html>
<head>
	<meta charset="utf-8">
    <title>标题</title>
</head>
<body>
	<img stc="地址" usemap="#map1">	<!--usemap与map元素中名叫map1的map元素关联,需要在名字面前加#-->
    <map name="map1">		<!--name中名字用于与usemap关联,map元素,客户端分区响应的关键元素-->
    <area>	<!--可以为多个,每个各自代表图像上可以被点击的一块区域-->
    
    </map>
</body>
</html>
```

```html
<area href="链接">		<!--链接为点击图片时跳转的链接-->
<area href="链接" target="_blank">	<!--跳转链接时打开一个新建页-->
<area alt="备用内容">		<!--当图片错误时显示alt的内容-->
<area htef="链接" alt="备用内容" shape="属性" coords="1,2,3,4">
<!--shape与coords共同起作用,shape代表用户可点击的图像区域,coords代表区域数值-->
<area htef="链接" alt="备用内容" shape="rect" coords="x1,y1,x2,y2">	
<!--rect代表一个矩形区域,用四个逗号分隔的整数组成,分别代表矩形的一个角的顶点坐标,对角的顶点坐标-->
<area htef="链接" alt="备用内容" shape=“circle” coords="x,y,r">
<!--circle代表一个圆形区域,用三个逗号分隔的整数组成,分别圆心的坐标与圆的半径-->
<area htef="链接" shape=“poly” coords="x1,y1,x2,y2,x3,y3,...">
<!--poly代表一个多边形,包含至少六个逗号分隔的整数组成,每一对代表多边形的顶点-->
```

## html5中嵌入视频

```html
<video></video>		<!--视频创建属性-->
<video src="链接">	<!--src后面放入视频文件的链接-->
<video src="链接" height="长度" width=“宽度”>	
<!--height后面接视频的长度,width后面接视频的宽度-->
<video src="链接" autoplay>	<!--autoplay代表网页打开完成后自动播放视频-->
<video src="链接" autoplay muted>		
<!--muted表示播放视频时静音,由于谷歌浏览器,在不静音的情况下无法播放视频,所以需加上muted属性,右键视频显示控件,即可调节音量-->	
<video src="链接" controls>	<!--controls代表播放视频时显示视频控件-->
<video src="链接" controls preload="node">	
<!--preload属性为预先加载视频,后面的node代表不会载入-->
<video src="链接" controls preload="auto">
<!--auto代表缓存整个视频-->
<video src="链接" controls preload="metadata">
<!--metadata代表只下载第一帧-->
<video src="链接" loop>		<!--视频循环播放-->
<video src="链接" poster="链接">	<!--poster视频载入时显示图片,后面接图片链接-->
<video>
	<source src="链接" type=“video/类型”>	
<!--source元素设置视频格式,type后面接video/视频类型,例如:mp4,ogg.当video中的视频为浏览器不支持的视频格式时,跳转到source中播放视频-->    
</video>
```

