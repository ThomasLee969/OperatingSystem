# 进程间同步/互斥问题

## 银行柜员服务问题

### 问题描述

银行有 n 个柜员负责为顾客服务，顾客进入银行先取一个号码，然后等着叫号。当某个柜员空闲下来，
就叫下一个号。

编程实现该问题，用P、V操作实现柜员和顾客的同步。

### 实现要求

1.	某个号码只能由一名顾客取得；
2.	不能有多于一个柜员叫同一个号；
3.	有顾客的时候，柜员才叫号；
4.	无柜员空闲的时候，顾客需要等待；
5.	无顾客的时候，柜员需要等待。

### 实现提示

1.	互斥对象：顾客拿号，柜员叫号；
2.	同步对象：顾客和柜员；
3.	等待同步对象的队列：等待的顾客，等待的柜员；
4.	所有数据结构在访问时也需要互斥。

### 测试文本格式

测试文件由若干记录组成，记录的字段用空格分开。记录第一个字段是顾客序号，第二字段为顾客进入
银行的时间，第三字段是顾客需要服务的时间。

下面是一个测试数据文件的例子：

    1 1 10
    2 5 2
    3 6 3

### 输出要求

对于每个顾客需输出进入银行的时间、开始服务的时间、离开银行的时间和服务柜员号。

### 思考题

1.	柜员人数和顾客人数对结果分别有什么影响？
2.	实现互斥的方法有哪些？各自有什么特点？效率如何？