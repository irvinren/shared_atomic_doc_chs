欢迎光临共享原子性的文档!
=========================================

<big> 这个模块可以为python程序提供多线程与多进程程序当中所需要的可共享变量的原子操作。

内部提供的类:
- - [atomic_int/原子有符号整数](./原子有符号整数API.md)
- - [atomic_uint/原子无符号整数](./原子无符号整数API.md)
- - [atomic_float/原子浮点数](./原子布尔型浮点型API.md)
- - [atomic_bool/原子布尔型](./原子布尔型浮点型API.md)
- - [atomic_bytearray/原子字节数组](./原子字节数组API.md)
- - [atomic_string/原子字符串](./原子字符串API.md)
- - [atomic_set/原子集合](./原子集合API.md), 需要安装 [bitarray>=2.4.0](https://pypi.org/project/bitarray/).
- - [atomic_list/原子列表](./原子列表API.md), 需要安装 [bitarray>=2.4.0](https://pypi.org/project/bitarray/).

从旧版本继承的CTYPES API可以一直沿用。

系统需求:
- Linux/MacOSX, 
- - 支持 CPython 3.0-3.11, Pypy 3.0-3.9, 
- - 需要 cffi >= 1.0.0, <= 1.1.15, 
- Windows, 
- - 只去持 CPython 3.0-3.11, 不支持 Pypy. 
- - 需要 cppyy >=1.5.0, <=2.3.1, 它使用 [cling](https://github.com/vgvassilev/cling/tree/master/tools/packaging) 作为C++解释器.
- - 多进程模式不支持, 只支持单进程多线程模式.

使用范例, 请浏览 [原子API范例](./原子API范例.md)，[ctypes_API使用范例](./CTYPES范例.md)。

ctypes API 的使用参考, 请浏览 [ctypes API](./CTYPES_API.md).</big>

##

```{eval-rst}
.. toctree::

   原子API范例.md
   CTYPES范例.md
   原子有符号整数API.md
   原子无符号整数API.md
   原子布尔型浮点型API.md
   原子字节数组API.md
   原子列表API.md
   原子集合API.md
   原子字符串API.md
   CTYPES_API.md

 ```
 
 ![Python Logo](https://www.python.org/static/community_logos/python-logo.png)

