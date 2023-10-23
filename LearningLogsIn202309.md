# 2023年9月后端开发学习日志

## 9月19日

下午，决定跟着黑马程序员的视频开发一个“苍穹外卖”项目，学完了视频当中的day01部分

## 9月20日

### 问题遗留：密码错误

在学习“swagger介绍和使用方式”时，在“接口测试：登录功能测试”部分输入正确密码和用户名依然显示密码错误，且未找到原因。

### 早上进度

学习到新增员工功能开发部分

### 问题遗留

在跟着视频开发“新增员工”功能时，由于“密码错误”的问题未解决，无法获得jwt令牌的token字符串（而jwt令牌相关知识技术自己并未接触了解过）

### 解决方案

决定学习B站黑马程序员的网课`Javaweb：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)黑马程序员2023新版JavaWeb开发教程，实现javaweb企业开发全流程（涵盖Spring+MyBatis+SpringMVC+SpringBoot等）`

1. 发现阅读课程资源的初始项目代码很困难，不能很好的理解项目架构，包结构,决定学习网课P75-P79"分层解耦"部分
2. 关于登录功能jwt令牌不了解的问题，计划学习网课P156-P170“登录案例实现”部分

### 最终决定

在看了两个B站黑马程序员关于“分层解耦”和“请求响应-案例实现”的视频后，最终还是决定先系统的学习`黑马程序员2023新版JavaWeb开发教程，实现javaweb企业开发全流程（涵盖Spring+MyBatis+SpringMVC+SpringBoot等）`课程后再继续开发苍穹外卖项目

## 9月21日

### Html语法特点

1. 不区分大小写
2. 语法结构松散，语法规则要求不严格

### VS Code

1. 全称Visual Studio Code
2. 一款微软开发的代码编辑器
3. 拥有非常强大的**插件库**（小巧、好用），大大提高了开发效率

### 开发软件安装目录tips

开发相关的软件尽量安装在一个没有中文、没有空格的目录下。

### 路径书写方式

1. 绝对路径：
   1. 绝对磁盘路径（C:/.../....）
   2. 绝对网络路径（http://.../...）
2. 相对路径：
   1. ./ ：表示当前目录，可省略不写
   2. ../：表示当前目录的上一级目录，不可省略

### 像素与分辨率

1. 像素：组成图片的不可分割的最基本的**点**

2. 分辨率：在长和宽两个方向上各拥有的**像素个数**（形如：640X480）

3. 每个像素的大小（即点的大小）主要取决于显示器的屏幕**尺寸**和屏幕**分辨率**，相同面积不同分辨率的显示屏，其像素点大小就不相同

4. 单位面积上像素点越多即像素点越小，这图片就越清晰细腻

5. 影像分辨率：每英寸长度上的像素点个数（一英寸就相当于**25.4毫米**），简称*PPI*（*pixeleperinch*英文缩写）

6. 同一张图片，在不同的*PPI*（影像分辨率）显示屏上其尺寸是不相同的，  **像素点的大小就和这个影像分辨率有关**

### 日志记录：适当的概念辨析与问题思考

为了解像素、分辨率和最终显示图片大小的关系，仔细阅读了csdn上一篇细致全面的关于像素、分辨率的博客

博客`像素是什么，一个像素有多大，像素和分辨率的关系(http://t.csdn.cn/csPKr)`

### 在Html中引入CSS样式

具体有3种引入方式，语法如下表格所示：

| 名称     | 语法描述                                          | 示例                                           |
| -------- | ------------------------------------------------- | ---------------------------------------------- |
| 行内样式 | 在标签内使用style属性，属性值是css属性键值对      | &lt;h1 style="xxx:xxx;">中国新闻网&lt;/h1>     |
| 内嵌样式 | 定义&lt;style&gt;标签，在标签内部定义css样式      | &lt;style> h1 {...} &lt;/style>                |
| 外联样式 | 定义&lt;link&gt;标签，通过href属性引入外部css文件 | &lt;link rel="stylesheet" href="css/news.css"> |

### 日志记录：未找到拾色器相关文件

- 在跟着黑马程序员视频学习"css样式-color"部分时，未在黑马程序员提供的资料中找到视频中所说的拾色器相关文件资源。
- 决定暂时先不纠结于寻找资料当中的拾色器

### CSS选择器

选择器：**选取需设置样式的元素（标签）**

**选择器通用语法如下**：

```css
选择器名   {
    css样式名：css样式值;
    css样式名：css样式值;
}
```

3种常用选择器是元素选择器，id选择器，class选择器

**1.元素（标签）选择器：** 

- 选择器的名字必须是标签的名字
- 作用：选择器中的样式会作用于所有同名的标签上

