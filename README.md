# javascript_note
学习笔记
1. javascript 包含 ECMA BOM DOM
2. javascript 类型 字符串string 数字number 布尔值boolen 都是小写
3. javascript 的复合类型,所有的复合类型都是引用类型  

|类型|描述|
|:-:|:-:|
|Array|数组|
|Date|日期|
|Number|数字|
|String|字符串|
|Boolean|布尔值|
|Object|对象|
|RegExp|正则表达式|
|Math|数学公式|
|Function|函数|

> 这里引出一个函数

```javascript
/*操作符：in
*@return: boolean
*语法：'name' in object
*对象就是一个键值对的集合
*鸭子辨型
*重要：值类型和引用类型
*/
example:
	var student = {'name':'lilei'}
	var s1 = 'name';
	var s2 = 'age';
	console.log(s1 in student);

	result: true

```

* 引申：其他方法判读对象是否存在该属性

* 方法1:

```javascript

	if (s1 in student){}

```
* 方法2：

```javascript

	var has = false;

	for (var k in student){
		if(k==s1){
			has = ture
		}
	}
```
* 方法3：
```javascript

	if (student.age){

	}else{


	}
```
* 方法4：
```javascript

	if (student[s1]){

	}else{
	}
```

* 按值传递：将变量中的数据完整的拷贝一份，赋值给新的变量

example1:

```javascript
	var str = '123';
	//此时内存中有2个123的副本
	var str1 = str;
	console.log('str='+str+',str1='+str1);
	str = '456';
	console.log('str='+str+',str1='+str1);
	
	/*
	str=123,str1=123
	str=456,str1=123
	*/
```
* 引用类型：变量中存储的是数据的地址

example2:

```javascript
	var o = {'n':'123'}
	var o2 = o
	//内存中只有一个数据对象，将o的地址复制一份赋值给o2,既o2和o共享同一个数据

	console.log('o.n='+o.n+',o2.n='+o2.n)
	o.n = '456'
	console.log('o.n='+o.n+',o2.n='+o2.n)
	/*
		o.n=123,o2.n=123
		o.n=456,o2.n=456
	*/

```
example3: 一个特殊的函数，很重要的技巧

```javascript
	
	
	//判断num是否存在，如果存在就输出num,否则就输出没有参数 
	//方法一
	function fn(num){
		if(num !== undefined){
			console.log(num)
		}else{
			console.log('没有参数')
		}
	}
	//方法二：三元运算符
	function fn2(num){
		num !== undefined ? console.log(num):console.log('没有参数')
	}
	//方法三：短路
	function fn3(num){
		//如果num存在，就直接赋值给num,否则就是赋值后面的
		num = num || '没有参数'
	}
	//方法四：&& 这个方法一般用作能力检测
	//表达式1 && 表达式2 && 表达式3
	//如果第一个表达式为假，就返回第一个表达式，如果为真就返回第二个表达式
	



```
example4: delete

```javascript
	
	/*
	语法：boolean delete 数据
	1.删除数组元素，相当于把对应的键值所在的数据变成undefined,数组长度本身不发生变化
	2.删除对象的属性和方法
	3.删除没有用var声明的变量
	*/


```
