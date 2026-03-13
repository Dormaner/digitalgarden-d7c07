---
{"dg-publish":true,"permalink":"/前端/HTML+CSS+JS/"}
---

# 一、前端环境搭建

 1. 安装Vscode后，安装HTML CSS Support插件[00:02:21.928](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=2&time=00:02:21.928&app=jump-video-extension)，
 2. 安装Live Server插件[00:02:40.076](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=2&time=00:02:40.076&app=jump-video-extension)，这个插件的作用是实时预览页面（记住，只有在.html格式文件中，才能右键看到“Open With Live Server）
3. 安装Auto Rename Tag[00:03:03.710](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=2&time=00:03:03.710&app=jump-video-extension)，这个插件的作用是让我们在修改HTML标签的时候，同步修改与之匹配的另一个标签。
# 二、HTML

双标签用于有内容的元素，单标签用于没有内容的元素，比如分割线标签、换行标签等[00:01:38.698](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=3&time=00:01:38.698&app=jump-video-extension)
### 1、双标签

```html
<p>这是一个段落</p>
<h1>这是一个一级标题</h1>
<a href="#">这是一个超链接。</a>
```
### 2、单标签

```html
<input type = "text">
<br>
<hr>
```

### 3、HTML文件结构[00:02:10.687](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=3&time=00:02:10.687&app=jump-video-extension)和常用文本标签[00:00:37.603](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.videopod.episodesyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=4&time=00:00:37.603&app=jump-video-extension)


~~~html
<!-- 输入英文感叹号后按TAB键，就会自动生成基础的html目录结构： -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>这是一个测试</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <h2>这是一个二级标题</h2>
    <p>这是一个段落，用来测试HTML结构。</p>
    <p>我想进行<b>加粗</b>,<i>倾斜</i>、<u>下划线</u>、<s>删除线</s>等文字格式的测试。</p>
    <ul>
        <li>无序列表项 1</li>
        <li>无序列表项 2</li>
        <li>无序列表项 3</li>
    </ul>
    <ol>
        <li>有序列表项 1</li>
        <li>有序列表项 2</li>
        <li>有序列表项 3</li>
    </ol>
    <table>
        <!-- tr是table row的缩写，表示表格行 -->
        <!-- th是table header的缩写，表示表格的表头单元格 -->
        <!-- td是table data的缩写，表示表格的数据单元格 -->
        <tr>
            <th>表头 1</th>
            <th>表头 2</th>
            <th>表头 3</th>
        </tr>
        <tr>
            <td>数据 1</td>
            <td>数据 2</td>
            <td>数据 3</td>
        </tr>
    </table>
</body>
</html>
~~~

### 5、HTML标签属性[00:00:37.822](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.videopod.episodesyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=5&time=00:00:37.822&app=jump-video-extension)

~~~html
<开始标签 属性名=“属性值”>
<!-- 其中，属性名不区分大小写，属性值区分大小写 -->
~~~

class\id\style标签适用于大多数HTML元素的属性，其中class属性为HTML元素定义一个或多个类名，id属性定义元素唯一id，style规定了元素的行内样式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML 属性</title>
</head>
<body>
    <!-- a标签的 href 属性用于指定链接的目标地址。例如：
    a标签的 target 属性用于指定链接的打开方式。例如： -->
    <a href="https://www.example.com">这是一个链接</a>
    <br>
    <a href="https://www.example.com" target="_blank">在新标签页打开链接</a>
    <br>
    <!-- 由于目前我们的页面没有被嵌入到任何框架中，所以下面三个链接的效果与上面的相同： -->
    <a href="https://www.example.com" target="_parent">在父框架中打开链接</a>
    <br>
    <a href="https://www.example.com" target="_self">在当前框架中打开链接</a>
    <br>
    <a href="https://www.example.com" target="_top">在整个窗口中打开链接</a>
    <br>
    <!-- img标签的 src 属性用于指定图片的路径。alt 属性用于指定图片无法显示时的替代文本。例如： -->
    <img src="image.jpg" alt="该图片无法显示" width="200" height="150">
    