~~~
元素名称 {
    css样式名:css样式值；
}
~~~

例子如下：

~~~css
 div{
     color: red;
 }
~~~



**2.id选择器:**

- 选择器的名字前面需要加上#
- 作用：选择器中的样式会作用于指定id的标签上，而且有且只有一个标签（由于id是唯一的）

~~~
#id属性值 {
    css样式名:css样式值；
}
~~~

例子如下：

~~~css
#did {
    color: blue;
}
~~~



**3.类选择器：**

- 选择器的名字前面需要加上 .
- 作用：选择器中的样式会作用于所有class的属性值和该名字一样的标签上，可以是多个

~~~
.class属性值 {
    css样式名:css样式值；
}
~~~

例子如下：

~~~css
.cls{
     color: green;
 }
~~~

### 超链接

- 标签: &lt;a href="..." target="...">央视网</a>
- 属性:
  - href: 指定资源访问的url
  - target: 指定在何处打开资源链接
    - _self: 默认值，在当前页面打开
    - _blank: 在空白页面打开

```
<a href="http://www.baidu.com" target="_blank">百度一下</a>
```

### 视频、音频标签

- 视频标签: &lt;video>
  - 属性: 
    - src: 规定视频的url
    - controls: 显示播放控件
    - width: 播放器的宽度
    - height: 播放器的高度

- 音频标签: &lt;audio>
  - 属性:
    - src: 规定音频的url
    - controls: 显示播放控件

### 下午学习记录

13：00开始在图书馆学习，17.00下班干饭！！！

### 晚饭后记录实况

本来想着干完饭后，回到图书馆继续跟着黑马程序员的视频嘎嘎猛学，结果干完饭后相当萎靡，太虚啦！！！太虚啦！！！

于是，在走廊做完了游戏《崩坏：星琼铁道》的日常，状态好了一丢丢！！！

### 网页布局-盒子模型

- 盒子：页面中所有的元素（标签），都可以看做是一个 盒子，由盒子将页面中的元素包含在一个矩形区域内，通过盒子的视角更方便的进行页面布局

- 盒子模型组成：内容区域（content）、内边距区域（padding）、边框区域（border）、外边距区域（margin）

<img src="D:\桌面\NewLearner\后端开发学习日志\img\image-20231023183626631.png" alt="image-20230310092820616" style="zoom:80%;" /> 

**注：注意体会盒子模型中的工程师思维**

### 盒子模型中常用的布局标签

- 标签：<div> <span> （均没有语义）

- 特点：

  - div标签：

    - 一行只显示一个（独占一行）

    - 宽度默认是父元素的宽度，高度默认由内容撑开

    - 可以设置宽高（width、height）

  - span标签：

    - 一行可以显示多个

    - 宽度和高度默认由内容撑开

    - 不可以设置宽高（width、height）

### 表格标签

#### 标签

- &lt;table> : 用于定义整个表格, 可以包裹多个 &lt;tr>， 常用属性如下： 
  - border：规定表格边框的宽度
  - width：规定表格的宽度
  - cellspacing: 规定单元之间的空间

- &lt;tr> : 表格的行，可以包裹多个 &lt;td>  
- &lt;td> : 表格单元格(普通)，可以包裹内容 , 如果是表头单元格，可以替换为 &lt;th>  



#### 示例

代码如下：

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML-表格</title>
    <style>
        td {
            text-align: center; /* 单元格内容居中展示 */
        }
    </style>
</head>
<body>
    
    <table border="1px" cellspacing="0"  width="600px">
        <tr>
            <th>序号</th>
            <th>品牌Logo</th>
            <th>品牌名称</th>
            <th>企业名称</th>
        </tr>
        <tr>
            <td>1</td>
            <td> <img src="img/huawei.jpg" width="100px"> </td>
            <td>华为</td>
            <td>华为技术有限公司</td>
        </tr>
        <tr>
            <td>2</td>
            <td> <img src="img/alibaba.jpg"  width="100px"> </td>
            <td>阿里</td>
            <td>阿里巴巴集团控股有限公司</td>
        </tr>
    </table>

</body>
</html>
~~~

打开浏览器，效果如下图所示：

![image-20230309175121361](.\img\image-20230309175121361.png)



整合表格使用 table 标签包裹 , 其中的每一行数据都是一个 tr , 每一行中的每一个单元格都是一个 td , 而如果是表头单元格, 可以使用 th (具有加粗居中展示的效果)。

### 表单标签

- 表单场景: 表单就是在网页中负责数据采集功能的，如：注册、登录的表单。 

