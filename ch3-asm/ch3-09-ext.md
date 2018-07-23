## 3.9. 补充说明

如果是纯粹学习汇编语言，则可以从《深入理解程序设计：使用Linux汇编语言》开始，该书讲述了如何以C语言的思维变现汇编程序。如果是学习X86汇编，则可以从《汇编语言：基于x86处理器》一开始，然后再结合《现代x86汇编语言程序设计》学习AVX等高级汇编指令的使用。

Go汇编语言的官方文档非常匮乏。其中“A Quick Guide to Go's Assembler”是唯一的一篇系统讲述Go汇编语言的官方文章，该文章中又引入了另外两篇Plan9的文档：A Manual for the Plan 9 assembler 和 Plan 9 C Compilers。Plan9的两篇文档分别讲述了汇编语言以及和汇编有关联的C语言编译器的细节。看过这几篇文档之后会对Go汇编语言有了一些模糊的概念，剩下的就是在实战中通过代码学习了。

Go语言的编译器和汇编器都带了一个`-S`参数，可以查看生成的最终目标代码。通过对比目标代码和原始的Go语言或Go汇编语言代码的差异可以加深对底层实现的理解。同时Go语言连接器的实现代码也包含了很多相关的信息。Go汇编语言是依托Go语言的语言，因此理解Go语言的工作原理是也是必要的。比较重要的部分是Go语言runtime和reflect包的实现原理。如果读者了解CGO技术，那么对Go汇编语言的学习也是一个巨大的帮助。最后是要了解syscall包是如何实现系统调用的。

得益于Go语言的设计，Go汇编语言的优势也非常明显：跨操作系统、不同CPU之间的用法也非常相似、支持C语言预处理器、支持模块。同时Go汇编语言也存在很多不足：它不是一个独立的语言，底层需要依赖Go语言甚至操作系统；很多高级特性很难通过手工汇编完成。虽然Go语言官方尽量保持Go汇编语言简单，但是汇编语言是一个比较大的话题，大到足以写一本Go汇编语言的教程。本章的目的是让大家对Go汇编语言简单入门，在看到底层汇编代码的时候不会一头雾水，在某些遇到性能受限制的场合能够通过Go汇编突破限制。
