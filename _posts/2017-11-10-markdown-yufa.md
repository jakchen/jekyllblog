---
layout: post
title:  "markdown 简明语法"
categories: markdown
tags: markdown
author: jakchen
---
* content
{:toc}

## 1.关于标题




```
▪大标题
====
说明：在文本下面加上等于号 = ，那么上方的文本就变成了大标题。等于号的个数无限制，但一定要大于0个。

▪中标题
-------
说明：在文本下面加上下划线 - ，那么上方的文本就变成了中标题，同样的,下划线个数无限制。

▪除此以外，关于标题还有等级表示法，分为六个等级，显示的文本大小依次减小。不同等级之间是以井号 # 的个数来标识的。一级标题有一个 #，二级标题有两个 # ，以此类推。# 后面需要加空格。

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
效果如下：
![markdown标题]({{ site.url }}/assets/mdtitle.png)<br/>
实际上，前文所述的大标题和中标题是分别和一级标题和二级标题对应的。三到六级没有下面的横线。

## 2.显示文本
```
要显示一个超链接的话，就直接输入这个链接的URL
给一段文字加入超链接的格式：[ 要显示的文字]( 链接的地址 "悬停显示的字")。"悬停显示的字"是可选项。 链接的地址和"悬停显示的字"之间需加一个空格。

插入圆点符，在文字前加*，要注意的是星号* 后面要有一个空格。否则显示为普通星号。
此外还有二级圆点和三级圆点。就是多加一个Tab。第二行一个Tab，第三行两个Tab。
* 前端开发
  * javescript
  * html
  * css
```
效果如下：
![list]({{ site.url }}/assets/list.jpg)<br/>

## 3.插入图片
```
▪第一种方法：![img](/assets/list.jpg "悬停显示的字")。"悬停显示的字"是可选项。
  一个惊叹号 !
  接着一个方括号，里面放上图片的替代文字
  接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上选择性的 'title' 文字。

▪第二种方法：GitHub仓库里的图片（建议使用这种方法，其他来源URL很可能会失效）。
前提是你的远程仓库有图片，图片链接的地址格式如下：
https://github.com/你的用户名/你的项目名/raw/分支名/存放图片的文件夹/该文件夹下的图片

其中，raw表示原数据的意思；主分支master。一般默认。
```

## 4.插入代码
```
我们需要在代码的上一行和下一行用``` 标记。第一行后可加语言，可加亮代码。``` 不是三个单引号，而是数字1左边，Tab键上面的键。 示例如下：

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html    ```
```
如下所示：
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
如果你想使一段话中部分文字高亮显示，来起到突出强调的作用，可以把它用 ` ` 包围起来。
## 5.插入表格
```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```
如下所示：

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

## 以上基本够用了，不会的就用html标签。
markdown支持大部分的html文本编辑标签。例如换行，用``<br/>``等。<br/>
但markdown有些标签写起来要简洁得多。<br/>
附：[markdown支持的html标签](https://github.com/github/markup/tree/master#html-sanitization)