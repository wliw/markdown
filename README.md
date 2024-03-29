# 自我学习markdown
该仓库为个人学习markdown仓库，不具有任何权威性，纯属个人学习。  
如有相关侵权，请与我联系，将删除相关侵权内容，并给予最诚挚的歉意。

## 一、标题
方式1：  
一级标题：第一行标题，第二行加上三个以上的半角等号（=）；二级标题：第一行标题，第二行加上三个以上的半角连接符号（-）；以下为示例：

    一级标题一级标题
    ============== 

一级标题一级标题
==============

    二级标题二级标题
    --------------

二级标题二级标题
--------------

方式2：  
标题前面有1-6个半角井号（#）表示1-6级标题。以下为示例：

    # 一级标题
# 一级标题
    ## 二级标题
## 二级标题
    ### 三级标题
### 三级标题
    #### 四级标题
#### 四级标题
    ##### 五级标题
##### 五级标题
    ###### 六级标题
###### 六级标题

## 二、段落
由一行或多行文本组成，就像当前这句话一样。

## 三、换行 
1、在需要换行的地方，加两个空格，然后换行继续输入内容； 

_PS：编辑器中有如果有保存即去除末尾空格的设置，在编写markdown的时候，可能要暂时设置为不去除，末尾两个空格，在markdown中语法中识别为回车换行。_

    这是示例一[space][space]
    这是示例一

这是示例一  
这是示例一

2、每段文本中间加一个空行； 

    这是示例二

    这是示例二

这是示例二

这是示例二 

3、加上&lt;br /&gt;标签。

    这是示例三<br />
    这是示例三

这是示例三<br />
这是示例三

## 四、块引用
对于引用的文本，在每行的行首加上半角大于号：&gt;  
_PS：换行注意用上面换行规则_

    > 这是第一行引用文本；
    > 这是第二行引用文本；
    > 这是第三行引用文本；
    >> 这是二级块引用；
    >> 这是二级块引用；
    >>> 这是三级块引用；
    >>> 这是三级块引用；

> 这是第一行引用文本；这是第一行第二句应用文本；  
> 这是第二行引用文本；  
> 这是第三行引用文本；  
>> 这是二级块引用；  
>> 这是二级块引用；
>>> 这是三级块引用；  
>>> 这是三级块引用；

## 五、列表
无序列表：列表每项开头用半角星号（* ）或者半角连字符（-）或者半角加号（+)  
_PS：注意另取一个空行后开始编写列表_

    * 可以使用 `*` 作为标记
    + 也可以使用 `+`
    - 或者 `-`

* 可以使用 `*` 作为标记
+ 也可以使用 `+`
- 或者 `-` 

有序列表：列表以数字加点号（.）开头  

    1. What a great season.

        > 这是列表嵌套块级引用[space][space]
        > 这是列表嵌套块级引用[space][space]
        > 这是列表嵌套块级引用

    2. What a great season.

        * 列表嵌套列表
        * 列表嵌套列表

    3. What a great season.

        1. 列表嵌套列表
        2. 列表嵌套列表

1. What a great season.

    > 这是列表嵌套块级引用  
    > 这是列表嵌套跨级引用  
    > 这是列表嵌套跨级引用

2. What a great season.

    * 列表嵌套无序列表
    * 列表嵌套无序列表

3. What a great season.

    1. 列表嵌套有序列表
    2. 列表嵌套有序列表

## 六、代码块
在需要markdown能显示像HTML中&lt;pre&gt;&lt;/pre&gt;或者&lt;code&gt;&lt;/code&gt;的样式时，另取一行，缩紧四个空格或者一个tab，markdown自动标注为代码块。

    [space][space][space][space]这是代码块示例
    [tab]这是代码块示例

    这是代码块示例
    这是代码块示例

## 七、水平线
中间用三个以上连字符（-）或者星号（* ）或者下划线（_ ），就可实现一条水平线。  
_PS：要求连字符上一行必须不是文本内容，否则文本和连字符会一起被识别成二级标题，其他两个符号则不会影响_
    
    ---
    ***
    ___

---
***
___

### 反例：
    这是反例
    -------

这是反例
-------

## 八、链接
markdown的链接有两种编写方式：内联和引用

