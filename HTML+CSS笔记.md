# 一：HTML笔记

### 1.1 页面说明

```html
<!--声明文本规范-->
<!DOCTYPE html>
<!--根节点-->
<html>
	<!--头部信息-->
	<head>
		<!--设置网页编码格式 支持中文="utf-8"-->支持中文只有两种，还有一种是支持中文是jbk
		<meta charset="utf-8" />
		<!--标题信息-->
		<title></title>
		
	</head>
	<!--主体信息-->
	<body>
    </body>
</html>
```

### 1.2 基本标签

**alight属性**

图像中：值: `left(左)`, `right(右)`, `middle(中)`, `top(上)`, `bottom(下)`
表格中：表格 (`<table>`) 值: `left(左)`, `center(中)`, `right(右)`
				单元格 (`<td>`, `<th>`) 值: `left`, `center`, `right`, `justify(居中)`
块级元素 (`<div>`, `<p>`, `<h1>`, 等)：值: `left`, `center`, `right`, `justify`

| 标签                                                         | 说明                                     |
| ------------------------------------------------------------ | ---------------------------------------- |
| <h1></h1>                                                    | 标题标签 范围h1~h6                       |
| <p></p>                                                      | 段落标签                                 |
| <b></b>                                                      | 文字加粗                                 |
| <strong></strong>                                            | 文字加粗                                 |
| <i></i>                                                      | 文字倾斜                                 |
| <u></u>                                                      | 普通带下划线文字标签                     |
| <ins></ins>                                                  | 普通带下划线文字标签                     |
| <sub></sub>                                                  | 下标文字                                 |
| <sup></sup>                                                  | 上标文字                                 |
| <del></del>                                                  | 带删除线                                 |
| <span></span>                                                | 普通文字标签                             |
| <div></div>                                                  | 盒子标签                                 |
| <a href="地址"></a>                                          | 超链接标签，使用id可以跳转到页面指定位置 |
| <img src="地址" alt="加载失败提示语" title="鼠标悬停提示语"/> | 图片插入标签，可设置height,width         |
| `<br/>`                                                      | 换行标签                                 |
| <hr color="" width="宽度%" size="粗细，默认2px" align="水平线位置"/> | 水平线标签                               |
| `&nbsp;`                                                     | 一个空格                                 |
| `&copy;`                                                     | 版权符号&copy;                           |
| `&reg;`                                                      | 商标符号&reg;                            |
| `&yen;`                                                      | 钱&yen;                                  |

### 1.3 列表标签

> 注意：列表会有外边距

```html
<ol type="序列类型 取值：默认(数字) a(小写的英文) A(大写的英文) i(小写的罗马字母) I(大写的罗马字母)">
    <li>有序列表1</li>
    <li>有序列表2</li>
    <li>有序列表3</li>
    <li>有序列表3</li>
</ol>

<ul type="无序类表 取值：disc(实心圆点 默认) circle(空心圆点) (square(实心小方块))" >
    <li>无序列表</li>
    <li>无序列表</li>
    <li>无序列表</li>
    <li>无序列表</li>
</ul>

<dl>
    <dt>标题</dt>
    <dd>自定义序列项</dd>
    <dd>自定义序列项</dd>
    <dd>自定义序列项</dd>
    <dd>自定义序列项</dd>
</dl>
```

### 1.4 表格标签

```html
<table>
    <caption>标题标签</caption>
    <tr>//行标签
    	<th>表头便签（自动居中）</th>
    </tr>
    <tr>
        <td>单元标签（内容）</td>
    </tr>
</table>
```

tabel标签属性

| 属性        | 取值                                | 说明             |
| ----------- | ----------------------------------- | ---------------- |
| border      | 像素点(px)为单位取值                | 边框宽度取值     |
| width       | 像素点(px)为单位取值                | 表格宽度取值     |
| bgcolor     | 颜色名称  16进制颜色代码  RGB颜色值 | 背景色取值       |
| bordercolor | 颜色名称  16进制颜色代码  RGB颜色值 | 边框色           |
| cellspacing | 像素点(px)为单位取值                | 单元格之间的距离 |
| cellpadding | 像素点(px)为单位取值                | 文字与边框的距离 |

tr标签属性

| 属性   | 取值                | 说明             |
| ------ | ------------------- | ---------------- |
| align  | left  center  right | 内容水平显示方向 |
| valign | top  middle  bottom | 内容垂直显示方向 |

td标签属性

| 属性    | 取值 | 说明                         |
| ------- | ---- | ---------------------------- |
| colspan | 行数 | 合并行数(从左往右，合并要删) |
| rowspan | 列数 | 合并列数(从上往下，合并要删) |

### 1.5 表单标签

