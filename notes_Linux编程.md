### 调试方法
* pdb调试
python -m pdb xxx.py

l ---> list 显示当前代码
n ---> next 向下执行一行代码
C ---> continue 继续执行代码
b ---> break 添加断点
clear ---> 清除断点
s ---> step 进入函数
p ---> 打印一个变量的值
a ---> args 打印所有的形参数据
q ---> quit 退出调试
r ---> return 快速执行到函数的最后一行

* 交互调试
	pdb.run("func(args)")

* 程序里埋点
	pdb.set_trace()

* 日志调试

### 编码风格
pep8编码规范

### 进程
* fork
	os.fork() #创建新进程
	os.getpid() #当前进程号
	os.getppid() #父进程号

	fork炸弹

* Process
	from multiprocessing import Process
![Process用法](.\Process.PNG)