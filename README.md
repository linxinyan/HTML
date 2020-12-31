# HTML
### 一、head标签
#### 1、title标签：定义网页的标题 <br>
#### 2、meta标签：定义页面的特殊信息，两个重要的属性：name和http-equiv 
* name属性 <br>
    取值:keywords	     网页的关键字，可以是多个，而不仅仅是一个 <br>
         description     网页的描述 <br>
         author	     author <br>
         copyright	     版权信息 <br>
* http-equiv属性     
定义网页所使用的编码：`<meta charset="utf-8" />` <br>
定义网页自动刷新跳转：`<meta  http-equiv="refresh" content="6;url=http://www.baidu.com"/>` 6秒后跳转<br>
#### 3、style标签：定义元素的CSS样式 <br>
#### 4、script标签：定义页面的JavaScript代码，也可以引入外部JavaScript文件 <br> 
#### 5、link标签：引入外部CSS文件

### 二、文本
#### 1、标题标签：h1、h2、h3、h4、h5、h6
一个页面一般只能有一个h1标签，而h2到h6标签可以有多个
#### 2、段落标签：p
#### 3、换行标签 `<br/>`
#### 4、文本标签
粗体标签：`strong`、b  <br>
斜体标签：`em`、i、cite  <br>
上标标签：sup  <br>
下标标签：sub  <br>
中划线标签：s   <br>
下划线标签：u     <br>
#### 5、水平线标签 `<hr/>`
#### 6、div标签
划分区域，结合CSS针对该区域进行样式控制
#### 7、自闭合标签
    eg：<meta />	定义网页的信息（供搜索引擎查看）<br>
        <link />	引入“外部CSS文件” <br>
        <br />	换行标签 <br>
        <hr />	水平线标签  <br>
        <img />	图片标签    <br>
        <input />	表单标签    <br>
#### 8、 块元素（block）：如h1~h6、p、div、hr、ol、ul
####     行内元素（inline）：如strong、em、a、span   
### 三、列表
#### 1、有序列表
    <ol>
        <li>列表项</li>    //ol，即ordered list（有序列表）；li，即list（列表项）
        <li>列表项</li>    //<ol>标签的子标签只能是li标签
        <li>列表项</li>    
    </ol>   
默认采用数字顺序，若想改变列表项符号，通过`<ol type="属性值"></ol>`，属性值为1、a、A、i、I（CSS中用list-style-type实现列表项符号改变）
#### 2、无序列表
    <ul>
        <li>列表项</li>    //ul，即unordered list（无序列表）
        <li>列表项</li>    //ul标签的子标签也只能是li标签 ; ul元素内部的文本，只能在li元素内部添加，不能在li元素外部添加
        <li>列表项</li>
    </ul>
默认情况下，无序列表的列表项符号是●，改变列表符号通过：`<ul type="属性值"></ul>`（CSS中用list-style-type实现列表项符号改变）
#### 3、定义列表
    <dl>
        <dt>名词</dt>
        <dd>描述</dd>
        ……
    </dl>
dl即definition list（定义列表）；dt即definition term（定义名词）；而dd即definition description（定义描述）。  <br>
dt标签用于添加要解释的名词，而dd标签用于添加该名词的具体解释。
### 四、表格
表格：table <br>
行：tr  <br>
单元格：td <br>
表格标题：caption    <br>
表头单元格：th    <br>
表头：thead    <br>
表身：tbody    <br>
表脚：tfoot    

    <table>
        <caption>表格标题</caption>
        
        <!--表头-->        
        <thead>
            <tr>
                <th>表头单元格1</th>
                <th>表头单元格2</th>
            </tr>
        </thead>
        
        <!--表身-->
        <tbody>
            <tr>
                <td>表行单元格1</td>
                <td>表行单元格2</td>
            </tr>
            <tr>
                <td>表行单元格3</td>
                <td>表行单元格4</td>
            </tr>
        </tbody>
        
        <!--表脚-->
        <tfoot>
            <tr>
                <td>标准单元格5</td>
                <td>标准单元格6</td>
            </tr>
        </tfoot>
    </table>
* 表脚（tfoot）往往用于统计数据的。对于thead、tbody和tfoot标签，不一定全部都上，例如tfoot就很少用。根据实际需要来使用这些标签。  <br>
* thead、tbody和tfoot除了使得代码更具有语义之外，还方便分块来控制表格的CSS样式。 <br>
合并行：rowspan，将“纵向的N个单元格”合并。

    <td rowspan = "跨越的行数"></td>
 合并列：colspan
 ### 五、图片
    <img src="" alt="" title="" />  
