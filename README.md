# dom-note
This repository is used to record the note of leaning dom.
## 1. 事件流
事件流描述的是从页面中接受事件的顺序。  
IE的事件流是事件冒泡流，而Netscape的事件流是事件捕获流  
![事件流](http://wx2.sinaimg.cn/mw690/006epDUlgy1fvqqwfuuddj30qt0fymxp.jpg)  
### 1.1 DOM事件冒泡
事件冒泡  
事件冒泡，即事件最开始由最具体的元素(文档中嵌套层次最深的那个节点)  接收，然后逐级向上转播至最不具体的节点(文档)。  
![事件冒泡](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqqwg91wcj30va0akdgh.jpg)  
### 1.2 DOM事件捕获
事件捕获  
事件捕获的思想是不太具体的节点应该更早接收到事件，而最具体的节点最后接收到事件。  
![事件捕获](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqqxwslrnj30tm09q3yw.jpg)  
## 2. 事件处理程序
### 2.1 HTML事件处理程序
![html](http://wx1.sinaimg.cn/mw690/006epDUlgy1fvqqzu94n4j30uq0bgmxx.jpg)  
### 2.2 DOM0级事件处理程序
![图](http://wx2.sinaimg.cn/mw690/006epDUlgy1fvqr26w5p9j30pq04xwet.jpg)  
![代码](http://wx2.sinaimg.cn/mw690/006epDUlgy1fvqr27dmesj30ur0dxmy2.jpg)  
### 2.3 DOM2级事件处理程序
DOM2级事件定义了两个方法：用于处理指定和删除事件处理程序的操作：`addEventListener()`和`removeEventListener()`。它们都接收三个参数：要处理的事件名、作为事件处理程序的函数和一个布尔值。 
![图](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqr5qd262j30pt063gma.jpg)  
![代码](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqr5rank7j30v10hh402.jpg)   
### 2.4 IE事件处理程序
`attachEvent()`添加事件  
`detachEvent()`删除事件  
这两个方法接收相同的两个参数：事件处理程序名称与事件处理函数  
![ie](http://wx1.sinaimg.cn/mw690/006epDUlgy1fvqr8yepk7j30mk03t74e.jpg)  
![代码](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqr8y1fxtj30se0fn0u8.jpg)  
### 2.5 跨浏览器的事件处理程序
![代码](http://wx1.sinaimg.cn/mw690/006epDUlgy1fvqrbns5roj30lc0gnq48.jpg)  
## 3. 事件对象
事件对象`event`  
![事件对象](http://wx1.sinaimg.cn/mw690/006epDUlgy1fvqrebnk51j30jo03jq2w.jpg)  
### 3.1 DOM中的事件对象
1. `type`:获取事件类型  
2. `target`：事件目标  
3. `stopPropagation()` 阻止事件冒泡  
4. `preventDefault()` 阻止事件的默认行为  
![dom](http://wx4.sinaimg.cn/mw690/006epDUlgy1fvqrg38rh4j30ei05tdfy.jpg)  
### 3.2 IE中的事件对象
1. `type`:获取事件类型  
2. `srcElement`：事件目标  
3. `cancelBubble=true`阻止事件冒泡  
4. `returnValue=false`阻止事件的默认行为  
![ie](http://wx1.sinaimg.cn/mw690/006epDUlgy1fvqriq7nzjj30h207kaac.jpg)  
## 其他
该仓库中`/index.html`为html元素文件，`/js/event.js`为封装后多浏览器兼容的获取元素的js文件，
`/script/script.js`为浏览器加载完成后执行的js操作文件。
## 参考来源：
[慕课网DOM事件探秘](https://www.imooc.com/learn/138)  

