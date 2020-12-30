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
        <li>列表项</li>
        <li>列表项</li>
        <li>列表项</li>
    </ol>
ol，即ordered list（有序列表）；li，即list（列表项）   
`<ol>标签的子标签只能是li标签`  <br>
默认采用数字顺序，若想改变列表项符号，可<ol type="属性值"></ol>，属性值为1、a、A、i、I（CSS中用list-style-type实现列表项符号改变）
#### 2、无序列表
    <ul>
        <li>列表项</li>
        <li>列表项</li>
        <li>列表项</li>
    </ul>
 ul，即unordered list（无序列表）   
`ul标签的子标签也只能是li标签 ; ul元素内部的文本，只能在li元素内部添加，不能在li元素外部添加 ` <br>
默认情况下，无序列表的列表项符号是●，改变列表符号：<ul type="属性值"></ul> （CSS中用list-style-type实现列表项符号改变）
#### 3、定义列表
    <dl>
        <dt>名词</dt>
        <dd>描述</dd>
        ……
    </dl>
dl即definition list（定义列表）；dt即definition term（定义名词）；而dd即definition description（定义描述）。  <br>
dt标签用于添加要解释的名词，而dd标签用于添加该名词的具体解释。
### 四、表格
    
    
    
    
    
    
