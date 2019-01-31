# \<head\>元素：包含一些页面的元数据（不会在浏览器中显示）

> 元数据（Metadata）：又称中介数据、中继数据，是描述数据的数据（data about data），主要是描述数据属性（property）的信息，用来支持如指示存储位置、历史数据、资源查找、文件记录等功能。

## \<head\>元素内包含：  

### 1. \<title\> 元素：增加一个标题  
\<title\> 元素是用来表示整个HTML文档大致内容的元数据。  
\<title\> 元素的内容会被作为建议的书签名（Bookmarks），也会被用在搜索的结果中（有助于SEO）。

### 2. \<meta\> 元素：为一个文档添加元数据

许多 \<meta\> 元素包含了 name 和 content 特性：  
　　name：指定 meta 元素的类型；说明该元素包含了什么类型的信息。  
　　content：指定了实际的元数据内容。  

* 指定文档中字符的编码：  
```<meta charset="utf-8">（utf-8 是一个通用的字符集，它包含了任何人类语言中的大部分的字符。）```  
* 添加作者和描述：    
```<meta name="author" content="wsywwww">```  
```<meta name="description" content="这个网站怎样怎样。。。">（有助于SEO）```  

> Tip：许多 <meta> 特性已经不再使用。  例如：keywords，提供关键词给搜索引擎，根据不同的搜索词，查找到相关的网站。  
<meta  name="keywords" content="fill, in, your, keywords, here"\>  
> 被搜索引擎忽略了， 因为作弊者填充了大量关键词到keyword， 错误地引导搜索结果。  

* 其他类型的元数据：专有创作，旨在向某些网站(如社交网站)提供可使用的特定信息。  

### 3. 为站点增加自定义图标：favicons    
添加图标的方式：  
　　1、将其保存在与网站的索引页面相同的目录中，以.ico格式保存。（大多数浏览器将支持更通用的格式，如.gif或.png，但使用ICO格式将确保它能在如Internet Explorer 6一样久远的浏览器显示）  
　　2、将以下行添加到HTML <head>中以引用它： ```<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">```    
　　（图标出现在打开的页面标签页和书签面板中的书签页面）  
  
### 4. 在HTML中应用CSS和JavaScript  
```<link rel="stylesheet" href="my-css-file.css">```  
```<script src="my-js-file.js"></script>```  
\<script\> 部分没必要非要放在文档头部；实际上，把它放在文档的尾部（在 \</body\>标签之前）是一个更好的选择，这样可以确保在加载脚本之前浏览器已经解析了HTML内容（如果脚本加载某个不存在的元素，浏览器会报错）。  

### 5. 为文档设定主语言：```<html lang="en-US">```   
如果HTML文档的语言设置好了，就会被搜索引擎更有效地索引 (例如，允许它在特定于语言的结果中正确显示)，对于那些使用屏幕阅读器的视障人士也很有用(比如， 法语和英语中都有“six”这个单词，但是发音却完全不同)。
* 还可以将文档的分段设置为不同的语言。例如，把日语部分设置为日语：  
```<p>Japanese example: <span lang="jp">ご飯が熱い。</span>.</p>```