- 表单标签: &lt;form>
- 表单属性:
  - action: 规定表单提交时，向何处发送表单数据，表单提交的URL。
  - method: 规定用于发送表单数据的方式，常见为： GET、POST。
    - GET：表单数据是拼接在url后面的， 如： xxxxxxxxxxx?username=Tom&age=12，url中能携带的表单数据大小是有限制的。
    - POST： 表单数据是在请求体（消息体）中携带的，大小没有限制。

- 表单项标签: 不同类型的input元素、下拉列表、文本域等。
  - input: 定义表单项，通过type属性控制输入形式
  - select: 定义下拉列表
  - textarea: 定义文本域





##### 示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML-表单</title>
</head>
<body>
    <!-- 
    form表单属性: 
        action: 表单提交的url, 往何处提交数据 . 如果不指定, 默认提交到当前页面
        method: 表单的提交方式 .
            get: 在url后面拼接表单数据, 比如: ?username=Tom&age=12 , url长度有限制 . 默认值
            post: 在消息体(请求体)中传递的, 参数大小无限制的.
    -->   
	
    <form action="" method="get">
        用户名: <input type="text" name="username">
        年龄: <input type="text" name="age">

        <input type="submit" value="提交">
    </form>
	
</body>
</html>
```



表单编写完毕之后，通过浏览器打开此表单，然后再表单项中录入值之后，点击提交，我们会看到表单的数据在url后面提交到服务端，格式为：?username=Tom&age=12。

表单中的所有表单项，要想能够正常的采集数据，在提交的时候能提交到服务端，表单项必须指定**name属性**。 否则，无法提交该表单项。

```html
用户名: <input type="text" name="username">
```

### 表单项

在一个表单中，可以存在很多的表单项，而虽然表单项的形式各式各样，但是表单项的标签其实就只有三个，分别是：

- &lt;input>: 表单项 , 通过type属性控制输入形式。

  | type取值                 | **描述**                             |
  | ------------------------ | ------------------------------------ |
  | text                     | 默认值，定义单行的输入字段           |
  | password                 | 定义密码字段                         |
  | radio                    | 定义单选按钮                         |
  | checkbox                 | 定义复选框                           |
  | file                     | 定义文件上传按钮                     |
  | date/time/datetime-local | 定义日期/时间/日期时间               |
  | number                   | 定义数字输入框                       |
  | email                    | 定义邮件输入框                       |
  | hidden                   | 定义隐藏域                           |
  | submit / reset / button  | 定义提交按钮 / 重置按钮 / 可点击按钮 |

- &lt;select>: 定义下拉列表, &lt;option> 定义列表项

- &lt;textarea>: 文本域

### 示例

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML-表单项标签</title>
</head>
<body>

<!-- value: 表单项提交的值 -->
<form action="" method="post">
     姓名: <input type="text" name="name"> <br><br>
     密码: <input type="password" name="password"> <br><br> 
     性别: <input type="radio" name="gender" value="1"> 男
          <label><input type="radio" name="gender" value="2"> 女 </label> <br><br>
     爱好: <label><input type="checkbox" name="hobby" value="java"> java </label>
          <label><input type="checkbox" name="hobby" value="game"> game </label>
          <label><input type="checkbox" name="hobby" value="sing"> sing </label> <br><br>
     图像: <input type="file" name="image">  <br><br>
     生日: <input type="date" name="birthday"> <br><br>
     时间: <input type="time" name="time"> <br><br>
     日期时间: <input type="datetime-local" name="datetime"> <br><br>
     邮箱: <input type="email" name="email"> <br><br>
     年龄: <input type="number" name="age"> <br><br>
     学历: <select name="degree">
               <option value="">----------- 请选择 -----------</option>
               <option value="1">大专</option>
               <option value="2">本科</option>
               <option value="3">硕士</option>
               <option value="4">博士</option>
          </select>  <br><br>
     描述: <textarea name="description" cols="30" rows="10"></textarea>  <br><br>
     <input type="hidden" name="id" value="1">
	 	
     <!-- 表单常见按钮 -->
     <input type="button" value="按钮">
     <input type="reset" value="重置"> 
     <input type="submit" value="提交">   
     <br>
</form>

</body>
</html>
```

### 下班

20：05今天的Javaweb工程开发部分结束liao

总体而言，使用日志形式记录下自己的开发和学习过程是有益的，值得尝试一段时间

计划将日志类md文档发到GitHub、Gitee上

## 9月23日 周六

### 中午，下午学习记录

#### JavaScript引入方式

**第一种方式：**内部脚本，将JS代码定义在HTML页面中

- JavaScript代码必须位于&lt;script&gt;&lt;/script&gt;标签之间
- 在HTML文档中，可以在任意地方，放置任意数量的&lt;script&gt;
- 一般会把脚本置于&lt;body&gt;元素的底部，可改善显示速度

例子：

~~~html
<script>
    alert("Hello JavaScript")
