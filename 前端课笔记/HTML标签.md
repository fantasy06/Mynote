# HTML初级



整体结构

```html
<html> <!--开始标签-->
<html>
	<head>
		<meta charset="utf-8" />  <!--字符编码避免网页文字乱码-->
		<title>网页的标题</title>
	</head>
	<body>
	<!--网页的基本内容-->
	</body>
</html> <!--结束标签-->

```

## 初级标签

1. 标题标签

   > H1，H2，....，H6。（1-->6）大标题-->小标题，成对出现，开始标签  `<H1>` ，一个结束标签  `</H1>` 。

2. 段落标题

   >段落是通过  `<p> ` 标签进行定义的，成对出现，开始标签   `` <p>``  ，一个结束标签  `</p>` 。

3. 文字标签

   > `<strong></strong>`，加粗文字标签；`<em></em>`  斜体文字标签，可嵌套

4. 符号标签

   >`<del></del>`，在文字上添加删除线，如：~~文字~~

## 高级标签

1. **块状标签**

   > `<div></div>` ,每一个div占满一整行。  `<span></span>`，文本信息在一行展示

2. **空格和换行，尖括号**

   >`<br>`  换行标签，`&nbsp;` 空格符号，`&lt `左尖括号，`&gt;` 右尖括号

 3. **有序列表标签**

    > ```html
    > <ol>			  <!--网页显示-->
    >   <li>第一条</li>	<!--1.第一-->
    >   <li>第二条</li>	<!--2.第二-->
    >   <li>第三条</li>	<!--3.第三-->
    > </ol>
    > ```
    >
    >  `<ol>` 可以增加属性，type，换排序符号；
    >
    > 如 `<ol type="A">` ，就从A，B顺序排列；符号可以换 `A,a,1,i I` ，不填默认数值`1`；
    >
    > 倒叙 `<ol reversed="reversed">` ；
    >
    >  `<ol start="数值">`，更换开始符号的数值；

4. **无序列表标签**

   >```html
   ><ul>			  
   >  <li>第一条</li>	
   >  <li>第二条</li>	
   >  <li>第三条</li>	
   ></ul>
   >```
   >
   >默认每一段文本前面显示小圆点
   >
   >属性：`<ul type=disc>` 默认值实心小圆点，`circle ` 空心小圆点，`square` 小方块

  5. **图片插入**

     > `<img src="图片路径">`
     >
     > 包括：
     >
     > 1，网上url；
     >
     > 2，本地的绝对路径(同一个文件夹下，直接写图片文件名)；
     >
     > 3，本地的相对路径(不同一个文件夹下，写完整图片路径)；
     >
     > 属性：
     >
     > 1，`<img src="图片路径" alt="图片占位符">`，即图没有加载出来时显示
     >
     > 2，`<img src="图片路径" title=”图片提示符“>`，即鼠标移到图时显示

6. **链接标签a**

     >1. 超链接：`<a href="网址">网站名</a>`
     >2. 锚点：`<a href="#id">文字</a>`；id指某个标签的id名字，运用于：页面目录，回到顶部
     >3. 打电话或发邮件：`<a href="tel:电话号码">文字</a>`；`<a href="mailto:邮箱地址">文字</a>`
     >4. 协议限定符：使用js
     >
     >属性：`target=_blank ` 点击链接在新页面弹出

7. **表单**

   - 信息输入框

       > ```html
       > <form method="get" action="" > 	<!--action：发送出去的地址-->
       > 	name: <input type="text" name="name" />		 <!--文本输入框，name：数值内容-->
       > 	password: <input type="password" name="password" />	<!--密码输入框，name：数值内容-->
       > <input type="submit" value="Submit" />  			<!--提交按键，value：数据值-->
       > </form>
       > ```

   - 单选框

       > ```html
       > <form method="get" action="" > 	<!--action：发送出去的地址-->
       > 	<p> 选择其中一个 </p>
       > 1.第一个<input type="radio" name="name" value:"one">	<!--name相同表示同个选择问题-->
       > 1.第二个<input type="radio" name="name" value:"two">
       > 1.第三个<input type="radio" name="name" value:"three">
       > <input type="submit" value="Submit" />  		<!--提交按键，	value：数据值-->
       > </form>
       > ```

   - 副选框

       > ```html
       > <input type="checkobx" name="题目" value:"提交的数值">  	<!--大致与上面相同-->
       > ```

   - 选项下拉菜单

       > ```html
       > <select name="">
       >  <option>选项一</option>
       >   <option>选项二</option>
       > </select>
       >```
       > 表单添加默认选项：标签后加入 `checked="checked"`
       >  


