### 面向对象

* 基本特征：抽象（abstract）、继承（inherit）、多态（Polymorphism）
* 实例方法、类方法（@claasmethod）、静态方法（@staticmethod）
* 构造设计{JAVA、C++等} = 创建（__new__） + 初始化（__init__） {python} 

### 异常处理

* except Exception as ret : 
		print (ret)
* else / finally
* ""(空字符)、None、[]、{} 、 0都是为假，其它有值（如非0）均为真

### 模块使用

* 主程序不调用子模块测试部分：
	`if __name__ == '__main__':
		main()`

* 包：在包文件夹里面添加__init__.py文件
	并在__init__.py文件添加语句：
	__all__ = ["所需的模块1","所需的模块2"]  #(对from 包 import *)
	from . import 所需的模块1,所需的模块2

* import 包 路径顺序：
	当前路径 --> os.__file__下的路径

* *模块的发布、安装:*
* 发布：
 1. 在包相同目录下建立setup.py文件
 2.	`from distutils.core import setup`

	`setup(name="", version="1.0", description="", author="", py_modules=['包.模块1', '包.模块2', '包.模块3'])`

 3. 命令行输入python3 setup.py build
 4. 命令行输入python3 setup.py sdist

* 安装:
	解压后，命令行输入sudo python3 setup.py install

#