</script>
~~~



**第二种方式：**外部脚本将， JS代码定义在外部 JS文件中，然后引入到 HTML页面中

- 外部JS文件中，只包含JS代码，不包含script标签
- 引入外部js的&lt;script&gt;标签，必须是**双标签**

例子：

~~~html
<script src="js/demo.js"></script>
~~~

注意：demo.js中只有js代码，没有&lt;script&gt;标签

#### JavaScript输出语句

常用的3种Js输出语句如下：

| api              | 描述             |
| ---------------- | ---------------- |
| window.alert()   | 警告框           |
| document.write() | 在HTML 输出内容  |
| console.log()    | 写入浏览器控制台 |

#### JavaScript变量

JavaScript是弱类型语言，常用以下3个关键字声明变量

| 关键字 | 解释                                                         |
| ------ | ------------------------------------------------------------ |
| var    | 声明**全局变量**                                             |
| let    | 声明**代码块变量**，只在代码块内生效，常用于声明**局部变量** |
| const  | 声明**常量**，常量一旦声明，不能修改                         |

#### 数据类型和运算符

js中的数据类型分为 ：**原始类型** 和 **引用类型**，具体有如下类型

| 数据类型  | 描述                                               |
| --------- | -------------------------------------------------- |
| number    | 数字（整数、小数、NaN(Not a Number)）              |
| string    | 字符串，单双引皆可                                 |
| boolean   | 布尔。true，false                                  |
| null      | 对象为空                                           |
| undefined | 当声明的变量未初始化时，该变量的默认值是 undefined |

使用**typeof函数**可以返回变量的数据类型

js中的运算规则绝大多数还是和java中一致的，具体运算符如下：

| 运算规则   | 运算符                                                       |
| ---------- | ------------------------------------------------------------ |
| 算术运算符 | + , - , * , / , % , ++ , --                                  |
| 赋值运算符 | = , += , -= , *= , /= , %=                                   |
| 比较运算符 | &gt; , < , >= , <= , != , == , ===   **注意     == 会进行类型转换，=== 不会进行类型转换** |
| 逻辑运算符 | && , \|\| , !                                                |
| 三元运算符 | 条件表达式 ? true_value: false_value                         |

### 下班

今天是周六，决定好好休息，好好玩，保持活力

13：50下班

## 9月25日 周一

### 早上，学习记录

#### JavaScript函数的两种定义方式

方式一：

```
function 函数名(参数1,参数2..){
    要执行的代码
}
```

示例：

```
function add(a, b){
    return a + b;
}
```

方式二：

```
var functionName = function (参数1,参数2..){   
	//要执行的代码
}
```

示例：

```
   	var add = function(a,b){
        return  a + b;
    }
```

#### JavaScript对象

##### 基本对象：Array、JSON、String

###### Array

Array对象是用来定义数组的

定义方式一：

```
var 变量名 = new Array(元素列表); 
var arr = new Array(1,2,3,4); //1,2,3,4 是存储在数组中的数据（元素）
```

定义方式二：

```
var 变量名 = [ 元素列表 ]; 
var arr = [1,2,3,4]; //1,2,3,4 是存储在数组中的数据（元素）
```

**注：JavaScript中数组的长度是可变的，并且可以存储任意类型的值**

属性和方法

属性：

| 属性   | 描述                         |
| :----- | :--------------------------- |
| length | 设置或返回数组中元素的数量。 |

方法：

| 方法方法  | 描述                                                 |
| :-------- | :--------------------------------------------------- |
| forEach() | 遍历数组中的每个**有值的元素**，并调用一次传入的函数 |
| push()    | 将新元素添加到数组的末尾，并返回新的长度             |
| splice()  | 从数组中删除元素                                     |

forEach()函数

~~~js
//e是形参，接受的是数组遍历时的值
arr.forEach(function(e){
     console.log(e);
})
~~~

当然了，在ES6中，引入箭头函数的写法，语法类似java中lambda表达式，修改上述代码如下：

~~~js
arr.forEach((e) => {
     console.log(e);
}) 
~~~

###### String

两种定义方式：

方式一：

```
var 变量名 = new String("…") ; //方式一
var str = new String("Hello String");
```

方式二：

```
var 变量名 = "…" ; //方式二
var str = "Hello String";
```

属性和方法

属性：

| 属性   | 描述           |
| ------ | -------------- |
| length | 字符串的长度。 |

方法：

| 方法        | 描述                                     |
| ----------- | ---------------------------------------- |
| charAt()    | 返回在指定位置的字符。                   |
| indexOf()   | 检索字符串。                             |
| trim()      | 去除字符串两边的空格                     |
| substring() | 提取字符串中两个指定的索引号之间的字符。 |