------

# CSS初级

## 引入CSS

 1. 行间样式
	>
	>    ```html
	>    <div style="css定义内容">   
	>    </div>
	>    ```

 2. 页面级CSS
	>
	>    在头部标签  `<head>`  下加入
	>
    >    ```html
    >    <style type="text/css">
    >        <!--css定义内容-->	
    >    </style>
    >    ```

 3. 外部CSS文件
    >    新加一个文件后缀为.CSS
    >
    >    在头部标签  `<head>`  下加入
    >
    >    ```html
    >    <link rel="stylesheet" type="text/css" href="CSS文件位置"/>\
    >    ```
    >

## **CSS选择器**

1. `id`，在div标签加入id名
  
    >```html
    ><!--id创建-->
    ><div id="填id名"></div>
    ><!--下面css定义,引入css页面填写-->
    >#id名{   "css定义内容"   }
    >```


2. `class`，在div标签加入class名

    >```html
    ><!--class创建-->
    ><div class="填calss名"></div>
    ><!--下面css定义,引入css页面填写-->
    >#id名{  "css定义内容"   }
    >```


3. `标签选择`

    >```html
    ><!--下面css定义,引入css页面填写-->
    >标签名{   "css定义内容"  }
    >```


4. `属性`，如[id]，[class]，[id="123"]...

    >```html
    ><!--下面css定义,引入css页面填写-->
    >[属性]{  "css定义内容"  }
    >```


5. `通配符`，对所以标签都生效

    >```html
    ><!--css定义,引入css页面填写-->
    >*{ "css定义内容" }
    >```

6. `父子选择器/派生选择器`

    >```html
    ><div>
    > <span>1</span>  <!--对 1 进行css定义-->
    ></div>
    ><!--下面css定义,引入css页面填写-->
    >div span{
    >	"css定义内容"
    >}
    >```


7. `直接子元素选择器`

    >```html
    ><div>
    > <span>1</span>  <!--对 1 进行css定义-->
    > <span>2</span>
    ></div>
    ><!--下面css定义,引入css页面填写-->
    >div > span{
    >	"css定义内容"
    >}
    >```


8. `并列选择器`

    >```html
    ><div> 1 </div>
    ><div calss="demo"> 2 </div>		<!--对 2 进行css定义-->
    ><p calss="demo"> 3 </p>
    ><!--下面css定义,引入css页面填写-->
    >div.demo{
    >	"css定义内容"
    >}
    >```


9. `分组选择器`

    >```html
    ><!--对 1,2,3 进行css定义-->
    ><em> 1 </em>			
    ><strong> 2 </strong>
    ><span> 3 </span>
    ><!--下面css定义,引入css页面填写-->
    >em,strong,span{
    >	"css定义内容"
    >}
    >```


10. `伪类选择器`

    >```html
    ><!--将鼠标悬浮在改标签时的变化，css定义-->
    ><a href="链接地址">链接文本</a>
    ><!--下面css定义,引入css页面填写-->
    >a:hover{
    >	"css定义内容"
    >}
    >```

## **CSS选择器的优先级**

- > `!import `> `行间样式` > `id` > `class` =`属性` > `标签选择` > `通配符`
   >
   > `!import`  在CSS定义内容后可加上
   >
   > 优先级是根据各个选择器的`权重大小`比较的
   >
   > |        选择器         |       权重        |
   > | :-------------------: | :---------------: |
   > |        !import        | Infinity (无穷大) |
   > |       行间样式        |       1000        |
   > |          id           |        100        |
   > | class \| 属性 \| 伪类 |        10         |
   > |    标签 \| 伪元素     |         1         |
   > |        通配符         |         0         |
   >
   > `注`：权重之间是256进制



