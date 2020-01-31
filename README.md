# C++11线程池

## 已经实现的功能

	1. corePoolSize个数的核心线程(核心线程不会退出),并根据任务量最大扩展到maxPoolSize个
	2. 线程池线程数=corePoolSize+提交的线程数量(submit和execute),不会超过maxPoolSize
	3. 可以设置线程数量
	4. 可以判断线程池状态
	6. 可以使用execute和submit提交任务(两种方式有差别)
	7. 可以设置线程回收策略也可以手动回收非core线程
	8. 线程回收策略使用的是thread.join(),可以避免线程资源无法释放
	9. largestPoolSize是线程池使用过的线程数

## TODO

	1. 实现interruptible_thread--不使用interruptible_thread
	2. 实现workStealingThreadPool
	3. 实现Executors工厂函数
	4. 实现ScheduledThreadPool 

## 用法
	1. 类似Java Executor
	2. 例子:example文件夹下

## 参考
	1. JDK1.8源码
	2. C++并发编程实战

## change log

	1. 实现线程池动态可伸缩--未使用interruptible_thread,利用join()将线程释放后移出线程队列