###### Json

JSON对象：**J**ava**S**cript **O**bject **N**otation，JavaScript对象标记法。是通过JavaScript标记法书写的文本。其格式如下：

```
{
    "key":value,
    "key":value,
    "key":value
}
```

**key必须使用引号并且是双引号标记，value可以是任意数据类型。**

那么json这种数据格式的文本到底应用在企业开发的什么地方呢？-- **经常用来作为前后台交互的数据载体**

使用示例：

```
    // 定义json字符串
    var jsonstr = '{"name":"Tom", "age":18, "addr":["北京","上海","西安"]}';
	alert(jsonstr);
	
    // 将json字符串转换为json对象
    var obj = JSON.parse(jsonstr);
    alert(obj.name);

    // 将json对象转换为json字符串
    alert(JSON.stringify(obj));
```

附：JavaScript自定义对象

```
    var user = {
        name: "Tom",
        age: 10,
        gender: "male",
        // eat: function(){
        //      console.log("用膳~");
        //  }
        eat(){
            console.log("用膳~");
        }
    }
```

##### Bom对象

BOM：Browser Object Model,浏览器对象模型

BOM中提供了如下5个对象：

| 对象名称  | 描述           |
| :-------- | :------------- |
| Window    | 浏览器窗口对象 |
| Navigator | 浏览器对象     |
| Screen    | 屏幕对象       |
| History   | 历史记录对象   |
| Location  | d地址栏对象    |

上述5个对象与浏览器各组成对应的关系如下图所示：

![](D:\桌面\NewLearner\后端开发学习日志\img\image-20210815194911914.png)

###### Window对象

Window对象：浏览器窗口对象。

window对象提供了获取其他BOM对象的属性：

| 属性      | 描述                  |
| --------- | --------------------- |
| history   | 用于获取history对象   |
| location  | 用于获取location对象  |
| Navigator | 用于获取Navigator对象 |
| Screen    | 用于获取Screen对象    |

window也提供了一些常用的函数，如下表格所示：

| 函数          | 描述                                               |
| ------------- | -------------------------------------------------- |
| alert()       | 显示带有一段消息和一个确认按钮的警告框。           |
| comfirm()     | 显示带有一段消息以及确认按钮和取消按钮的对话框。   |
| setInterval() | 按照指定的周期（以毫秒计）来调用函数或计算表达式。 |
| setTimeout()  | 在指定的毫秒数后调用函数或计算表达式。             |

示例：

```
//定时器 - setInterval -- 周期性的执行某一个函数
var i = 0;
setInterval(function(){
     i++;
     console.log("定时器执行了"+i+"次");
},2000);
```

结果如下：

![1668795435780](D:\桌面\NewLearner\后端开发学习日志\img\1668795435780.png) 

###### Location对象

Location：浏览器的地址栏对象

常用Location的href属性，用于获取或者设置浏览器的地址信息

~~~js
//获取浏览器地址栏信息
alert(location.href);
//设置浏览器地址栏信息
location.href = "https://www.itcast.cn";
~~~

### 早上，下班

9：25-11：25学习

下班，干饭！！！

### 中午，下午，学习记录

#### Dom对象

DOM：Document Object Model **文档对象模型**。也就是 JavaScript 将 HTML 文档的各个组成部分封装为对象。

HTML 文档是浏览器解析。封装的对象分为

- Document：整个文档对象
- Element：元素对象
- Attribute：属性对象
- Text：文本对象
- Comment：注释对象

如下图，左边是 HTML 文档内容，右边是 DOM 树

![1668796698067](D:\桌面\NewLearner\后端开发学习日志\img\1668796698067.png)

##### 获取Dom对象

document对象提供的用于获取Element元素对象的api如下表所示：

| 函数                              | 描述                                     |
| --------------------------------- | ---------------------------------------- |
| document.getElementById()         | 根据id属性值获取，返回单个Element对象    |
| document.getElementsByTagName()   | 根据标签名称获取，返回Element对象数组    |
| document.getElementsByName()      | 根据name属性值获取，返回Element对象数组  |
| document.getElementsByClassName() | 根据class属性值获取，返回Element对象数组 |

##### 设置或修改标签内容

```
var divs = document.getElementsByClassName('cls');
var div1 = divs[0];

div1.innerHTML = "传智教育666";
```

浏览器刷新页面，展示效果如下图所示：

![1668800387791](D:/BaiduNetdiskDownload/2023JavawebStudy/day02-JavaScript-Vue/讲义/assets/1668800387791.png) 

发现页面内容变成了传智教育666

##### 提高自己解决问题的能力

学会使用搜索引擎、官方技术文档

#### JavaScript事件

事件：

HTML事件是发生在HTML元素上的 “事情”，例如：

