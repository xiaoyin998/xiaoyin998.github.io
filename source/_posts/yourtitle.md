---
title: yourtitle
date: 2018-11-04 16:17:49
tags:
---
# hello-world  
## 小创
### 什么是Linux系统，Linux有哪些部分，Linux都用在了哪些地方？   
    Linux是一套免费使用和自由传播的类Unix操作系统，Linux可安装在各种计算机硬件设备中，比如手机、平板电脑、路由器、视频游戏控制台、台式计算机、大型机和超级计算机。其创始人为林纳斯·托瓦兹，于1991 年10 月5 日诞生。系统中的所有都归结为一个文件，包括命令、硬件和软件设备、操作系统、进程等等，Linux是一款免费的操作系统，用户可以通过网络或其他途径免费获得，并可以任意修改其源代码。其完全兼容POSIX1.0标准，这为用户从Windows转到Linux奠定了基础。
Linux支持多用户，各个用户对于自己的文件设备有自己特殊的权利，保证了各用户之间互不影响。多任务则是现在电脑最主要的一个特点，Linux可以使多个程序同时并独立地运行。Linux同时具有字符界面和图形界面。在字符界面用户可以通过键盘输入相应的指令来进行操作。它同时也提供了类似Windows图形界面的X-Window系统，用户可以使用鼠标对其进行操作。Linux由于其稳定性高、完全免费，目前主要用于服务器市场。  
### Linux和Windows有什么区别，Linux有哪些优势？  
       其同时具有字符界面和图形界面，开放源代码，用户可以通过网络或其他途径免费获得Linux，并可以任意修改其源代码，这是windows所做不到的。  
### Linux的基本文件（夹）操作命令有哪些？  
    1.date ：设置系统日期和时间。  
　　2. stty -a: 可以查看或者打印控制字符(Ctrl-C, Ctrl-D, Ctrl-Z等)  
　　3. passwd: print or set the system date and time (用passwd -h查看)  
　　4. logout, login: 登录shell的登录和注销命令  
　　5. pwd: 加载目录。  
    6. more, less, head tail: 显示或部分显示文件内容.  
　　7. lp/lpstat/cancel, lpr/lpq/lprm: 打印文件.  
　　8. 更改文件权限： chmod u+x...  
　　9. 删除非空目录：rm -fr dir  
　　10.拷贝目录： cp -R dir  
　　11. fg jobid :可以将一个后台进程放到前台。  
　　Ctrl-z 可以将前台进程挂起(suspend), 然后可以用bg jobid 让其到后台运行。  
　　job & 可以直接让job直接在后台运行。  
　　12. kill: 向一个进程发送控制信号。  
　　13.卸载： dpkg -r package  
　　14.卸载并删除配置文件: dpkg -P |--purge package  
    15.安装： dpkg -i package  
　　16. 查看软件包安装内容 :dpkg -L package  
　　17.查看文件由哪个软件包提供: dpkg -S filename   
    18. 安装: apt-get install packs  
