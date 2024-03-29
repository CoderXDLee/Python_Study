# 04-操作系统简史（科普）

## 目标

* 了解操作系统的发展史
* 知道 Linux 内核及发行版的区别
* 知道 Linux 的应用领域

## 1、操作系统的发展史

### 1.1 Unix

1965年之前的时候，电脑并不像现在这样普遍，它可不是一般人能碰的起的，除非是军事或者学院的研究机构，而且当时大型主机至多能提供30台终端（30个键盘、显示器），连接一台电脑。

![](../.gitbook/assets/da-xing-zhu-ji.png)

**为了解决数量不够用的问题**

* 1965年之后，由 **贝尔实验室** 加入了 **麻省理工学院** 以及 **通用电气公司** 合作的计划：该计划要建立一套 **多用户\(multi-user\)**、**多任务\(multi-processor\)**、**多层次\(multi-level\)** 的 **Multics** 操作系统，想让大型主机支持 300 台终端。
* 1969 年前后这个项目进度缓慢，资金短缺，贝尔实验室退出了研究。
* 1969 年从这个项目中退出的 **Ken Thompson（肯·汤普逊）**当时在实验室无聊时，为了让一台空闲的电脑能够运行 “星际旅行（Space Travel）” 游戏（也是他自己编写的游戏），在8月份左右趁着其妻子探亲的时间，**用了一个月时间**，使用汇编写出了 Unix 操作系统的原型。
* 1970 年，美国贝尔实验室的 **Ken Thompson （肯·汤普逊）**，以 **BCPL** 语言为基础，设计出很简单且很接近硬件的 **B 语言**（取BCPL的首字母），并且他用 **B语言** 写了第一个 Unix 操作系统。
* 1971 年，同样酷爱 “星际旅行（Space Travel）” 的 **Dennis M Ritchie（丹尼斯·里奇）** 为了能早点玩上游戏，加入了 **Ken Thompson** 的开发项目，合作开发 Unix，他的主要工作是**改造 B语言**，因为 **B语言**的跨平台性较差。
* 1972 年，**Dennis M Ritchie（丹尼斯·里奇）**在 **B语言** 的基础上最终设计出了一种新的语言，他取了 BCPL 的第二个字母作为这种语言的名字，这就是 **C语言**。

![Unix &#x521B;&#x59CB;&#x4EBA;](../.gitbook/assets/ken-tang-pu-xun-he-dan-ni-si-li-qi.png)

**C语言**

* 在把  **Unix** 移植到其他类型的计算机上使用时，**C语言**强大的移植性在此显现
  * 机器语言和汇编语言都不具备移植性，为 x86 开发的程序，不可能在 Alpha、SPARC 和 ARM 等机器上运行
* 而 **C 语言**程序则可以使用在任意架构的处理器上，只要那种架构的处理器**具有对应的C语言编译器和库**，然后将 C源代码编译、连接成二进制文件之后即可运行。

[肯·汤普逊](https://zh.wikipedia.org/wiki/%E8%82%AF%C2%B7%E6%B1%A4%E6%99%AE%E9%80%8A)

[丹尼斯·麦卡利斯泰尔·里奇](https://zh.wikipedia.org/wiki/%E4%B8%B9%E5%B0%BC%E6%96%AF%C2%B7%E9%87%8C%E5%A5%87)

**Unix 家谱**

![Unix&#x5BB6;&#x8C31;](../.gitbook/assets/unix.svg)

### 1.2 Minix

* 因为 **AT&T** 的政策改变，在 Version 7 Unix 推出之后，发布新的使用条款，将 Unix 的源码私有化，在大学中不再能使用 Unix 源代码。
* **Andrew S. Tanenbaum（塔能鲍姆）**教授为了能在课堂上教授学生操作系统运作的细节，决定在不使用任何 **AT&T** 的源代码的前提下，自行开发与 Unix 兼容的操作系统，以避免版权上的争议。
* 以 **小型 Unix（mini-Unix）**之意，将它称为 **MINIX**。

### 1.3 Linux

* 1991 年 **Linus （林纳斯）**就读于赫尔辛基大学期间，对 Unix 产生浓厚的兴趣，尝试着在 Minix 上做一些开发工作。
* 因为 **Minix** 只是教学使用，因此功能并不强，**林纳斯** 经常要用他的**终端仿真器（Terminal Emulator）**去访问大学主机上的新闻组和邮件，为了方便读写和下载文件，他自己编写了磁盘驱动程序和文件系统，这些在后来成为了 Linux 第一个内核的雏形，当时，他年仅21岁。
* 林纳斯 利用 GNU 的 bash 当做开发环境，gcc 当做编译工具，编写了 Linux 内核，一开始 Linux 并不能兼容 Unix。
  * 即 Unix 上跑的应用程序不能在 Linux 上跑，即应用程序和内核之间的接口不一致
  * 一开始 Linux 只适用于 386，后来经过全世界网友的帮助，最终能够兼容多种硬件。

![&#x6797;&#x7EB3;&#x65AF;&#xB7;&#x6258;&#x74E6;&#x5179;](../.gitbook/assets/image.png)

\*\*\*\*[林纳斯·本纳第克特·托瓦兹](https://zh.wikipedia.org/wiki/%E6%9E%97%E7%BA%B3%E6%96%AF%C2%B7%E6%89%98%E7%93%A6%E5%85%B9)