- 按钮被点击

- 鼠标移到元素上

- 输入框失去焦点

- ........

##### 事件绑定方式 

方式1：通过html标签中的事件属性进行绑定

```
<input type="button" id="btn1" value="事件绑定1" onclick="on()">

<script>
    function on(){
        alert("按钮1被点击了...");
    }
</script>
```

方式2：通过DOM中Element元素的事件属性进行绑定

```
<input type="button" id="btn2" value="事件绑定2">

document.getElementById('btn2').onclick = function(){
    alert("按钮2被点击了...");
}
```

**需要注意的是：事件绑定的函数，只有在事件被触发时，函数才会被调用。**

#### 下班

12：35-15：00学完了JavaScript剩下部分的学习内容。

下班！！！

## 9月26日 周二

### 下午学习记录

14：00开始上班

#### MVVM

MVVM(Model-View-ViewModel)具体释义如下：

- Model: **数据模型**，特指前端中通过请求从后台获取的数据
- View: **视图**，用于展示数据的页面，可以理解成我们的html+css搭建的页面，但是没有数据
- ViewModel: **数据绑定到视图**，负责将数据（Model）通过JavaScript的DOM技术，将数据展示到视图（View）上

如图所示就是MVVM开发思想的含义：

![1668857055058](D:\桌面\NewLearner\后端开发学习日志\img\1668857055058.png)



#### Vue的基础使用示例

在创建vue对象时，有几个常用的属性：

- el:  用来指定哪儿些标签受 Vue 管理。 该属性取值 `#app` 中的 `app` 需要是受管理的标签的id属性值
- data: 用来定义数据模型
- methods: 用来定义函数

在html区域编写视图，其中{{}}是插值表达式，用来将vue对象中定义的model展示到页面上的

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue-快速入门</title>
    <script src="js/vue.js"></script>
</head>
<body>

    <div id="app">
        <input type="text" v-model="message">
        {{message}}
    </div>

</body>
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
            message: "Hello Vue"
        }
    })
</script>
</html>
```

#### Vue的常用指令

Vue指令：HTML 标签上带有 v- 前缀的特殊属性，不同指令具有不同含义。

vue的常用指令，如下表所示：

| **指令**  | **作用**                                            |
| --------- | --------------------------------------------------- |
| v-bind    | 为HTML标签绑定属性值，如设置  href , css样式等      |
| v-model   | 在表单元素上创建双向数据绑定                        |
| v-on      | 为HTML标签绑定事件                                  |
| v-if      | 条件性的渲染某元素，判定为true时渲染,否则不渲染     |
| v-else    |                                                     |
| v-else-if |                                                     |
| v-show    | 根据条件展示某元素，区别在于切换的是display属性的值 |
| v-for     | 列表渲染，遍历容器的元素或者对象的属性              |

##### v-bind和v-model

| **指令** | **作用**                                       |
| -------- | ---------------------------------------------- |
| v-bind   | 为HTML标签绑定属性值，如设置  href , css样式等 |
| v-model  | 在表单元素上创建双向数据绑定                   |

**v-bind**:  为HTML标签绑定属性值，如设置  href , css样式等。当vue对象中的数据模型发生变化时，标签的属性值会随之发生变化。

我们需要给&lt;a&gt;标签的href属性赋值，并且值应该来自于vue对象的数据模型中的url变量。所以编写如下代码：

```
<a v-bind:href="url">链接1</a>
```

在上述的代码中，v-bind指令是可以省略的，但是:不能省略，所以第二个超链接的代码编写如下：

```
<a :href="url">链接2</a>
```

**v-model**： 在表单元素上创建双向数据绑定。什么是双向？

-  vue对象的data属性中的数据变化，视图展示会一起变化
-  视图数据发生变化，vue对象的data属性中的数据也会随着变化。

v-bind和v-model使用示例：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue-指令-v-bind</title>
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        <a v-bind:href="url">链接1</a>
        <a :href="url">链接2</a>

        <input type="text" v-model="url">

    </div>
</body>
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
           url: "https://www.baidu.com"
        }
    })
</script>
</html>
```

**注意**：当使用v-bind或v-model绑定**特定属性**后，后面一定要在data域中设置该**特定属性**，例如上面的示例代码中一定要在data域中设置url

**注意**：当在data域中设置多个属性值时，要用英文逗号隔开(有憨憨在这个点上Debug了半天)

##### v-on

v-on: 用来给html标签绑定事件的。

**需要注意的是如下2点**：

- v-on语法给标签的事件绑定的函数，必须是vue对象中声明的函数

- v-on语法绑定事件时，事件名相比较js中的事件名，没有on

