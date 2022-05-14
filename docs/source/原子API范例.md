# 原子API范例（多线程多进程混合）:

使用本模块需如下步骤:

1) 创建子进程所需要的函数, 子进程当中可以创建多线程.

   `def process_run(a):`

   `     def subthread_run(a):`
   
   `         a.array_sub_and_fetch(b'\x0F')`

   `     threadlist = []`
   
   `     for t in range(5000):`
   
   `         threadlist.append(Thread(target=subthread_run, args=(a,)))`

   `     for t in range(5000):`
   
   `         threadlist[t].start()`

   `     for t in range(5000):`
   
   `         threadlist[t].join()`

2) 创建共享字节数组

    `    a = atomic_bytearray(b'ab', length=7, paddingdirection='r', paddingbytes=b'012', mode='m')`

3) 启动这些进程与线程并利用共享字节数组

    `    processlist = []`
    
    `    for p in range(2):`
    
    `        processlist.append(Process(target=process_run, args=(a,)))`

    `    for p in range(2):`
    
    `        processlist[p].start()`

    `    for p in range(2):`
    
    `        processlist[p].join()`

    `    assert a.value == int.to_bytes(27411031864108609,length=8,byteorder='big')`

