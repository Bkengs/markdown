## 区块元素

### 段落与换行

#### 段落

markdown中的段落要保持去后都有一个空行，markdown中的段落要保持去后都有一个空行，markdown中的段落要保持去后都有一个空行，markdown中的段落要保持去后都有一个空行，markdown中的段落要保持去后都有一个空行。

#### 换行

markdown中的段落的换行需要先在换行处插入2个以上的空格，markdown中的段落的换行需要先在换行处插入2个以上的空格  
markdown中的段落的换行需要先在换行处插入2个以上的空格，markdown中的段落的换行需要先在换行处插入2个以上的空格。

### 区块的引用

#### 在每一行的开头处加入>和空格

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

#### 也可以只在整个段落的第一行最前面加上>和空格

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

#### 嵌套的区块的引用

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

#### 区块的引用中可以继续使用其他标记

> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");

### 列表

#### 无序列表使用*，+，-加空格

* Red
* Green
* Blue

#### 有序列表数字组加.加空格的形式，markdown不会在意你的每个数字，第一个往下依次累加，注意五个同类型的列
#### 即使中间隔了空行，也还是会自动连接起来

1.  Bird
2.  McHale
3.  Parish  

  
1.  Bird
1.  McHale
4.  Parish

#### 列表段落，

* Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
* Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.

#### 列表项目可以包含多个段落，每个项目下的段落开头都必须缩进 4 个空格或是 1 个制表符

1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.

#### 列表项目可以包含其他标记，>需要1个缩进（4个空格），代码块需要2个缩减（8个空格）[实际情况下github需要9个]

    代码块

*   A list item with a blockquote:
    
    > This is a blockquote
    > inside a list item.
    
1.   一列表项包含一个列表区块：

         return shell_exec("echo $input | $markdown_script");

#### 行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠

1986\. What a great season.

### 代码区块

#### 1个缩减或者4个空格，一个代码区块会一直持续到没有缩进的那一行

    tell application "Foo"
        beep
    end tell

### 分割线，用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西，可以有空个

- - -

## 区段元素

### 链接（可带title）（可以用相对路径）

#### 行内式

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

#### 参考式

链接内容定义的形式为：

* 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
* 接着一个冒号
* 接着一个以上的空格或制表符
* 接着链接的网址
* 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

This is [an example][id] reference-style link.

[id]: http://example.com/  "Optional Title Here"

### 斜体（单个*或_包围） 粗体（两个*或_包围）如果要在文字前后直接插入普通的星号或底线，你可以用反斜线
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

### 代码，如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段

Use the `printf()` function.
``There is a literal backtick (`) here.``

### 图片

行内式的图片语法看起来像是：

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
详细叙述如下：

一个惊叹号 !
接着一个方括号，里面放上图片的替代文字
接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。
参考式的图片语法则长得像这样：

![Alt text][id]
「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

[id]: url/to/image  "Optional title attribute"
到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 <img> 标签。