</body>
</html>
```
## 6、块元素与行内元素

```html
<!-- 块元素与行内元素
块元素是指那些在页面上独占一行，占据整个父元素宽度的HTML元素。常见的块元素有：<div>、<h1>到<h6>、<p>、<ul>、<ol>、<li>、<section>、<article>等。
行内元素是指那些不会独占一行，只占据其内容所需宽度的HTML元素。常见的行内元素有：<span>、<a>、<img>、<strong>、<em>等。 -->
<!-- 块元素可以包含其他块元素和行内元素，而行内元素通常只能包含文本或其他行内元素。块元素的默认宽度是其父元素的100%，可设置margin\padding等布局，而行内元素的宽度则由其内容决定，width和height属性通常不起作用。 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- div没有任何语义，只是用来组织内容而已 -->
     <!-- 下面创建一个导航栏 -->
    <div>
        <!-- a标签是行内元素，所以多个链接会排列在同一行： -->
        <a href="#">链接1</a>
        <a href="#">链接2</a>
        <a href="#">链接3</a>
    </div>
    <!-- 下面创建一个主要内容区域，如果确定了类名，可以通过快捷键div.content快速生成，如果确定了id，可以通过快捷键div#id名快速生成 -->
     <div class="content">
        <!-- h1、p是块元素，会独占一行 -->
        <h1>这是主要内容区域的标题</h1>
        <p>段落1</p>
        <p>段落2</p>
     </div>
     <!-- span标签是行内元素，不会换行，多个span标签会排列在同一行，你可以把span标签理解为一个小的容器，用来包裹一小段文本或其他行内元素，以便后续利用css进行样式设置或操作： -->
    <span>第一个span标签</span>
    <span>第二个span标签</span>
    <br>
    <span>这是嵌入链接的span标签，点击<a href="#">这里</a>进行跳转</span>
</body>
</html>
```
## 7、HTML表单

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- action属性指定表单数据提交的地址，一般是后端提供的url，这里先用#占位 -->
    <form action="#">
        <!-- span标签用来包裹文本或其他行内元素，用户输入的东西似乎无法提取？ -->
        <span>请输入用户名：</span>
        <input type="text" placeholder="请输入用户名：">
        <br><br>

        <!-- label标签可以通过for属性关联对应的输入框id，提高可访问性 -->
        <label for="pwd">请输入密码：</label>
        <input id="pwd" type="password" placeholder="请输入密码：">
        <br><br>

        <label >性别</label>
        <!-- 下面也可以写成<input type="radio">
        <label>男</label>，下面的更简化了 -->
        <!-- 加上了同一个name属性后，单选按钮才能互斥 -->
        <input type="radio" name="gender">男
        <input type="radio" name="gender">女
        <br><br>

        <input type="checkbox" name = "hobby">唱
        <input type="checkbox" name = "hobby">跳
        <input type="checkbox" name = "hobby">RAP
        <input type="checkbox" name = "hobby">篮球
        <br><br>

        <input type="submit" value="提交"> 
    </form>
    
</body>
</html>
```

# 三、CSS

HTML用来定义页面的结构和内容，CSS用来控制页面的外观和样式，通过CSS来指定页面中各个元素的颜色、字体、大小、间距、边框、背景等

## 1、CSS语法[00:01:41.094](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=8&time=00:01:41.094&app=jump-video-extension)