　　19. apt-get update : 更新源  
　　20.apt-get upgrade: 升级系统。  
　　21. apt-get dist-upgrade: 智能升级。安装新软件包,删除废弃的软件包  
　　22. apt-get -f install ： -f == --fix broken 修复依赖  
　　23. apt-get autoremove: 自动删除无用的软件  
　　24. apt-get remove packages :删除软件  
　　25. apt-get remove package --purge 删除包并清除配置文件  
　　26. 清除删除包的残余配置文件: dpkg -l |grep ^rc|awk '{print $2}' |tr ["/n"] [" "]|sudo xargs dpkg -P  
　　27.安装软件时候包的临时存放目录 : /var/cache/apt/archives  
　　28. 清除该目录: apt-get clean  
　　29. 清除该目录的旧版本的软件缓存: apt-get autoclean  
　　30. 查询软件some的依赖包： apt-cache depends some  
　　31. 查询软件some被哪些包依赖: apt-get rdepends some  
　　32. 搜索软件: apt-cache search name|regexp  
　　33. 查看软件包的作用：apt-cache show package  
　　34. 查看一个软件的编译依赖库: apt-cache showsrc packagename|grep Build-Depends  
　　35. 下载软件的源代码 : apt-get source packagename (注: sources.list 中应该有 deb-src 源)  
　　36. 安装软件包源码的同时, 安装其编译环境 :apt-get build-dep packagename (有deb-src源)  
　　37.将本地光盘加入安装源列表: apt-cdrom add  
　　38. 查看内核版本： uname -a  
　　39. 查看ubuntu 版本: cat /etc/issue  
　　40. 查看网卡状态 : ethtool eth0  
　　41. 查看内存,cpu的信息： cat /proc/meminfo ; cat /proc/cpuinfo  
　　42. 打印文件系统空间使用情况: df -h  
　　43. 查看硬盘分区情况: fdisk -l  
　　44. 产看文件大小: du -h filename;  
　　45. 查看目录大小： du -hs dirname ; du -h dirname是查看目录下所有文件的大小  
　　46. 查看内存的使用： free -m|-g|-k  
　　47. 查看进程： ps -e 或ps -aux -->显示用户  
　　48. 杀掉进程: kill pid  
　　49. 强制杀掉： killall   
       等等。  
### 什么是开源软件，开源社区有哪些，开源软件有什么优势和劣势？  
       开源软件即开放源代码软件，其源码可以被公众使用，并且此软件的使用，修改和分发也不受许可证的限制。  
       开源社区包括开源中国、GoogleCode、GitHub、SourceForge、CodeProject、Apache、ChinaUnix、CodePlex、LUPA、Linux中文社区、51开源社区、Open-Open等。  
       开源软件优点是免费，代码开放，方便其他程序员编辑；缺点是安全性得不到保障。  
### 为什么要有版本控制，git都有哪些操作，和GitHub有什么关系？  
       版本控制可以保证修改文件或代码时不破坏掉修改前的状态；发布软件的时候很多时候会有多个版本，而生成软件的源代码却往往只有一份，只是在最后编译生成的时候用到不同的部分，大部分代码还是共用的，所以往往需要版本控制，几个版本复制几个文件夹出来。  
       git update-index –-skip-worktree [file] 可以实现修改本地文件不会被提交，但又可以拉取最新更改的需求。  
       git update-index --no-assume-unchanged重新跟踪  
       pretty=oneline 每个提交日志信息只显示一行  
       git checkout – readme.txt把readme.txt文件在工作区的修改全部撤销  
       git reset HEAD readme.txt把暂存区的修改撤销掉，重新放回工作区  
       git checkout – readme.txt撤销修改,也就是回到版本库的状态  
       git remote add origin 远程版本库URL：git push -u origin master把本地的master分支和远程的master分支关联起来  
       git log --graph 命令可以看到分支合并图  
       等等。  
       git是软件,它可在本地建立仓库,你写的代码的各个版本都可以存储，github是网上仓库,你写的代码的各个版本都可以存储。
Tom之所以把网站叫做Github，是因为其核心部分版本控制是用Git来处理的。gitHub是一个面向开源及私有软件项目的托管平台，
因为只支持git 作为唯一的版本库格式进行托管，故名gitHub。  
### ARM架构处理器都有哪些，有什么特点，处理器的结构都有哪些，有哪些特点？  
    ARMv7架构的Cortex-A5,A7,A8,A9,A12,A15，ARMv8架构的Cortex-A53,A57，A72。  
    1、体积小、低功耗、低成本、高性能；  
　　2、支持Thumb（16位）/ARM（32位）双指令集，能很好的兼容8位/16位器件；  
　　3、大量使用寄存器，指令执行速度更快；  
　　4、大多数数据操作都在寄存器中完成；  
　　5、寻址方式灵活简单，执行效率高；  
　　6、指令长度固定。  
       CPU从逻辑上可以划分成3个模块，分别是控制单元、运算单元和存储单元。逻辑单元包括指令寄存器、指令译码器、控制单元、寄存器、逻辑运算单元（ALU）、预取单元、总线单元、数据高速缓存。  
       AMD的CPU特点是核心数量多，单核性能低，功耗比较高，性价比比较高；英特尔的CPU的特点是，核心数量少，单核性能强，所以对于绝大多数游戏来说都比AMD的表现要好，功耗低，发热低，比较主流。  
