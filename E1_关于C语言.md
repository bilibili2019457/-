# [1. 程序的基本概念](http://akaedu.github.io/book/ch01.html)

## 1. 程序和编程语言

**1. 程序是什么？（定义与构成）**

- **定义**：告诉计算机怎么做事的指令集合（处理数学、符号、声音、图像——底层全是数字）。
- **四大金刚（指令类型）**：输入、输出、基本运算、测试与分支、循环。任何复杂软件都由这几种简单指令组成。
- **编写方法**：把复杂任务层层拆解，直到能用上述简单指令实现（大问题拆小问题）。

**2. 编程语言是什么？（分类与层级）**

- **低级语言（硬件说话）**：机器语言（纯数字）和汇编语言（助记符）。与硬件一一对应，不可移植，难写但执行快。
- **高级语言（人说话）**：C/C++/Java/Python。用语句写，可移植（平台无关），好写好读。
- **翻译官**：高级语言要转成低级语言才能执行。转法有两种——
  - **编译器（Compile）**：一次性全翻译完，生成可执行文件（如 .exe），之后直接跑（如 C 语言）。
  - **解释器（Interpret）**：边翻译边执行，不生成独立文件，逐行运行（如 Shell 脚本）。

**3. 终极对比（编译 vs 解释）**

- **编译**：**速度快**（提前翻好了），但**换台电脑要重新编译**。
- **解释**：**跨平台牛**（装好解释器就能跑），但**执行速度慢**（边翻边跑浪费时间）。

**4. 语言进化（补充分类）**

- 1~2代：机器/汇编；3代（C/Python）：命令式（告诉怎么一步步做）；4~5代（SQL）：声明式（告诉要什么，具体步骤不管）。

>@ALPS 习题 : 解释执行的语言相比编译执行的语言有什么优缺点？
>
>
>
>解释性的语言，是一行一行的翻译的， 而编译型语言是一次性全部编译。所以编译语言的 "翻译速度会更快"。 但是解释器，它是能够迅速跨平台， 因为本质上它是一种语言的一行一行的翻译， 装好解释器就能直接翻译。 

>无论是解释性语言，还是编译性语言， 其实都有一定的跨平台性。只是解释器是一行一行翻译的， 会更强一点。

>python， Java 本质还是用C语言写的， 我认为，他们到底来说，还是要让让计算机知道人在说什么，做什么， 要说什么， 要做什么。 所以还得编译成机器语言。 那我就觉得， 吗， 解释器更像是一层对翻译的封装， 本质是一种预处理， 一行一行处理完了， 还得编译。

## 2. 自然语言和形式语言

>告诉你，计算机语言对就是对， 错就是错。是一种严格的语言表达方式。

## 3. 程序的调试

### Bug 的分类

编译时错误

运行时错误 

逻辑错误和语义错误

## **4. 第一个程序**

~~~C
#include <stdio.h>

int main(void)
{
        printf("hello world!\n");
        return 0; 
}
~~~

~~~shell
alps@Alps:~/linux_learning$ gcc main.c
cc1: fatal error: main.c: No such file or directory
compilation terminated.
alps@Alps:~/linux_learning$ ls
Uint_1
alps@Alps:~/linux_learning$ cd Uint_1/
alps@Alps:~/linux_learning/Uint_1$ ls
main.c
alps@Alps:~/linux_learning/Uint_1$ gcc main.c
alps@Alps:~/linux_learning/Uint_1$ ls
a.out  main.c
alps@Alps:~/linux_learning/Uint_1$ ./a.out 
hello world!
alps@Alps:~/linux_learning/Uint_1$ 
~~~

### @ALPS 习题

>1、尽管编译器的错误提示不够友好，但仍然是学习过程中一个很有用的工具。你可以像上面那样，从一个正确的程序开始每次改动一小点，然后编译看是什么结果，如果出错了，就尽量记住编译器给出的错误提示并把改动还原。因为错误是你改出来的，你已经知道错误原因是什么了，所以能很容易地把错误原因和错误提示信息对应起来记住，这样下次你在毫无防备的情况下撞到这个错误提示时就会很容易想到错误原因是什么了。这样反复练习，有了一定的经验积累之后面对编译器的错误提示就会从容得多了。

## [2. 常量、变量和表达式](http://akaedu.github.io/book/ch02.html)

### 转义字符 ： 

| \'   | 单引号'（Single Quote或Apostrophe） |
| ---- | ----------------------------------- |
| \"   | 双引号"                             |
| \?   | 问号?（Question Mark）              |
| \\   | 反斜线\（Backslash）                |
| \a   | 响铃（Alert或Bell）                 |
| \b   | 退格（Backspace）                   |
| \f   | 分页符（Form Feed）                 |
| \n   | 换行（Line Feed）                   |
| \r   | 回车（Carriage Return）             |
| \t   | 水平制表符（Horizontal Tab）        |
| \v   | 垂直制表符（Vertical Tab）          |

# [3. 简单函数](http://akaedu.github.io/book/ch03.html)

# [4. 分支语句](http://akaedu.github.io/book/ch04.html)

# [5. 深入理解函数](http://akaedu.github.io/book/ch05.html)

# [6. 循环语句](http://akaedu.github.io/book/ch06.html)

# [7. 结构体](http://akaedu.github.io/book/ch07.html)

# [8. 数组](http://akaedu.github.io/book/ch08.html)

- # [9. 编码风格](http://akaedu.github.io/book/ch09.html)

# [11. 排序与查找](http://akaedu.github.io/book/ch11.html)

# [12. 栈与队列](http://akaedu.github.io/book/ch12.html)

# [13. 本阶段总结](http://akaedu.github.io/book/ch13.html)

# [14. 计算机中数的表示](http://akaedu.github.io/book/ch14.html)

# [15. 数据类型详解](http://akaedu.github.io/book/ch15.html)

# [16. 运算符详解](http://akaedu.github.io/book/ch16.html)

# [21. 预处理](http://akaedu.github.io/book/ch21.html)

# [23. 指针](http://akaedu.github.io/book/ch23.html)

# [24. 函数接口](http://akaedu.github.io/book/ch24.html)

# [25. C标准库](http://akaedu.github.io/book/ch25.html)

# [26. 链表、二叉树和哈希表](http://akaedu.github.io/book/ch26.html)