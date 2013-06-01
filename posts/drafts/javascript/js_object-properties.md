对象的属性
=======

_属性_ 可以是任意标识符。当属性中存在空格或连字符（-）是，属性必须用字符串表示：

	var people={
		"first name":"Junqing",
		"last name":"Hu"
	};

_属性值_ 可以为任意的对象或原始值：

	var computer={
		"disk":{
			capacity:500,
			type:"SSD"
		}
	};

对象是动态的，刻意随意地 _添加和删除属性_ ：

	line.color="#AAF"; // 为 line 对象添加 color 属性
	？？
内置属性
--------

自定义属性
----------

属性的特征
----------

对象的数据属性包含四个特征：

+ 值（value）
+ 可写（writable）
+ 可枚举（enumerable）
+ 可配置（configurable）

对象的存取器属性也包含四个特征：

+ 读取（get）
+ 写入（set）
+ 可枚举（enumerable）
+ 可配置（configurable）

存取器属性没有值，其可写特征由是否存在 setter 决定。

获取属性的特征描述：

	Object.getOwnPropertyDescriptor(obj.prop);

数据属性的返回值：

	{value: value, writable: true|false, enumerable: true|false, configurable: true|false}

存取器属性的返回值：

	{get: getter, set: setter, enumerable: true|false, configurable: true|false}
	
如果属性为继承属性，或属性不存在，则返回 undefined。

设置属性特征：

	Object.definePeoperty(obj,prop,{descriptor});
	Object.definePeopertys(obj,{prop,descriptor});

属性可以是已存在的，也可以新建属性。

属性操作
--------

###1.查询

获取对象的属性值，有两种方式：

	var x=point.x; // 获取 point 的 x 属性，等同于 point["x"]
	var name=people["first name"]; // 获取 people 的 first name 属性

两种方式是等同的，第二种方式的方括号中为属性名的字符串形式。当属性名为字符串形式时，只能使用第二种方式。

如果访问的属性不存在，则返回 undefined。

###2.设置

对应于属性的查询方式，属性的设置方式也有两种：

	point.x=10; // 等同于 point["x"]=10
	people["first name"]="Junqing";

如果设置的属性不存在，则为对象 _新建属性_ 。

###3.getter 和 setter

getter 和 setter 所对应的属性称为“存取器属性”，它们是用来读写属性的方法。

存取器属性的定义：

	var num={
		x:1,
		y:2,
		get sum(){
			return this.x+this.y;
		},
		set sum(value){
			this.x=this.y=value;
		}
	};

sum 同时作为 num 的属性，以及属性的读取和设置函数。（当仅有 get 方法时，该属性为只读属性）

存取器属性的使用：

	var n=circle.r; // 获取 num 的 sum 属性
	num.sum=5; // 设置 num 的 sum 属性

###4.删除

使用 delete 操作符，可以从对象中删除属性：

	delete point.x; // 删除 point 的 x 属性

delete 操作是能删除对象的自有属性，不能删除继承的属性。

###5.检测

in 操作符可以检测指定的属性是否属于对象：

	"x" in point; // true x 属性属于 point 对象
	"z" in point; // false z 属性不属于 point 对象

hasOwnProperty() 方法可以检测指定的属性是否是对象的自有属性：

	point.hasOwnProperty("y"); // true y 是 point 的自有属性

类似于 in 操作，可以直接判断某个属性是否为 undefined，来确定它是否存在：

	point.x !== undefined; // true point 中包含 x 属性

###6.遍历（枚举）

object.propertyIsEnumerable() 可以检测对象的属性是否可枚举。

使用 for/in 循环，可以遍历对象的所有属性：

	// 声明对象
	var o={
		x:1,
		y:2
	};
	// 遍历属性，读取属性值
	for(p in o){
		console.log(p+":"+o[p]);
	}

__注意：__ 读取到的属性名为字符串形式，只能通过 o[p] 访问对应的属性值。

Object.keys(obj) 可以获取包含 obj 对象中 _可枚举的_ 自有属性名称的数组：

	Object.keys(o);
	// 返回 ["x","y"]

Object.getOwnPropertyNames(obj) 可以获取包含 obj 对象 _所有_ 自有属性名称的数组。