- 例如：在js中，事件绑定demo函数

  ~~~html
  <input onclick="demo()">
  ~~~

  vue中，事件绑定demo函数

  ~~~html
  <input v-on:click="demo()">
  ~~~

示例代码：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue-指令-v-on</title>
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

        <input type="button" value="点我一下" v-on:click="handle()">

        <input type="button" value="点我一下" @click="handle()">

    </div>
</body>
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
           
        },
        methods: {
            handle: function(){
                alert("你点我了一下...");
            }
        }
    })
</script>
</html>
```

#### v-if和v-show

| 指令      | 描述                                                |
| --------- | --------------------------------------------------- |
| v-if      | 条件性的渲染某元素，判定为true时渲染,否则不渲染     |
| v-if-else |                                                     |
| v-else    |                                                     |
| v-show    | 根据条件展示某元素，区别在于切换的是display属性的值 |

示例代码：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue-指令-v-if与v-show</title>
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">
        
        年龄<input type="text" v-model="age">经判定,为:
        <span v-if="age <= 35">年轻人(35及以下)</span>
        <span v-else-if="age > 35 && age < 60">中年人(35-60)</span>
        <span v-else>老年人(60及以上)</span>

        <br><br>

        年龄<input type="text" v-model="age">经判定,为:
        <span v-show="age <= 35">年轻人(35及以下)</span>
        <span v-show="age > 35 && age < 60">中年人(35-60)</span>
        <span v-show="age >= 60">老年人(60及以上)</span>

    </div>
</body>
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
           age: 20
        },
        methods: {
            
        }
    })
</script>
</html>
```

**v-if和v-show的区别：**虽然浏览器呈现的效果是一样的，但是浏览器中html源码不一样。v-if指令，不满足条件的标签代码直接没了，而v-show指令中，不满足条件的代码依然存在，只是添加了css样式来控制标签不去显示。

##### v-for

v-for: 从名字我们就能看出，这个指令是用来遍历的。其语法格式如下：

~~~html
<标签 v-for="变量名 in 集合模型数据">
    {{变量名}}
</标签>
~~~

需要注意的是：需要循环那个标签，v-for 指令就写在那个标签上。

有时我们遍历时需要使用索引，那么v-for指令遍历的语法格式如下：

~~~html
<标签 v-for="(变量名,索引变量) in 集合模型数据">
    <!--索引变量是从0开始，所以要表示序号的话，需要手动的加1-->
   {{索引变量 + 1}} {{变量名}}
</标签>
~~~

接下来，我们在VS Code中创建名为16. Vue-指令-v-for.html的文件编写代码演示，提前准备如下代码：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue-指令-v-for</title>
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">

    </div>
</body>
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
           addrs:["北京", "上海", "西安", "成都", "深圳"]
        },
        methods: {
            
        }
    })
</script>
</html>
```

然后分别编写2种遍历语法，来遍历数组，展示数据，代码如下：

~~~html
 <div id="app">
     <div v-for="addr in addrs">{{addr}}</div>
     <hr>
     <div v-for="(addr,index) in addrs">{{index + 1}} : {{addr}}</div>
</div>
~~~

浏览器打开，呈现如下效果：

![1668866805981](D:\桌面\NewLearner\后端开发学习日志\img\1668866805981.png) 

##### Vue的生命周期

**vue的生命周期：指的是vue对象从创建到销毁的过程。**vue的生命周期包含8个阶段：每触发一个生命周期事件，会自动执行一个生命周期方法，这些生命周期方法也被称为**钩子方法**。其完整的生命周期如下图所示：

| 状态          | 阶段周期 |
| ------------- | -------- |
| beforeCreate  | 创建前   |
| created       | 创建后   |
| beforeMount   | 挂载前   |
| mounted       | 挂载完成 |
| beforeUpdate  | 更新前   |
| updated       | 更新后   |
| beforeDestroy | 销毁前   |
| destroyed     | 销毁后   |

对于后端开发，我们需要重点关注的是**mounted

**mounted：**挂载完成，Vue初始化成功，HTML页面渲染成功。**mounted一般用于页面初始化自动的ajax请求后台数据**

示例：

我们编写mounted声明周期的钩子函数，与methods同级，代码如下：

~~~html
<script>
    //定义Vue对象
    new Vue({
        el: "#app", //vue接管区域
        data:{
           
        },
        methods: {
            
        },
        mounted () {
            alert("vue挂载完成,发送请求到服务端")
        }
    })
</script>
~~~

浏览器打开，运行结果如下：我们发现，自动打印了这句话，因为页面加载完成，vue对象创建并且完成了挂载，此时自动触发mounted所绑定的钩子函数，然后自动执行，弹框。

![1668867458156](D:/BaiduNetdiskDownload/2023JavawebStudy/day02-JavaScript-Vue/讲义/assets/1668867458156.png) 

#### 下班

16：30下班啦！！！

## 9月28日 周四

### 中午，下午，学习记录

饭后，清了游戏崩坏星穹铁道的日常。12:45开始学习。

#### Ajax

Ajax: 全称Asynchronous JavaScript And XML，异步的JavaScript和XML

Ajax的作用：

- **与服务器进行数据交换**：通过Ajax可以给服务器发送请求，并获取服务器响应的数据。
- **异步交互**：可以在**不重新加载整个页面**的情况下，与服务器交换数据并**更新部分网页**的技术，如：搜索联想、用户名是否可用的校验等等。

##### 同步请求和异步请求

- **同步请求**：浏览器页面在发送请求给服务器，在服务器处理请求的过程中，**浏览器页面不能做其他的操作**。只能等到服务器响应结束后才能，浏览器页面才能继续做其他的操作。 
- **异步请求**：浏览器页面发送请求给服务器，在服务器处理请求的过程中，浏览器页面还可以做其他的操作。

#### Axios

原生的Ajax请求的代码编写起来还是比较繁琐的，**Axios**是对原生的AJAX进行封装，简化书写。Axios官网是：`https://www.axios-http.cn`

