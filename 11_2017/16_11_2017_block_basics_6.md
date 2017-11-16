# 区块链上的账本

上篇文章中，我们介绍了分布式系统所面临的问题和困境（**Intergrity**和**信任**）。在接下来的几篇文章中，我会先介绍一些区块链的基础知识，为更好的理解区块链技术是如何解决分布式系统问题打好基础。

## 我的可乐

一个简单的例子：有一天我手里拿着一瓶在小卖部买的可乐去商场购物，结账时售货员告诉我：你这瓶可乐是我们商场拿的，也要交钱。我就不乐意了，这明明是我自己带的，凭啥交钱。我肯定不想多交这份钱，于是我要证明给这个售货员这个可乐是我自己带的。那么问题来了，我该怎么证明这瓶可乐是我自己带的呢？

## 所有权 证人

为了证明这瓶可乐是我带进超市的（所有权），我把小卖部的大爷叫了过来当我的证人，和售货员对质。于是售货员开始问这个大爷各种问题：大爷你能记得这个人吗？大爷你卖的是可口可乐还是百事可乐？大爷。。。（MMP）最后大爷完全正确的回答对了所有问题并对天发誓说的都是真话。售货员又问道：大爷，你是不是收这人钱了，怎么能记得一清二楚。

发现了么，虽然有个证人帮我证明我对可乐的所有权，但是售货员并不是很相信这个大爷。那假如我有10个证人证明我的所有权呢？售货员应当很快就能相信这瓶可乐一开始就是我的。

实际上，多个证人是区块链的核心概念之一，在后文中，我会详细解释为什么此概念如此重要。

## 所有权

我们继续来讨论所有权的问题。我们抽象一下上面例子告诉我们的：证明所有权需要三个要素：

1. 所有者的证明（例如身份证）
2. 物品的证明
3. 所有者和物品间的映射（可以简单理解为两者的联系）

正如上面例子所示，有个证人就可以证明物品的所有权，这可能是最最最古老的证明所有权的方式。但是这真的挺麻烦的，所以先民发明了纸和笔之后就用文件来记录身份和所有权了。还是用例子来说明：我打算在京东买个Iphone，我先注册个京东账号（实名认证），然后买了个Iphone，京东给我开了发票，交易就算完成了。这个例子中我在京东实名认证的账号就是我的所有者证明，而Iphone本身的UDID（设备唯一标识符）就是物品的证明，而发票就是从我（所有者）到我购买的Iphone的UDID的映射。这三个元素一起就可以证明Iphone是我的了。（假装自己买了个IphoneX哈哈）。

发票是所有者和物品之间的映射的一个简单例子，生活中还有很多此类映射，例如记账本，注册表等等（为了阅读方便，后文中我用记账本代替所有者和物品间的映射）。记账本会在一比交易发生的同时更新，更新的是所有者的证明，也可能是物品。例如我通过微信转给小明100块，微信的记账本（假设所有微信间转帐都记录在这个记账本上）就会更新：我少了100，小明多了100。

现在大家应该清楚了生活中**记账本**是如何证明我们对物品的所有权的，那么这个所谓的**记账本**在区块链中有怎么样的作用呢？

## 所有权 区块链

接着上面转账的例子，故事继续发展下去：第二天早上起来，我突然发现自己的微信钱包少了1000块钱，我去问小明怎么回事，小明告诉我他只收到了100块钱啊，可能是微信**记账本**出错了吧。于是我打电话问微信客服，这怎么一回事，微信客服查了**记账本**后告诉我说：记账本记错了。记错了？记错了！这么重要的东西怎么能记错呢！

不知道大家发现了没有，上面的例子只有一个记账本，而这个记账本**出错了**。惊不惊喜，意不意外？如果微信拒不承认记账本出错了，我不是白白亏了900块钱？这可怎么办？要是我这里也有个微信记账本的**副本**就好了，如果小明那里也有个**副本**的话我们就可以一起向微信出示使我俩的记账本，证明我只转出了100块。假如微信想抵赖，我们二对一数量占优势，少数服从多数，微信记账本该听我们俩记账本的。**民主的胜利** :)

光想没用，回到家我就开始开发一套系统，下午就开发好了（假装自己是个软件高手，其实我们币知道却是都是技术牛）。这套系统连接了我的手机，微信服务器，小明的手机。三者各自维护一个**记账本**，这个系统确保了三个记账本的数据一致，而且在三个记账本间进行转账是十分安全可靠的。

不知不觉中，我开发了一个极其简易的区块链雏形。上面例子中我开发的系统就是个区块链系统；我的手机，小明手机，微信服务器是区块链上的节点；**记账本**就是区块链节点上维护的数据。

至此，我们介绍了什么事区块链上的**记账本**。在下一篇文章中，我带大家了解什么是双发问题。

