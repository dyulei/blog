Selector APIs
============

方法
----

###1.getElementById("ID")

通过指定的 `id` 属性值搜索目标元素。

可用于：

+ document

返回值：
>node

###2.getElementsByName("name")

通过指定的 `name` 属性值搜索目标元素。

可用于：

+ document

返回值：
>nodeList

###3.getElementsByClassName("class")

通过指定的 class 属性值搜索目标元素。

可用于：

+ document
+ element

返回值：
>nodeList

###4.getElementsByTagName("tag")

通过指定的 HTML tag 搜索目标元素。

可用于：

+ document
+ element

返回值：
>nodeList

###5.querySelector("selector")

通过指定的 selector 搜索目标元素。

可用于：

+ document
+ element

返回值：
>node

###6.querySelectorAll("selector")

通过指定的 selector 搜索目标元素。

可用于：

+ document
+ element

返回值：
>nodeList

返回值
------

###1.node

单个节点，可直接访问其属性或调用其方法。

###2.nodeList

节点列表，类似于数组。nodeList.length 属性代表了节点的个数。可以通过处理数组的方法访问每个节点。

行为
----

以下四个方法的返回值是 __动态__ 的：

+ getElementById("id")
+ getElementByName("name")
+ getElementsByClassName("class")
+ getElementsByTagName("tag")

当 HTML 文档结构发生改变时，函数的返回值可能会改变。示例代码：

	// HTML
	<p class="target">1</p>
	<p>2</p>
	// JS
	var target=document.getElementsByClassName("target");
	var len=target.length; // len=1
	// 修改 <p>2</p> 的 class
	document.getElementsByTagName("p")[1].className="target";
	// 重新读取 target.length
	len=target.length; // len=2

另外两个方法只会读取执行时的文档状态：

+ querySelector("selectors")
+ querySelectorAll("selectors")

示例代码：

	// HTML
	<p class="target">1</p>
	<p>2</p>
	// JS
	var target=document.querySelectAll(".target");
	var len=target.length; // len=1
	// 修改 <p>2</p> 的 class
	document.getElementsByTagName("p")[1].className="target";
	// 重新读取 target.length
	len=target.length; // len=1