### 为什么在路由器中可以安装Linux，在路由器中使用的Linux和在桌面端使用的有什么区别？  
       Linux支持路由器功能，如OpenWrt、LEDE，都是基于Linux的路由器系统。  
### 为什么要有操作系统？  
       操作系统是一种驱动程序。让人们不需要关心一些硬件细节，就可以使用硬件。  
       可享使用硬件资源；为使用者指定一些规范，让不同的使用者可以共享使用硬件。  
       操作系统就是为了让人们更加方便的使用硬件资源的一个工具，让我们更好地使用硬件资源各种硬件资源。  
### 自己对计算机分层思想的理解。  
       分层思想主要就是将一个复杂的计算机网络分开管理，各个层实行相应的功能，便于管理，和标准的实行。分层思想是一种模块化设计，总的来说就是为了方便。
### UART串口通信的层次结构是怎样的？  
       起始位：先发一个逻辑“0”信号，表示传输的开始  
       数据位：紧接着起始位，从低位开始传动，发送速率靠时钟确定  
       停止位：数据位加上这一为使得“1”的位数为偶数（偶校验）或奇数（奇校验），以此来校验数据的正确性  
       停止位：一个字符数据的结束标  
       空闲位：处于逻辑“1”状态，表示当前线路没有数据传输。  
### 为什么Qt可以跨平台使用而VS不能，C语言的编译步骤是怎样的，常用的编译器有哪些？  
       针对每一种OS平台，QT都有一套对应的底层类库，而接口是完全一致的，因此只要是在QT库上开发的程序，放在任何一种平台下都可以编译运行。  
      【第一步】编辑hello.c  
       1 #include <stdio.h>   
       2 #include <stdlib.h>   
       3 int main()   
       4 {   
       5 printf("hello world!\n");   
       6 return 0;   
       7 }  
      【第二步】预处理  
        预处理过程实质上是处理“#”，将#include包含的头文件直接拷贝到hell.c当中；将#define定义的宏进行替换，同时将代码中没用的注释部分删除等。  
       （1）将所有的#define删除，并且展开所有的宏定义。说白了就是字符替换  
       （2）处理所有的条件编译指令，#ifdef #ifndef #endif等，就是带#的那些  
       （3）处理#include，将#include指向的文件插入到该行处  
       （4）删除所有注释  
       （5）添加行号和文件标示，这样的在调试和编译出错的时候才知道是是哪个文件的哪一行  
       （6）保留#pragma编译器指令，因为编译器需要使用它们。  
       【第三步】编译  
       （1）词法分析，  
       （2）语法分析  
       （3）语义分析  
       （4）优化后生成相应的汇编代码  
       【第四步】链接  
常用的编译器：  
        Cygwin、Mingw32、DJGPP、Dev-C++、GNU C++、MSC 5.0、6.0、7.0、MSQC 1.0、2.5、MSVC 1.0、4.2、6.0、7.0、Visual C++等等。  
### C语言中主函数的返回值可以返回什么东西，主函数的参数又是如何确定的？  
       main函数的返回值用于说明程序的退出状态。如果返回0，则代表程序正常退出。返回其它数字的含义则由系统决定。通常，返回非零代表程序异常退出。返回值为1的时候则代表程序运行遇到问题失败。  
       主函数的第一个参数是一个整数，它表示第二个参数里的指针个数，主函数的第二个参数是一个字符指针数组，其中每个指针代表一个字符串，所有这些字符串的内容都来自于用户的命令。  
       argc是命令行总的参数个数，argv[]是argc个参数，其中第0个参数是程序的全名，以后的参数命令行后面跟的用户输入的参数，char *argv[]是一个字符数组,其大小是int argc,主要用于命令行参数，  
char*envp[]用来取得系统的环境变量。