### 方式一：内联
用中括号包裹链接的文本[link text]，后面用小括号包裹真实链接和可选的链接title(link "title")，举例说明：  

    This is [a link example](https://github.com/wliw/markdown 'a link example').
    This is [an another example](https://github.com/wliw/markdown).

This is [a link example](https://github.com/wliw/markdown 'a link example').  
This is [an another example](https://github.com/wliw/markdown).

也可以根据当前markdown文件的位置，通过相对路径写法获取本地链接。

    This is [a relative link](./index.html).

This is [a relative link](./index.html).

### 方式二：引用
第一行用中括号包裹链接文本[link text]，后面跟着另一个中括号包裹的链接映射文本[map link id]，两个中括号之间可以有空格，每个[map link id]另起一行，编写出对应的链接，同样链接后面跟着title文本，用于鼠标hover时显示tip文本，举例： 

    This is [a reference link example][reference link].
    This is [a reference relative link example][reference relative link].
    
    [reference link]: https://github.com/wliw/markdown
    [reference relative link]: ./index.html "title text"

This is [a reference link example][reference link].  
This is [a reference relative link example][reference relative link].  

[reference link]: https://github.com/wliw/markdown
[reference relative link]: ./index.html "title text"

    PS：
    [id]: link "title text"
    [id]: link 'title text'
    [id]: link (title text)
    1、这三种表达方式是等价的，不过Markdown.pl 1.0.1 有一个已知的问题就是不能用单引号来包围链接标题；
    2、引用的链接与上面的内容要添加一行分割，做兼容性处理，github或者其他一些地方没有空行无法正常解析为引用链接方式。

链接引用id可以忽略，即写一个空中括号[link text][]，此时[link text]就是链接引用id；另外链接引用id对大小写不敏感；[link text][A]等价于[link text]][a]。

    [ignore map link id][]
    
    [ignore map link id]: https://github.com/wliw/markdown

[ignore map link id][]

[ignore map link id]: https://github.com/wliw/markdown

## 九、强调
用星号（\*）或者下划线（\_）包裹的内容等价于HTML中的em元素，用两个星号（\*\*）或者用两个下划线（\_\_）包裹内容等价于HTML的strong元素。举例：

    *强调内容*
    _强调内容_
    **强调内容**
    __强调内容__

*强调内容*  
_强调内容_  
**强调内容**  
__强调内容__

## 十、代码
使用反引号包裹代码片段，等价于HTML中code元素包裹的内容
    
    这是markdown中的代码示例`var a = 1;`。

这是markdown中的代码示例`var a = 1;`。

## 十一、图片
与链接有相似的格式，但是比链接多了一个感叹号，也分为内联和引用两个格式，或者直接HTML用img标签。
    
    ![alt text](link "title text")

    ![alt text][link id]
    
    [link id]: link "title text"
    
    <img src="imgSrc" alt="alt text" title="title text" width="width" height="height" />

举例：

    ![头像](https://avatars1.githubusercontent.com/u/24364542?s=460&v=4 "头像")

    ![头像][avatar]
    
    [avatar]: https://avatars1.githubusercontent.com/u/24364542?s=460&v=4 "头像"
    
    <img src="https://avatars1.githubusercontent.com/u/24364542?s=460&v=4" alt="alt text" title="title text" width="200" height="200" />

![头像](https://avatars1.githubusercontent.com/u/24364542?s=460&v=4 "头像")
![头像][avatar]

[avatar]: https://avatars1.githubusercontent.com/u/24364542?s=460&v=4 "头像"

<img src="https://avatars1.githubusercontent.com/u/24364542?s=460&v=4" alt="alt text" title="title text" width="200" height="200" />

## 十二、自动链接
使用尖括号包裹URL或者email地址，markdown会将其自动转换成链接或者邮件链接。举例：

    <https://github.com/wliw/markdown>[space][space]
    <wliw@github.com>

<https://github.com/wliw/markdown>  
<wliw@github.com>

## 十三、转义字符
像星号（\*）、下划线（\_）等大部分ASCII字符在markdown中都有语法标识符含义，如果要把这些字符输出而不是被解析成markdown语法，则字符前添加反斜杠（\\），表示转义字符。举例：

    \*
    \_
    \-
    \\ \` \! \{\} \[\] \(\) \. \# \+

\*  
\_  
\-  
\\ \` \! \{\} \[\] \(\) \. \# \+

###### 参考链接
[Markdown 中文文档](https://markdown-zh.readthedocs.io/en/latest/)  
[Markdown 入门参考](http://xianbai.me/learn-md/index.html)

