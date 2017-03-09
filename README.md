# Android Nougat 源码分析

作者: 郭孝星<br/>
邮箱: guoxiaoxingse@163.com<br/>
博客: https://guoxiaoxing.github.io/<br/>
简书: http://www.jianshu.com/users/66a47e04215b/latest_articles<br/>

**关于作者**

>郭孝星，非著名程序员，代码洁癖患者，爱编程，好吉他，喜烹饪，爱一切有趣的事物和人。

**关于文章**

>作者的文章都会同时发布在个人博客和简书博客上, 文章顶部也会附上文章的Github链接。如果文章中有什么疑问欢迎发邮件与我交流, 对于交流的
问题, 请描述清楚并附上代码与日志, 一般都会给予回复。如果文章中有什么错误, 也欢迎斧正。如果你觉得本文章对你有所帮助, 也欢迎去star文章,
关注文章的最新的动态。

<img src="https://github.com/guoxiaoxing/android-framework-source-code-analysis/raw/master/art/android_7_nougat.jpg"/>

**写在前面**

>之前看过很多Android框架层的源码以及分析源码的书籍，但都是零零散散的不成系统，作为一个 Android 开发人员，
自上而下的 Android 底层源码的功力还是很重要的，从今天开始我就对整个 Andriod 框架层的源码和原理做个系统的
分析，虽然 对于 Android 源码的分析，很多前辈都写过，但之所以会有这个系列的文章，一来 Android 的源码也在
不断的变化目前已经到 Android 7.0 Nougat，本系列文章会针对最新的代码进行分析，二来就是源码分析的过程是比
较枯燥的，本系列的文章会一种独特的视角来减轻大家在阅读源码时的负担，好了，让我们开始吧。

这是本系列博客的第一篇文章，后续的每篇文章都会配上详尽的类图、时序图、示例代码，每大章节还是设立导读PPT。

Android 的源码是多名伟大工程师智慧的结晶，不可谓博大而精深，所以我们在学习之前，要掌握相关的基本技术，欲工
其事，必先利其器，我们需要掌握以下的技术。

**代码版本**

>[android-7.1.1_r1](https://source.android.com/source/build-numbers.html#source-code-tags-and-builds)

**分析思路**

>以某一个支线为起点，从上层往底层，不断地追溯，在各个模块、文件、方法之间来回跳转，反复地阅读，理清整个流程的逻辑。
同时带着思考去看源码，去揣测作者的用意，去理解代码的精妙之处，去思考代码可能存在的缺陷，去总结优秀的代码设计思想。


本系列文章由下至上，从内核层到框架层再到应用层，从内核空间到用户空间，全面的分析内部的实现原理和设计思路。在源码的分析过程中，还会穿插分析源码的
设计模式与编程思想，以下为后续文章的具体安排。

**Android系统架构图**

<img src="https://github.com/guoxiaoxing/android-framework-source-code-analysis/raw/master/art/android_system_architecture.jpg"/>

**Android系统基础篇**

>本篇章从Android源码的下载与编译开始，讲述HAL、智能指针等底层原理。

- [1 Android系统基础篇：基础理论与常用工具](https://github.com/guoxiaoxing/android-open-source-project-analysis/blob/master/doc/Android系统基础篇/1 Android系统基础篇：基础理论与常用工具.md)
- [2 Android系统基础篇：源码下载与编译](https://github.com/guoxiaoxing/android-open-source-project-analysis/blob/master/doc/Android系统基础篇/2 Android系统基础篇：源码下载与编译.md)
- 3 Android系统基础篇：硬件抽象层
- 4 Android系统基础篇：智能指针

**Android系统驱动篇**

**Android系统应用篇**

- 第一章 Andriod 系统架构概述
- 第二章 Android UI 框架
- 第三章 Android 应用资源管理框架
- 第四章 Android 应用程序框架
- 第五章 Binder 进程间通信
- 第六章 Logger 日志系统
- 第七章 Ashmem 匿名共享内存系统
- 第八章 Webkit
- 第九章 OpenGL|ES
- 第十章 Android 多媒体系统
- 第十一章 Android 定位系统
- 第十二章 Android 安全机制
- 第十三章 硬件抽象层
- 第十四章 ART/Dalvik 虚拟机
