# linux笔记
## 1. linux发展史
  - 在1981 年，IBM 公司推出了享誉全球的微型计算机IBM PC。
  - 在1981-1991 年间，MS-DOS 操作系统 一直是微型计算机操作系统的主宰,此时软件价格仍然居高不下。
  - 当时的一个计算机技术阵营就是UNIX 世界。但是为了寻求高利润率，UNIX 经销商们把价格抬得极高.
  - 此时，出现了MINIX 操作系统，并且有一本描述其设计实现原理的书 同时发行。AST的这本书写的非常详细，并且叙述得有条有理，于是几乎全世界的计算机爱好者都开始看这本书，以期能理解操作系统的工作原理。
  - 1991 年，Linus Benedict Torvalds 是赫尔辛基大学计算机科学系的二年级学生，也是一个自学的计算机hacker。这个21岁的芬兰年轻人喜欢鼓捣他的计算机，测试计算机的性能和限制。但当时他所缺乏的就是一个专业级的操作系统。
  - 在同一年间，GNU 计划已经开发出了许多工具软件。其中最受期盼的GNU C 编译器已经出现，但还没有开发出免费的GNU 操作系统。 即使是教学使用的MINIX 操作系统也开始有了版权，需要购买才能得到源代码。
  - 1991年4月开始，Linus 几乎花费了全部时间研究MINIX-386 系统(Hacking the kernel)，并且尝试着移植GNU 的软件到该系统上(GNU gcc、bash、gdb 等)。并于4 月13 日在comp.os.minix 上发布说自己已经成功地将bash 移植到了MINIX 上。
  - 第一个与Linux 有关的消息是在1991 年7 月3日 在comp.os.minix 上发布的（当然，那时还不存在Linux 这个名称，当时Linus 脑子里想的名称可能是FREAX，FREAX 的英文含义是怪诞的、怪物、异想天开等）。其中透露了他正在进行Linux 系统的开发，并且已经想到要实现与POSIX 兼容的问题了。
  - 在Linus 另一个发布的消息中(1991 年8 月25日 comp.os.minix)，他向所有MINIX 用户询问“Whatwould you like to see in minix?”(“你最想在MINIX系统中见到什么？”)，在该消息中他首次透露出正在开发一个(免费的)386(486)操作系统，并且说只是兴趣而已，代码不会很大，也不会象GNU 的那样专业。
     希望大家反馈一些对于MINIX 系统中喜欢哪些特色不喜欢什么等信息，并且说明由于实际和其它一些原因，新开发的系统刚开始MINIX 很象（并且使用了MINIX的文件系统）。并且已经成功地将bash(1.08版)和gcc(1.40 版)移植到了新系统上，而且在过几个月就可以实用了。
     最后，Linus 申明他开发的操作系统没有使用一行MINIX 的源代码；而且由于使用了386 的任务切换特性，所以该操作系统不好移植（没有可移植性），并且只能使用AT 硬盘。对于Linux 的移植性问题，Linus当时并没有考虑。但是目前Linux 几乎可以运行在任何一种硬件体系结构上。
  - 到了1991 年的10 月5 日 ，Linus 在comp.os.minix 新闻组上发布消息，正式向外宣布Linux 内核系统的诞生（Free minix-like kernel sources for 386-AT）。这段消息可以称为Linux 的诞生宣言，并且一直广为流传。因此10 月5 日对Linux社区来说是一个特殊的日子，许多后来Linux 的新版本发布时都选择了这个日子。
  
  ## 2. linux主要版本
   Linux的发行版本可以大体分为两类，一类是商业公司维护的发行版本，一类是社区组织维护的发行版本，前者以著名的Redhat(RHEL)为代表，后者以Debian为代表。
   下面介绍一下各个发行版本的特点：
    - Redhat，应该称为Redhat系列，包括RHEL(Redhat Enterprise Linux，也就是所谓的Redhat Advance Server，收费版本)、FedoraCore(由原来的Redhat桌面版本发展而来，免费版本)、CentOS(RHEL的社区克隆版本，免费)。Redhat应该说是在国内使用人群最多的Linux版本，甚至有人将Redhat等同于Linux，而有些老鸟更是只用这一个版本的Linux。所以这个版本的特点就是使用人群数量大，资料非常多，言下之意就是如果你有什么不明白的地方，很容易找到人来问，而且网上的一般Linux教程都是以Redhat为例来讲解的。Redhat系列的包管理方式采用的是基于RPM包的YUM包管理方式，包分发方式是编译好的二进制文件。稳定性方面RHEL和CentOS的稳定性非常好，适合于服务器使用，但是Fedora Core的稳定性较差，最好只用于桌面应用。

