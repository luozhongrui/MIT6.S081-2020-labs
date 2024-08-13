# Lab1: Xv6 and Unix utilities

## sleep


**YOUR JOB**
实现 xv6 的 UNIX 程序 `sleep`：您的 `sleep` 应该暂停到用户指定的计时数。一个滴答(tick)是由 xv6 内核定义的时间概念，即来自定时器芯片的两个中断之间的时间。您的解决方案应该在文件 `user/sleep.c` 中

## pingpong
**YOUR JOB**
编写一个使用UNIX系统调用的程序来在两个进程之间`“ping-pong”`一个字节，请使用两个管道，每个方向一个。父进程应该向子进程发送一个字节;子进程应该打印`<pid>: received ping`，其中`<pid>`是进程ID，并在管道中写入字节发送给父进程，然后退出;父级应该从读取从子进程而来的字节，打印`<pid>: received pong`，然后退出。您的解决方案应该在文件`user/pingpong.c中`。

## Primes
**YOUR JOB**

使用管道编写prime sieve(筛选素数)的并发版本。这个想法是由Unix管道的发明者Doug McIlroy提出的。请查看这个网站(翻译在下面)，该网页中间的图片和周围的文字解释了如何做到这一点。您的解决方案应该在`user/primes.c`文件中。


## find
**YOUR JOB**

写一个简化版本的UNIX的`find`程序：查找目录树中具有特定名称的所有文件，你的解决方案应该放在`user/find.c`

## xargs
 **YOUR JOB**
编写一个简化版UNIX的`xargs`程序：它从标准输入中按行读取，并且为每一行执行一个命令，将行作为参数提供给命令。你的解决方案应该在`user/xargs.c`