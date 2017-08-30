	#-*- coding:utf-8 -*-
	#coding = utf-8

### 导入包的相对路径:
	import sys
	sys.path
	sys.path.append("相对路径")

### dir() #查看对象的方法

### 深拷贝、浅拷贝:
	import copy
	a = [11, 22, 33]
	b = copy.deepcopy(a)

### 面向对象
	property(getter,setter)的使用

* 装饰器:

		@property  #getter
		def num(self):
			return self.num

		@property.setter  #setter
		def num(self,newNum):
			self.num = newNum

### 动态添加属性以及方法:
		import types
		obj.func = types.MethodType(func, obj) #绑定
		obj.func() #调用

### __slots__ = ("property1", "property2")
	锁定对象只能添加的属性

### 生成器:
	1. 函数加入yield 变成生成器
	next() 或 .__next__() 调用生成器时，超出后异常名为StopIteration

	2. .send() 替代 yield 传递的值

	3. 多任务: 共三种。协程、进程、线程。

### 迭代器:
		from collections import Iterator

		isinstance('abc', Iterable) #判断能否迭代
		isinstance('abc', Iterator) #判断是否迭代器

* iter() 把列表、元组等转换为迭代器

### 闭包:
	
### 装饰器：
* 封闭：已实现的功能代码块
* 开放：对扩展开发

* 通用装饰器:

	def func(functionName):
		def func_in(*args, **kwargs):
			print("-----Notes------")
			ret = functionName(*args, **kwargs)
			return ret
		return func_in

* 作用域:
	LEGB规则	

### 元类:
	ORF映射
	obj_name = type("obj_name", (父类), {属性(字典)}) 

### GC(Garbage collection)垃圾回收
	1. 引用计数机制为主
	2. 分代回收为辅 (循环引用)

* 导致引用计数+1情况：
	1. 对象被创建
	2. 对象被引用
	3. 对象被作为参数，传入到一个函数中
	4. 对象作为一个元素，存在容器中

* 导致引用计数-1情况：
	1. 对象的别名被显式销毁，dle
	2. 对象的别名被赋予新的对象
	3. 一个对象离开它的作用域
	4. 对象所在容器被销毁，或从容器中删除对象

### 内建方法:
	range()
	map()
	filter()
	reduce()
	sorted()

### functools
	functools.partial #偏函数

	@functools.wraps(func)

### 模块进阶
常用标准库:
hashlib
	m = hashlib.md5()
	m.update(b"code") #encode
	m.hexdigest() #decode

扩展库:
beautifulsoup4