## CSS语法

1. 基本样式

   > ```css
   > 选择器{
   >         属性名1：属性值1;
   >         属性名2：属性值2;
   >         属性名3：属性值3;
   > }
   > /*例如定义一个div*/
   > div{ 
   >     width:100px; 
   >     height:100px; 
   >     background:red; 
   > }
   > ```

2. 文字定义

   >```css
   >font-size:16px;     /* 调整文字大小 */
   >font-weight:bold;	/* 调整文字粗细  可选属性，默认是 "normal"，"bold" 是加粗，可直接写数值: "100-900" 之间。*/
   >font-style:normal;	/* 属性值："italic" 斜体的字体样式, "oblique" 倾斜的字体样式*/
   >font-family:字体名称;	/* 可以修改显示的字体  */
   >/*字体颜色定义，三种方法*/
   >color:rgb(0,0,0);	/* 红，绿，蓝 三个颜色的值 0-255*/
   >color:#000000;		/* 可以分开00-00-00，代表红，绿，蓝的值，用16进制数表示  */
   >color:red;			/*直接所以英文颜色名字*/	
   >```



3. 段落文字定义

   >```css
   >/* 段落文字水平居中 */
   >text-align:center;	/* 可以选属性，靠左 "left"，靠右："right" */
   >line-height:10px;	/* 行高，行间距 */
   >text-indent:2em;	/* 首行缩进两个字符大小；1 em= 1 font-size   */
   >text-decoration:line-through;	/* 删除线 */
   >text-decoration:underline;	/* 下划线 */
   >text-decoration:overline;	/* 上划线 */
   >```

4. 边框

   > borde(边框)
   >
   > ```css
   > /* 边框宽度 | 边框样式 | 边框颜色 */
   > border:1px dashed green;	/* "dashed" 虚线；"solid" 实线 */
   > /*可以分开4个边角定义*/
   > /* 例如左边left,可选 tiop，right，bottom */
   > border-left:1px dashed green;
   > ```
   > `margin(外边距)`	`padding（填充）`
   >
   >  margin/padding:1px ，margin/padding:30%；
   >
   > 对应四个上，下，左，右位置大小的值
   >
   > 可拆开， margin/padding-top，依此类推



## 元素的类型

每一个元素都有默认的 `display` 属性值；

- **行类元素**

  >特点：内容决定元素所占位置，不可以通过css改变宽高
  >
  >行内元素标签：`span`	`strong`	`a`	`em`	`del`
  >
  >CSS默认：`display: inline;`
  >
  >凡是带有 inline 的元素，都有文字特征

- **块类元素**

  > 特点：独占一行，可以通过css改变宽高
  >
  > 块内元素标签：`div`   `p`   `ul`   `li`   `ol`  `form`  `address`
  >
  > CSS默认：`disply: block;`

- **行级块元素**

  > 特点：内容决定改变大小，可以通过css改变宽高
  >
  > 行级块元素标签：`img`
  >
  > CSS默认：`disply: inline-block;`

## 盒子模型

- 内容
  >CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距（margin），边框（border），填充（padding），和实际内容（content）。
  >
  >盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

- 结构图

  > <img src="https://www.runoob.com/images/box-model.gif" style="zoom: 150%;" />

- 说明
  >
  >- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
  >- **Border(边框)** - 围绕在内边距和内容外的边框。
  >- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
  >- **Content(内容)** - 盒子的内容，显示文本和图像

- 宽度和高度的计算

  >总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距;
  >
  >总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

## 定位

### absolute 定位

>脱离原来位置进行定位
>
>位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于`<html>`；
>
>absolute 定位使元素的位置与文档流无关，因此不占据空间

###  relative 定位

>保留原来的位置进行定位
>
>相对自己原来的位置进行定位
>
>元素虽然偏移某个距离，但仍然占据原来的空间

### fixed 定位

>元素的位置相对于浏览器窗口是固定位置。
>
>即使窗口是滚动的它也不会移动

### CSS定位属性

> `top`	`bottom`	`left`	`right`
>
> 分别对应上，下，左，右位置的值，可用数值 与百分比  top:1px ，top:30%；
