---
title: 比特币的隐私性
---

社会的数字化进程不断向前，互联网上暴露的关于你我的数据越来越多，也越来越事关生死。密码朋克宣言的第一句话就说“隐私对于构建开放社会是非常必要的”，那么比特币的隐私性如何呢？下面来讨论下。

## 肉身和账户隔离

比特币的隐私策略就是隔离比特币地址和持有者的肉身身份。

比特币的隐私保护策略跟传统金融系统的策略截然不同的。比特币白皮书的第十部分是专门介绍隐私的，中本聪提到传统机构的策略是在机构内部绑定用户的肉身身份和他们的账户，隐私性体现在公众是不能随意获取这些信息的。而比特币采用了相反的思路，公众可以看到所有的转账记录，其中包括发送和接收方的比特币地址、转账金额等信息。而比特币的隐私体现在比特币的地址跟地址持有者的肉身身份之间是没有绑定关系的。

但是，真正做到肉身身份和比特币地址的分离是非常困难的。中本聪建议大家每次交易都去更换一下比特币地址，但是这样就真的能够隔离身份和地址了吗？

## 交易是可追踪的

比特币是人类历史上最透明的一个支付系统，所有的交易历史都会被保留，这种特质给比特币的隐私安全带来了极大的挑战。

一旦暴露再次隐身就变得很难。实际中有很多场合都会涉及到实名制的问题，实名制意味着肉身身份和我们的地址被绑定了，也就是这个地址的隐私被暴露了。而一旦最初的这个地址暴露以后，即使我们更换一个新的地址，把暴露地址中的币转入新地址，新地址和老地址之间关联性就非常明显，所以新的地址也就没有隐私性可言了。

另外一个更让人担忧的事情是即使我自己遵守了最佳实践，没有暴露隐私，如果跟我交易的地址隐私泄露了，从那个地址的持有者的身上找到我的身份信息也就会比较容易了。

交易在全网的扩散过程也可能会暴露隐私。比特币交易被创建后，会从构建交易的机器上按照点对点传播协议逐步扩展到网络上的很多计算机上，这时候如果想定位交易最初是从哪台机器上发出的，其实没有那么容易。但是，不容易不代表没可能，如果监听者同时去监听网络上的很多节点，记录下我的交易到达各个节点的时间，那么根据时间差，还是很有可能运算出发出交易的节点的位置的。对此，比特币也提出了一个名为 [Dandelion](https://github.com/bitcoin/bips/blob/master/bip-0156.mediawiki) 的改进方案，但是在我写本文的时候（2019年1月），这个方案还处在草案阶段。

综上，比特币的隐私性是不足够好的。

## 解决方案

为了获得更强的隐私性，加密货币社区一直在不停的努力。

最引人注目的是一些基于零知证明或者其它技巧的隐私币项目。例如，Zcash 和门罗币，这样的项目是独立的区块链项目发行的自己的加密货币。

比特币社区内部也在思考各种改进方案。例如，由核心开发团队提出的 Confidential Transaction 以及 Coinjoin 。后来有人结合这两项技术，提出一套新的加密货币协议，名为 [Mimblewimble](mimblewimble) 。Mimblewimble 暂时还没有被比特币项目采纳。但是实现了 Mimblewimble 的独立区块链项目有两个： [Grin](grin) 和 Beam 。

其它的方案还有不少，这里就不一一说了。

## 总结

关于比特币隐私性的讨论主体内容就这些了，总结起来主要有这样几个要点：首先，比特币本身主张通过隔离肉身身份和比特币地址这种方式来保证用户隐私。其次，由于交易全部公开可追踪，所以要真正通过比特币实现隐私，实际中是很难的。最后，社区提出了各种方案来增进加密货币的隐私。

参考：

- https://bitcointalk.org/index.php?topic=279249.0