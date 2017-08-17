### 导入包的相对路径:
	import sys
	sys.path
	sys.path.append("相对路径")

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

### 迭代:
	from collections import Iterable
	