##### Axios的基本使用

Axios的使用比较简单，主要分为2步：

- 引入Axios文件

  ~~~html
  <script src="js/axios-0.18.0.js"></script>
  ~~~

- 使用Axios发送请求，并获取响应结果，官方提供的api很多，此处给出2种，如下

  - 发送 get 请求

    ~~~js
    axios({
        method:"get",
        url:"http://localhost:8080/ajax-demo1/aJAXDemo1?username=zhangsan"
    }).then(function (resp){
        alert(resp.data);
    })
    ~~~

  - 发送 post 请求

    ```js
    axios({
        method:"post",
        url:"http://localhost:8080/ajax-demo1/aJAXDemo1",
        data:"username=zhangsan"
    }).then(function (resp){
        alert(resp.data);
    });
    ```

  axios()是用来发送异步请求的，小括号中使用 js的JSON对象传递请求相关的参数：

  - **method**属性：用来设置请求方式的。取值为 get 或者 post。
  - **url**属性：用来书写请求的资源路径。如果是 get 请求，需要将请求参数拼接到路径的后面，格式为： url?参数名=参数值&参数名2=参数值2。
  - **data**属性：作为请求体被发送的数据。也就是说如果是 post 请求的话，数据需要作为 data 属性的值。

  then() 需要传递一个匿名函数。我们将 then()中传递的匿名函数称为 **回调函数**，意思是该匿名函数在发送请求时不会被调用，而是在成功响应后调用的函数。而该回调函数中的 resp 参数是对响应的数据进行封装的对象，通过 resp.data 可以获取到响应的数据。

**Axios请求方法的别名**

Axios还针对不同的请求，提供了别名方式的api,具体如下：

| 方法                               | 描述           |
| ---------------------------------- | -------------- |
| axios.get(url [, config])          | 发送get请求    |
| axios.delete(url [, config])       | 发送delete请求 |
| axios.post(url [, data[, config]]) | 发送post请求   |
| axios.put(url [, data[, config]])  | 发送put请求    |

我们目前只关注get和post请求，所以在上述的入门案例中，我们可以将get请求代码改写成如下：

~~~js
axios.get("http://yapi.smart-xwork.cn/mock/169327/emp/list").then(result => {
    console.log(result.data);
})
~~~

post请求改写成如下：

~~~js
axios.post("http://yapi.smart-xwork.cn/mock/169327/emp/deleteById","id=1").then(result => {
    console.log(result.data);
})
~~~

#### Vue和Axios结合使用案例

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ajax-Axios-案例</title>
    <script src="js/axios-0.18.0.js"></script>
    <script src="js/vue.js"></script>
</head>
<body>
    <div id="app">
        <table border="1" cellspacing="0" width="60%">
            <tr>
                <th>编号</th>
                <th>姓名</th>
                <th>图像</th>
                <th>性别</th>
                <th>职位</th>
                <th>入职日期</th>
                <th>最后操作时间</th>
            </tr>

            <tr align="center" >
                <td>1</td>
                <td>Tom</td>
                <td>
                    <img src="" width="70px" height="50px">
                </td>
                <td>
                    <span>男</span>
                   <!-- <span>女</span>-->
                </td>
                <td>班主任</td>
                <td>2009-08-09</td>
                <td>2009-08-09 12:00:00</td>
            </tr>
        </table>
    </div>
</body>
<script>
    new Vue({
       el: "#app",
       data: {
        
       }
    });
</script>
</html>
```

### 下班

14：20决定下班啦！！！