```html
<form>
    <input type=""/>
    <select>//下拉列表框
        <option>选项内容</option>
    </select>
    <textarea>多行文本域</textarea>
    <button type="reset/submit">重置/提交</button>
</form>
<!--label标签：通过for="id"关联表单控件-->
<label for="username">用户名：</label>
<input type="text" id="username"/>
<!--或者直接写在当中-->
<label>用户名：<input type="text"/></label>
```

form标签属性

| 属性         | 取值                 | 说明                               |
| ------------ | -------------------- | ---------------------------------- |
| id           | 自定义               | 唯一标识                           |
| name         | 自定义               | 名称                               |
| action       | 地址                 | 表单提交的地址                     |
| method       | get  post            | 表单提交方式，文件提交需设置为post |
| enctype      | multipart/form-data  | 文件提交需设置                     |
| autocomplete | on(默认值，允许) off | 设置输入框是否显示历史输入         |

input标签属性

| 属性         | 取值                 | 说明                                 |
| ------------ | -------------------- | ------------------------------------ |
| type         | ...                  | 决定这个input的类型                  |
| disabled     | /                    | 禁用该input，可在js中控制true false  |
| checked      | checked              | 按钮默认选中                         |
| id           | 自定义               | 唯一标识不可重复                     |
| size         | 像素点(px)为单位取值 | 针对文本框和密码框而言表示宽度       |
| name         | 自定义               | 元素名称                             |
| value        | 自定义               | 针对框表设置初始值，针对按钮表文本值 |
| maxlength    | 数字                 | 可以输入最大字符数量                 |
| autocomplete | off                  | 使文本框不会显示下拉历史输入         |
| placeholder  | 内容                 | 设置文本框内提示语，输入内容覆盖     |
| readonly     | true                 | 元素设置为只读                       |
| required     | /                    | 表单提交时必须填写                   |
| autocomplete | on(默认值，允许) off | 设置输入框是否显示历史输入           |

属性type取值

| 取值           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| text           | 文本框                                                       |
| password       | 密码框                                                       |
| file           | 文件域                                                       |
| submit         | 提交按钮                                                     |
| reset          | 重置按钮                                                     |
| button         | 普通按钮                                                     |
| radio          | 单选按钮（同组按钮设置相同name，value为后端取值）            |
| checkbox       | 多选按钮（同组按钮设置相同name，value为后端取值）            |
| email          | 邮箱框，会验证邮件的样式                                     |
| url            | 会验证是否符合URL的格式要求                                  |
| number         | 数字输入框，属性：max  min  step(点击切换时的数字间隔)  value |
| range          | 滑动条控件，类似于进度条，属性同number                       |
| color          | 选取颜色，提交时以十六进制颜色代码提交                       |
| data           | 日期选择器：年月日                                           |
| month          | 年 月                                                        |
| week           | 年 周                                                        |
| time           | 时 分                                                        |
| dataTime       | 年月日 时 分 自动选择网络时间                                |
| dataTime-local | 年月日 时 分 自动选择本地时间                                |

select标签属性

| 属性         | 取值                 | 说明                       |
| ------------ | -------------------- | -------------------------- |
| size         | 项数                 | 显示几项                   |
| autocomplete | on(默认值，允许) off | 设置输入框是否显示历史输入 |

option标签属性

| 属性     | 取值   | 说明               |
| -------- | ------ | ------------------ |
| selected | /      | 默认选择           |
| value    | 自定义 | 提交表单时传递的值 |

textarea标签属性

> input属性此处也可用

| 属性         | 取值                        | 说明                       |
| ------------ | --------------------------- | -------------------------- |
| cols         | 像素点(px)为单位取值        | 文本区宽                   |
| rows         | 像素点(px)为单位取值        | 文本区高                   |
| name         | 自定义                      | 表单提交该本文域的名字     |
| wrap         | 默认换行，off表示不自动换行 | 控制文本如何换行           |
| autocomplete | on(默认值，允许) off        | 设置输入框是否显示历史输入 |

### 1.6 媒体标签

音频标签

```html
<audio controls>
  <source src="audio-file.mp3" type="audio/mpeg">
  <source src="audio-file.ogg" type="audio/ogg">
</audio>
```

视频标签

```html
<video width="640" height="360" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
</video>
```

| 属性     | 取值                                                         | 说明                                                         |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| controls | /                                                            | 显示音频播放控件                                             |
| src      | url地址                                                      | 指定音频视频文件的URL。如果提供多个音频源，应使用`<source>`元素。 |
| autoplay | /                                                            | 页面加载后自动播放音频                                       |
| loop     | /                                                            | 音频播放结束后重新开始                                       |
| muted    | /                                                            | 初始静音                                                     |
| preload  | `auto`（默认），`metadata`（只预加载元数据），和`none`（不预加载） | 指示浏览器如何预加载音频                                     |
| poster   | url地址                                                      | 视频加载前显示的图像                                         |

# 二：CSS笔记