src 图片路径；alt 图片不显示时的提示文字；title 鼠标移到图片上出现的提示文字 <br>
对于img标签，src和alt这两个是必选属性；title是可选属性 <br>
图片格式：<br>
1、位图 <br>
（1）jpg适合存储颜色丰富的复杂图片，如照片、高清图片等。此外，jpg体积较大，并且不支持透明。 <br>
（2）png是一种无损格式，可以无损压缩以保证页面打开速度。此外，png体积较小，并且支持透明，不过不适合存储颜色丰富的图片。 <br>
（3）gif动图，图片效果最差，但适合制作动画。<br>
2、矢量图   <br>
优点：图片无论放大、缩小或旋转等都不会失真。  <br>
缺点：难以表现色彩丰富的图片效果（非常差）。  
### 六、超链接
#### 1、外部链接
    <a href="链接地址">文本或图片</a>    
不止文本，图片也可以设置为超链接，如`<a href="链接地址"><img src="" alt="" /></a>` <br>
其中target属性定义超链接打开窗口的方式。取值_blank，在新窗口打开链接
#### 2、锚点链接
当页面内容较多，导致页面过长的情况下，点击某一个超链接，就会跳到当前页面的某一部分 <br>
eg：`<a href="#article">推荐文章</a>`  跳转到指定id的元素位置
### 七、表单
* 如果一个页面仅仅供用户浏览，那就是静态页面。如果这个页面还能实现与服务器进行数据交互（像注册登录、话费充值、评论交流），那就是动态页面。
#### 1、form标签：所有表单标签放在form标签内部
（1）name属性：一个form标签就是一个表单。为了区分不同的表单，使用name属性来给表单进行命名。 <br>
（2）method属性：指定表单数据使用哪一种http提交方法，通常取值"post" <br>
（3）action属性：指定表单数据提交到哪一个地址进行处理，eg：`<form action="index.php"></form>` <br>
（4）target属性：指定窗口的打开方式。取值_blank，在新窗口打开链接 <br>
（5）enctype属性：指定表单数据提交的编码方式，除非用到上传文件功能，一般情况下不用设置
#### 2、input标签：`<input type="表单类型" />`
#### （1）单行文本框 `<input type="text" />`
属性：value 设置文本框的默认值；size 设置文本框的长度；maxlength 设置文本框中最多可以输入的字符数
#### （2）密码文本框 `<input type="password" />`
属性同单行文本框一致，二者的区别是：在单行文本框中输入的字符是可见的，而在密码文本框中输入的字符不可见。
#### （3）单选框 `<input type="radio" name="组名" value="取值" />`
name属性表示单选按钮所在的组名，value表示单选按钮的取值，这两个属性必须要设置。<br>
要想在默认情况下，选中某个单选框，使用checked属性来实现。
#### （4）复选框 `<input type="checkbox" name="组名" value="取值" />`     
#### （5）普通按钮button `<input type="button" value="取值" />` 
value的取值就是按钮上的文字<br>
配合JavaScript来进行各种操作
#### （6）提交按钮submit `<input type="submit" value="取值" />`
向服务器提交表单数据
#### （7）重置按钮reset `<input type="reset" value="取值" />`
清除用户在表单中输入的内容   <br>
* 重置按钮只能清空它“所在form标签”内表单中的内容，对于当前所在form标签之外的表单清除是无效的。
#### （8）文件上传 `<input type="file" />`     
#### （9）多行文本框 `<textarea rows="行数" cols="列数" value="取值">默认内容</textarea>`
默认内容为多行文本框默认显示的文本
#### （10）下拉列表
    <select>
        <option>选项内容</option>
        ……
        <option>选项内容</option>
    </select>
select标签属性：<br>
（1）multiple	设置下拉列表可以选择多项（使用“Ctrl+鼠标左键”来选取）: `<select multiple></select>` <br>
（2）size 设置下拉列表显示几个列表项，取值为整数 <br>
option标签属性：<br>
（1）selected	是否选中
（2）value 选项值
* 表单元素不一定都要放在form标签内。对于要与服务器进行交互的表单元素就必须放在form标签内才有效。如果表单元素不需要跟服务器进行交互，那就没必要放在form标签内。
### 八、框架
#### 1、iframe标签：实现一个内嵌框架
     <iframe src="链接地址" width="数值" height="数值"></iframe>
     

