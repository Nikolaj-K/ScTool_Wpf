# ScTool_Wpf

ScTool 是 SmartContract Tools 的简写，是一套NEO智能合约调测工具。
嗯，他是一套工具。包含两组服务器和前端，全部都开源。

一组服务器叫做RemoteSharpContractBuilder,暂时存放在SmartContractBrowser 项目中。

另一组服务器是一个定制的 neo cli 节点,暂时存放在neo-gui-nel 项目中。

目前我们只部署了TestNet的服务API，由于我们的服务器是开发使用，经常会做各种操作。如果你喜欢这套工具，我们建议你自己部署服务。

我们直接采用了前后端分离的设计，是因为请求开发Web工具集的呼声很高。
我们已经准备好为Web开发工具集的API。

## 功能

这套工具目前主要有两个功能

1.C# online编译器

![](image/pic1.png)
将代码复制进来，或者在这里编写。若生成成功，你的源码、avm、abi文件、map文件 会被保存在服务器上。
任何人均可查看。

这个编译器基于远程API工作，所以他可以开发一个Web版本
![](image/pic2.png)
我们建立了一个范例。

最终，我们会提供一整套的Web开发工具。

2.智能合约交易调试工具

另一个功能是针对一个具体的交易，查看他的执行细节
![](image/pic3.png)
如图我们刚刚发起了一笔交易
![](image/pic4.png)
然后在调试工具中输入交易ID即可查询交易执行的细节。
如果调用链中包含你用我们的C#online编译器编译的合约，我们还能自动帮你下载到源码，并对应。

这里有你需要的一切信息。
执行栈和计算栈上的值在每一步的时候的情况。
有哪些Syscall被调用。
Notify Log 这些都不在话下。

3.其他可能性

实际上，你也可以利用这套调试工具去开发特色的爬虫，收集NEO区块链上不为人所知的秘密。
我们可以准确的判定一个智能合约交易的行为，完全基于链上真实执行情况。

## 使用方法
   
编译功能的使用方法：写代码->按编译按钮->看到结果并自动保存在服务器

调试功能的使用方法：输入txid->按load按钮->看结果

GoodDay.