　　- Debian，或者称Debian系列，包括Debian和Ubuntu等。Debian是社区类Linux的典范，是迄今为止最遵循GNU规范的Linux系统。Debian最早由Ian Murdock于1993年创建，分为三个版本分支(branch)： stable, testing和unstable。其中，unstable为最新的测试版本，其中包括最新的软件包，但是也有相对较多的bug，适合桌面用户。testing的版本都经过unstable中的测试，相对较为稳定，也支持了不少新技术(比如SMP等)。而stable一般只用于服务器，上面的软件包大部分都比较过时，但是稳定和安全性都非常的高。Debian最具特色的是apt-get /dpkg包管理方式，其实Redhat的YUM也是在模仿Debian的APT方式，但在二进制文件发行方式中，APT应该是最好的了。Debian的资料也很丰富，有很多支持的社区，有问题求教也有地方可去:)

　　- Ubuntu严格来说不能算一个独立的发行版本，Ubuntu是基于Debian的unstable版本加强而来，可以这么说，Ubuntu就是一个拥有Debian所有的优点，以及自己所加强的优点的近乎完美的Linux桌面系统。根据选择的桌面系统不同，有三个版本可供选择，基于Gnome的Ubuntu，基于KDE的Kubuntu以及基于Xfc的Xubuntu。特点是界面非常友好，容易上手，对硬件的支持非常全面，是最适合做桌面系统的Linux发行版本。

　　- Gentoo，伟大的Gentoo是Linux世界最年轻的发行版本，正因为年轻，所以能吸取在她之前的所有发行版本的优点，这也是Gentoo被称为最完美的Linux发行版本的原因之一。Gentoo最初由Daniel Robbins(FreeBSD的开发者之一)创建，首个稳定版本发布于2002年。由于开发者对FreeBSD的熟识，所以Gentoo拥有媲美FreeBSD的广受美誉的ports系统——Portage包管理系统。不同于APT和YUM等二进制文件分发的包管理系统，Portage是基于源代码分发的，必须编译后才能运行，对于大型软件而言比较慢，不过正因为所有软件都是在本地机器编译的，在经过各种定制的编译参数优化后，能将机器的硬件性能发挥到极致。Gentoo是所有Linux发行版本里安装最复杂的，但是又是安装完成后最便于管理的版本，也是在相同硬件环境下运行最快的版本。

　　- 最后，介绍一下FreeBSD，需要强调的是：FreeBSD并不是一个Linux系统!但FreeBSD与Linux的用户群有相当一部分是重合的，二者支持的硬件环境也比较一致，所采用的软件也比较类似，所以可以将FreeBSD视为一个Linux版本来比较。FreeBSD拥有两个分支：
　　stable和current。顾名思义，stable是稳定版，而current则是添加了新技术的测试版。FreeBSD采用Ports包管理系统，与Gentoo类似，基于源代码分发，必须在本地机器编后后才能运行，但是Ports系统没有Portage系统使用简便，使用起来稍微复杂一些。FreeBSD的最大特点就是稳定和高效，是作为服务器操作系统的最佳选择，但对硬件的支持没有Linux完备，所以并不适合作为桌面系统。
