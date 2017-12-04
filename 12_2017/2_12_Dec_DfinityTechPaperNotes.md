# Prologue

1. Daemon contracts?
2. VRF (verifiable random function)

# INtroduction

## 4 layer of  consensus mechanism

1. 1st layer: 身份和注册

所有的矿工都会被注册，拥有永久匿名di

2. 2st: layer: 随机beacon

random beacon 由注册的矿工产生的VRF。
VRF的output是无法被任何人预测，直到它被公开。
VRF是基于 threshold signature (51%)的。 基于BLS签名

3. 3st： 区块链和fort resolution

PSP（probabilistic slot protocal），对矿工进行排序。排序高的矿工的区块获得更高权重
区块分叉的问题：总区块重量相加最重的chain获得胜利。
PSP优势：1.. ranking instantly，可预测的区块时间
		2.. 总是只有一个胜利的矿工。

4. 4st： 公正和接近实时的结算

notarization:加速结算速度。只有公正过的区块可以加入到链。矿工只公正最高顺位的区块（由random beacon算出） 
notarization不是一个共识，可以理解为一个优化的共识。一般来说自由一个block会被公正，最多两个区块就可确认一笔交易。

## threshold relay&& network scalability

一个代表所有注册矿工的committe（随机取样的矿工群 （threshold mechanism, non-interactive））处理 random beacon 和 notarization。 committe会通过threshold relay不停改变

## consistency vs 可用性。(没懂)

# high-level view 共识协议

## roles

dfinity点对点网络包含挖矿客户和轻客户，都被称作：观察者

## committees 和 threshold relay

## 区块排名
random beacon会产生随机数决定注册矿工的排名，这个排名会影响到哪个矿工的区块会被公正。

##notarization：