选择器 {
	属性1：属性值1；
	属性2：属性值2；
}
{ #f2ce64}

```css
p{
	 color: blue;
	 font-size:16px;
}
```

## 2、最小示例[00:02:56.723](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=8&time=00:02:56.723&app=jump-video-extension)
```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS样式</title>
    <style>
        /* 在这里写CSS样式 */
        p {
            color: blue;
            font-size: 28px;
        }
    </style>
</head>
<body>
    <p>这是一个段落。</p>
</body>
</html>
```

## 3、CSS三种导入方式[00:04:51.811](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=8&time=00:04:51.811&app=jump-video-extension)

- 内联样式：对每一个标签进行灵活控制
- 内部样式：统一页面中的元素样式，不推荐
- 外部样式：方便在多个页面使用同一种样式。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS样式</title>
    <!-- 把外部样式表链接进来 -->
    <link rel="stylesheet" href="./css/style.css">
    <style>
        /* 在这里写CSS样式 */
        p {
            color: blue;
            font-size: 28px;
        }
        h1 {
            color: green;
            font-size: 50px;
        }
    </style>
</head>
<body>
    <!-- 这是内联样式设置的段落：可以对每个标签进行控制 -->
    <p style="color: red;">这是使用内联样式的段落。</p>

    <!-- 这是内部样式设置的段落：会根据上面p标签的样式来显示 -->
    <p>这是使用内部样式的段落。</p>
    <h1>这也是使用内部样式的标题。</h1>

    <!-- 这是外部样式设置的标题：会根据css/style.css文件中的h3样式来显示 -->
    <h3>这是使用外部样式的标题。</h3>
</body>
</html>
```
> 三种导入方式的优先级：内联样式>内部样式表>外部样式表

外部链接的文件可以统一放在一个css文件夹中，在文件夹中新建一个名为style.css文件即可，文件内容如下

```css
h3 {
    color: purple;
    font-size: 24px;
}
```

## 4、选择器

选择器是CSS中的关键部分，它允许你针对特定元素或一组元素定义样式，上面我们已经应用了最普通的选择器[[前端/HTML+CSS+JS#^f2ce64\|#^f2ce64]]

- 元素选择器
- 类选择器
- ID选择器
- 通用选择器
- 子元素选择器
- 后代选择器（包含选择器）
- 并集选择器（兄弟选择器）
- 伪类选择器
~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    /* 控制所有h1元素颜色为蓝色 */
    h1 {
        color: blue;
    }

    /* 类选择器，控制类名称为highlight的元素颜色为红色 */
    .highlight {
        color: red;
    }

    /* ID选择器，控制ID名称为purple的元素颜色为紫色 */
    #purple {
        color: purple;
    }

    /* 通用选择器，控制所有元素的字体为Arial */
    * {
        font-family: Arial;
    }

    /* 子元素选择器,好像只选择儿子这一代。控制father类下的直接子元素son类的颜色为绿色 */
    .father > p.son {
        color: green;
    }

    /* 后代选择器，控制father类下的所有后代元素grandson类的颜色为橙色，无论是第几代都属于后代 */
    .father .grandson {
        color: orange;
    }

    /* 相邻选择器，选择紧接在h5后面的第一个p元素，设置颜色为棕色 */
    h5 + p {
        color: brown;
    }

    /* 伪类选择器，选择ID为element的元素的鼠标悬停状态，设置颜色为粉色 */
    #element:hover {
        color: pink;
    }
</style>
<body>
    <h1>普通的选择器测试</h1>

    <!-- 我想让类选择器测试1变成红色，但是类选择器测试2保持默认颜色，如果用普通的h2选择器的话就会都变成红色 -->
    <h2 class="highlight">类选择器测试1</h2>
    <h2>类选择器测试2</h2>

    <!-- 让ID选择器测试变成紫色： -->
    <h3 id="purple">ID选择器测试</h3>

    <h4>通用选择器测试</h4>

    <div class="father">
        <p class="son">子元素选择器测试</p>
        <div>
            <p class="grandson">后代选择器测试</p>
        </div>
        <p class="grandson">伪后代选择器测试</p>
    </div>

    <h5>相邻选择器测试</h5>
    <p>第一个段落。</p>
    <p>第二个段落。</p>

    <p id="element">伪类选择器测试</p>
    
</body>
</html>
~~~

## 5、CSS常用属性[00:00:01.202](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=10&time=00:00:01.202&app=jump-video-extension)

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
         /* 块级元素独占一行，可以设置宽高 */
        .myblock {
            width: 200px;
            height: 100px;
            background-color: lightblue;
        }
        /* 行内元素不会独占一行，宽高属性无效 */
        .myinline {
            background-color: lightgreen;
        }
        /* 既有块级元素特性又有行内元素特性的行内块元素，可以设置宽高 */
        .mylinline-block {
            width: 100px;
            height: 150px;
        }
        .div-inline {
            /* 下面这行代码将div标签转换为行内元素，这样它就不会独占一行了 */
            display: inline;
            background-color: lightyellow;
        }
        .span-block {
            /* 下面这行代码将span标签转换为块级元素，这样它就会独占一行了 */
            display: block;
            background-color: lightgray;
            width: 1000px;
            height: 100px;
        }
    </style>
</head>
<body>
    <h1 style="font: bolder 50px 'KaiTi';">这是一个font复合属性</h1>
     <!-- 也可以写成下面这样，就是太长了 -->
    <h1 style="font-weight: bolder; font-size: 50px; font-family: 'KaiTi';">这是一个font复合属性</h1>
    <p style="line-height: 50px;">段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试段落间距测试</p>

    <div class="myblock">这是一个块级元素</div>
    <span class="myinline">这是一个行内元素</span>
    <img src="./test.png" alt="" class="mylinline-block">
    <img src="./test.png" alt="" class="mylinline-block">
    <div class="div-inline">这是一个转成行内元素的div标签，它本来是块级元素</div>
    <span class="span-block">同理这是一个转成块级元素的span标签，它本来是行内元素，现在会独占一行，并且可以设置宽高</span>

</body>
</html>
~~~

## 6、盒子

![Pasted image 20251202142712.png](/img/user/image/Pasted%20image%2020251202142712.png)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .mydiv {
            display: inline-block;
            background-color: lightgray;
            
            /* 对左侧边框设置5像素宽的红色点状边框 */
            border-left: 5px dotted red;
            /* 对上侧边框设置8像素宽的绿色虚线边框,会覆盖上面的设置 */
            border: 10px solid blue;
            padding: 50px 20px 100px 0px; /* 内容距离上 右 下 左边框的数值 */
            margin: 100px; /* 距离周围元素100px */
        }
    </style>
</head>
<body>
    <div class="mydiv">这是一个段落测试</div>
</body>
</html>
```

## 7、浮动布局

- 标准布局：按照元素顺序从左到右、从上到下，前面的布局都是这样的
- 浮动布局：可以把盒子自定义地塞到上下左右的某一个方位
- 定位布局
- Flexbox和Grid（自适应布局）

浮动布局的语法如下
~~~html
选择器{
	float: left/right/none;
}
~~~

注意：浮动和inline-block行内块有点像，但是浮动只会在父元素内部进行，两个浮动盒子之间不存在间距，也就是margin，如果父元素第一行装不下的话，会自动放到第二行

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .father {
            /* height: 200px;如果不设置高度，父盒子高度会塌陷，出现布局错误 */
            background-color: lightgray;
            border: 1px solid black;
            overflow: hidden; /* 这一行代码是因为父盒子错误了，所以要清除浮动布局，回归标准布局 */
        }
        .leftson { 
            width: 100px;
            height: 100px;
            background-color: lightblue;
            float: left; /* 左浮动 */
        }
        .rightson {
            width: 100px;
            height: 100px;
            background-color: lightgreen;
            float: right; /* 右浮动 */
        }
    </style>
</head>
<body>
    <div class="father">
        <div class="leftson">左侧浮动盒子</div>
        <div class="rightson">右侧浮动盒子</div>
    </div>
    <p>这是一段文本</p>
    
</body>
</html>
~~~

## 8、定位布局

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1 {
            width: 700px;
            height: 350px;
            background-color: lightgray;
            position: relative; /* 使相对定位的子元素以此为定位参考（否则相对于页面） */
        }
        .box-normal {
            width: 100px;
            height: 100px;
            background-color: lightblue;
        }
        .box-relative {
            width: 100px;
            height: 100px;
            background-color: lightgreen;
            position: relative; /* 相对定位 */
            top: 20px; /* 向下移动20像素 */
            left: 50px; /* 向右移动50像素 */
        }

        .box2 {
            width: 700px;
            height: 350px;
            background-color: lightgray;
            position: relative; /* 使绝对定位的子元素以此为定位参考（否则相对于页面），如果不设置，绝对定位的子元素会相对于body定位，也就是跑到浏览器的左上角去了 */
        }
        .box-absolute {
            width: 100px;
            height: 100px;
            background-color: orange;
            position: absolute; /* 绝对定位 */
            top: 150px; /* 距离父盒子顶部150像素 */
            left: 300px; /* 距离父盒子左侧300像素 */
        }

        .box3 {
            width: 700px;
            height: 350px;
            background-color: rgb(192, 192, 192);
        }
        .box-fixed {
            width: 100px;
            height: 100px;
            background-color: red;
            position: fixed; /* 固定定位 */
            top: 50px; /* 距离浏览器窗口顶部50像素 */
            right: 50px; /* 距离浏览器窗口右侧50像素 */
        }
    </style>
</head>
<body>
    <!-- 相对定位是相对于它原来的位置进行偏移 -->
    <h1>相对定位</h1>
    <div class="box1">
        <div class="box-normal"></div>
        <div class="box-relative"></div>
        <div class="box-normal"></div>
    </div>

    <!-- 绝对定位是相对于它的最近的已定位祖先元素进行定位，如果没有已定位祖先元素，则相对于初始包含块（通常是文档的body）进行定位，这也是为啥上面.box2要设置position: relative的原因，否则.box-absolute会相对于body定位。 -->
    <h1>绝对定位</h1>
    <div class="box2">
        <div class="box-normal"></div>
        <!-- 一旦给这个盒子进行了绝对定位后，他就脱离了文档流，不占据空间了，所以后面的.box-normal会顶上来 -->
        <div class="box-absolute"></div>
        <div class="box-normal"></div>
    </div>

    <h1>固定定位</h1>
    <div class="box3">
        <div class="box-normal"></div>
        <div class="box-fixed"></div>
        <div class="box-normal"></div>
    </div>
</body>
</html>
~~~


## 四、Javascript

Javascript是一种脚本语言，主要用于在网页上实现动态效果，增加用户与网页的交互性。
## 1、JS的三种不同的导入方式

在浏览器中按下F12打开开发者工具的控制台（Console）标签页，可以看到三条日志输出，分别对应外部JS文件、head中的JS代码和body中的JS代码。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 导入外部JS文件 -->
    <script src="js/myjs.js"></script>
    <!-- 在head中直接写JS代码 -->
    <script>
        console.log("hello Head导入");
    </script>
</head>
<body>
    <!-- 在body中直接写JS代码 -->
    <script>
        console.log("hello Body导入");
    </script>
</body>
</html>

```

外部对应的JS文件如下
```javascript
console.log("hello 外部导入");
```

## 2、JS变量

其中最重要、最常用的就是let

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        // 在现在代JS中已经很少使用了，建议用let和const来声明变量
        var x;
        let y = "hello";
        const z = 10;
        let arr = [1, 2, 3];
        console.log(x, y, z, arr);
    </script>
</body>
</html>
```

## 3、条件判断与循环

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        let age = 66;
        if (age < 18) {
            alert("未成年");
        } 
        else if (age >= 18 && age < 60) {
            alert("成年人");
        }
        else {
            alert("老年人");
        }

        for (let i = 1; i <= 5; i++) {
            alert("当前是第 " + i + " 次for循环");
        }

        for (let i = 1; i <= 10; i++) {
            if (i == 2){
                continue; // 跳过本次循环,继续下一次循环
            }
            if (i == 5){
                break; // 终止整个循环
            } 
            alert("当前是第 " + i + " 次带“continue”、“break”的for循环");
        }

        let count = 1;
        while(count <= 5) {
            alert("当前是第 " + count + " 次while循环");
            count++;
        }
    </script>
</body>
</html>
```

## 3、函数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        // 函数示例
        function showMessage() {
            alert("Hello world!");
        }
        showMessage();

        function add(a, b) {
            return a + b;
        }
        alert("结果是：" + add(3, 5)); 
    </script>
</body>
</html>
```

## 4、事件

常用事件有： 
- onClick：点击事件
- onMouseOver：鼠标经过
- onMouseOut：鼠标移出
- onChange：文本内容改变
- onSelect：文本框选中
- onFocus：光标聚集
- onBlur：移开光标

JS绑定事件的方法有三种：
- HTML属性
- DOM属性
- addEventListener方法

下面这是用**HTML属性**绑定事件的方法
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button onclick="showMessage()">Click me</button>
    <!-- 一个输入框可以绑定多个事件。
    下面的输入框绑定了onfocus和onblur事件，点击到输入框触发事件，移动开触发另一个事件。 -->
    <input type="text" onfocus="focusInput()" onblur="blurInput()">
    <script>
        // 函数示例
        function showMessage() {
            alert("Hello world!");
        }

        function focusInput() {
            console.log("鼠标点击聚焦了");
        }

        function blurInput() {
            console.log("鼠标移开失焦了");
        }
    </script>
</body>
</html>
```

DOM的全称是“Doucument Object Model”，其实就是一个**实例化的文档对象**，我可以调用这个对象上的所有东西，比如这个网页对象上的按钮等。
就像Python中的对象拥有属于自己的方法一样，DOM对象常用的方法有下面几种
- appendChild()：把新的子节点添加到指定节点
- removeChild()：删除子节点
- replaceChild()：替换子节点
- insertBefore()：在指定的子节点前面插入新的子节点
- createAttribute()：创建属性节点
- createElement()：创建元素节点
- createTextNode：创建文本节点
- getAttribute()：返回指定的属性值
下面这是用**DOM属性**和**addEventListener方法**绑定事件的方法

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button id="myButton">box1</button>
    <button class="box2">box2</button>
    <button>box3</button>
    <script>
        // 通过id找到元素
        // 找到文档中名为myButton的按钮，并为它添加点击事件。
        var mybox1 = document.getElementById("myButton");
        mybox1.onclick = function() {
            alert("box1按钮被点击了！");
        };
        
        // 通过类名找到元素
        // 找到文档中第一个class名为box2的按钮，并为它添加点击事件。加[0]是因为getElementsByClassName返回的是一个数组，需要取第一个元素。
        var mybox2 = document.getElementsByClassName("box2")[0];
        mybox2.onclick = function() {
            alert("box2按钮被点击了！");
        };

        // 通过标签名找到元素
        // 找到文档中第三个button标签的按钮，并为它添加点击事件。加[2]是因为getElementsByTagName返回的是一个数组，索引从0开始。
        var mybox3 = document.getElementsByTagName("button")[2];
        // 为box3按钮添加双击事件，使用addEventListener方法，dblclick表示双击事件,此外还可以使用click、mouseover等事件类型
        mybox3.addEventListener("dblclick", function() {
            alert("box3按钮被点击了！（通过addEventListener添加的事件）");
        });

        // 获取元素之后，我们还可以修改元素的样式和内容
        mybox3.style.backgroundColor = "lightblue"; // 修改box3按钮的背景颜色为浅蓝色
        mybox3.innerHTML = "我是box3"; // 修改box3按钮的文本内容
        mybox3.innerText = "我是box3按钮"; // 修改box3按钮的文本内容

    </script>
</body>
</html>
```

## 5、表格的增删改查

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        h1 {
            color: blue;
            text-align: center;
        }
        table {
            width: 100%;
            border-collapse: collapse; /* 合并表格边框 */
            margin-top: 20px;
        }
        th, td {
            border: 1px solid black;
            text-align: center;
            padding: 8px;
        }
    </style>
    <script src="./js/table.js"></script>
</head>
<body>
    <h1>增删改查示例</h1>
    <button onclick="addRow()">新增数据</button>

    <!-- 设置id以便通过js获取这个table -->
    <table id ="data-table">
            <th>姓名</th>
            <th>联系方式</th>
            <th>操作</th>
        </tr>
        <tr>
            <td>张三</td>
            <td>1234567890</td>
            <td>
                <button onclick="editRow(this)">修改</button>
                <button onclick="deleteRow(this)">删除</button>
            </td>
        </tr>
    </table>

</body>
</html>
```

外部链接的JS文件如下

```javascript

function addRow() {
    let table = document.getElementById("data-table");

    console.log(table);
    let length = table.rows.length;
    let newRow = table.insertRow(length);
    let cellCount = table.rows[0].cells.length;

    for (let i = 0; i < cellCount; i++) {
        let cell = newRow.insertCell(i);
        // 最后一列是操作和删除按钮
        if (i === 0) {
            cell.placeholder = "";
        } 
        else if (i === 1){
            cell.placeholder = "";
        } 
        else if (i === 2) {
            cell.innerHTML = '<button onclick="editRow(this)">修改</button> <button onclick="deleteRow(this)">删除</button>';
        }
    }
}

function deleteRow(clickedButton) {
    // 现在我想删除用户点击删除按钮的那一行，怎么办？我又无法判断是第几行被点击了
    // 所以需要this这个关键字来获取被点击的按钮，然后获取它的父元素（所属cell)，再获取父元素的父元素(所属row），也就是行元素，然后通过row所属的table删除这一行（毕竟自己删除自己不太合理吧）
    // clickedButton 是被点击的按钮

    // 获取被点击按钮的那一行
    var row = clickedButton.parentNode.parentNode;
    // 删除这一行，不能自己删除自己，需要通过父元素也就是table来删除
    row.parentNode.removeChild(row);
}

function editRow(clickedButton) {
    var row = clickedButton.parentNode.parentNode;
    console.log(row);

    let nameCell = row.cells[0];
    let contactCell = row.cells[1];

    // 将单元格内容替换为输入框
    nameCell.innerHTML = prompt("请输入新的姓名：");
    contactCell.innerHTML = prompt("请输入新的联系方式：");
}
```

# 五、如何实现响应式布局

响应式布局，说人话就是，根据不同屏幕大小来显示网页，毕竟手机上、电脑的屏幕大小不一样。

方法1：通过rem、vw/vh等单位，实现在不同设备上显示相同比例进而实现适配

方法2：响应式布局，通过媒体查询@media实现一套HTML配合多套css实现适配（这句话我没有搞懂）


```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
```

在HTML的head标签中，width=device-width的意思是，视口的显示宽度为整个设备的宽度，并且初始缩放比例为1.0

在响应式网页与移动端进行布局的时候，推荐使用rem，而不是px。

rem是一个倍数单位，他是基于html标签中的font-size属性值的倍数。

只要我们在不同的设备上设置一个rem的初始值（一般默认是16px），当设备发生变化，font-size就会自动等比适配大小，从而在不同的设备上表现统一。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .px-box {
            width: 300px;
            height: 100px;
            background-color: lightcoral;
            margin-bottom: 20px;
        }
        .rem-box {
            width: 5rem; 
            height: 5rem; 
            background-color: lightseagreen;
        }
    </style>
</head>
<body>
    <div class="px-box"></div>
    <div class="rem-box"></div>

    <script>
        // 初始化根字体大小为视口宽度的十分之一
        function updateRemBox() {
            document.documentElement.style.fontSize = window.innerWidth / 10 + 'px';
        }
        updateRemBox();

        // 每次调整窗口大小时更新根字体大小
        window.addEventListener('resize', updateRemBox);
    </script>
</body>
</html>
```

# 六、Flex布局

采用Flex布局的元素，成为Flex容器（Flex container）。他的所有子元素自动成为容器成员，成为Flex项目（Flex item）
![Pasted image 20251203110856.png](/img/user/image/Pasted%20image%2020251203110856.png)

快速生成六个标签的快捷方式[00:05:14.035](jv://?url=https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switchyu26vd_source=53c0f374e323d05903a4520945a10be6yu26p=22&time=00:05:14.035&app=jump-video-extension)：`.item*6`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        html{
            font-size: 16px;
        }
        .container {
            display: flex;
            width: 20rem;
            height: 30rem;
            background-color: rgb(99, 99, 99);
            /* 盒子的排列方式为纵向排列、并翻转，此外还有colum（纵向排列)、row-reverse（横向排列翻转） */
            /* flex-direction: row; */
            /* 默认是不换行nowrap、从上到下换行wrap、从下到上换行wrap-reverse */
            flex-wrap: wrap;
            /* 盒子内部所有元素的排列方式，有中心对齐center、左对齐flex-start、右对齐flex-end、两端拉扯space-between */
            justify-content: space-evenly;
            /* 和justify-content一样，这个是纵向的，另外还有stretch拉伸、中心对齐center、左对齐flex-start、右对齐flex-end等 */
            align-items: center;
            /* 这是多行元素的居中显示，上面哪个align-item是单行元素的居中，你把元素变成两行之后，就能看出效果了。 */
            align-content: center;
        }
        .item {
            /* width: 7rem;总宽度超过了大盒子的20rem，会自动缩放 */
            display: flex;
            width: 7rem;
            height: 10rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="item" style="background-color: rgb(255, 255, 0);">1</div>
        <div class="item" style="background-color: rgb(43, 173, 75);">2</div>
        <div class="item" style="background-color: brown;">3</div>
    </div>
</body>
</html>
```

# 七、下一步学习

[[前端/React\|React]]
[[前端/Typescript\|Typescript]]
[[前端/Tailwind css\|Tailwind css]]
