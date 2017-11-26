# Filecoin 常见问题

## Filecoin 基础及概念

### Filecoin的商业模型是什么？竞争对手是谁？盈利点在哪里？对投资者有什么好处？

在币圈中，IPFS 和 Filecoin已经无人不晓，但是大家还是有很多关于Filecoin和IPFS的问题，因此我们在此介绍一些相关的基本概念以及常见问题。

1. 作为未来的分布式存储系统，我们需要做到十分好才可以和现有的传统存储系统比肩，要做的非常好才能超越他们并更好地服务于互联网客户。举例来说：确保数据的完整性（不丢失用户数据），确保系统无停机（用户可随时获取数据），降低系统延迟（提升存取速度）。因此，建立一个云存储系统并非易事，也绝非一朝一夕可以完成的。我们认为Filecoin协议可以为以上问题提供非常好的解决方案，但同时，我们也清醒的认识到，去建立这个云存储系统会需要很多专家学者长时间的努力。所以如果作为投资者，你并不了解并认可Filecoin的概念以及潜力，请谨慎投资。

2. 主要的竞争对手包括了AWS S3, Google 云, Microsoft Azure, 阿里云等。

3. 作为一个还未完全成熟，并且潜力巨大的技术，Filecoin以及IPFS投资有很多的盈利点以及想象空间。因为Filecoin的价值是和Filecoin存储系统直接相关的。Filecoin分布式云存储系统的使用广度，使用深度，用户数量都会直接影响到Filecoin的价值。但是随着Filecoin逐步的普及，矿工数量的持续增长，市值的不断增高。投资Filecoin或进行Filecoin的可见利润会越来越高。

## Filecoin 技术概念

### 为什么我们要建Filecoin原生区块链。

对Filecoin项目之前有过了解的人都知道，我们原计划在以太坊上建立一个虚拟链来支撑Filecoin系统（详情参考Devcon 2）。不过今年3月，我们的团队解决了一个非常重要且底层的问题：使用Proof-of-Replication（复制量证明）和Proofs-of-Spacetime（时间空间占有证明）产生Filecoin的Proof-of-Work（工作量证明）。这个重大突破意味着Filecoin网络可以自己建立一个区块链网络并使用Proof-of-Work（空间时间证明）来确保区块链网络的安全运作。因此，我们的团队认为建立Filecoin底层区块链网络非常必要。同时，我们会确保Filecoin会和Ethereum兼容。

### 什么是有用的工作量证明

主流区块链网络通常使用基于计算能力的共识协议，例如比特币和以太坊。在这些网络中，大家使用机遇哈希能力的算法保持网络的正常运行。不同于这些主流区块链网络，Filecoin使用Proof-of-Spacetime（时间空间证明）共识协议，可以看作是一种有用的Proof-of-work（工作量证明）。说该协议是有用协议是因为该协议可以证明矿工，参与者确实在其硬件设备上进行了Filecoin网络文件的存储。比起比特币使用哈希能力来进行工作量证明，我们认为Filecoin的时间空间证明更能体现存储方面的工作量证明。

## IPFS 技术概念

### Filecoin 和 IPFS是什么关系？

Filecoin使用整套IPFS协议栈，例如libp2p, IPLD等。Filecoin讲使用IPFS协议去处理，分发网络上的文件及数据。Filecoin提出并使用刺激模型，该模型能够帮助IPFS节点存储，备份，服务Filecoin网络中的文件和数据。

### Filecoin 和 IPFS如何共同运行？

Filecoin节点包括IPFS节点，因此它们会同时使用IPFS协议。其他IPFS节点给某一节点发送文件存取请求时，该请求会被执行IPFS协议的Filecoin节点所执行。

### Filecoin 和 以太坊的关系

Filecoin将会应用以太坊的技术栈河以太坊区块链网络本身。具体的实现方式是Filecoin将会使用一个原生以太坊合约进行同以太坊的通信。在可见的未来中，我们会致力于开发包含以太坊和Filecoin的混合节点，更好地进行数据存取服务。因为Filecoin是以太坊强有力的支持者，我们将竭力进行同时基于以太坊和Filecoin的开发。

## Filecoin 网络中的公平原则

### 我并不是一个政府认可的投资者，我如何投资Filecoin区块链应用？

Filecoin是一个官方承认的区块链应用，因此我们只接受政府认可的投资者（offering of SAFTs under US Reg D, 506(c)）参与ICO。这对Filecoin的合法性，发展都是好事，然而可能会阻碍了一些希望投资Filecoin，却不是政府认可的投资者。但是ICO并非投资Filecoin的唯一途径。除却ICO，大家还可以通过以下方式参与Filecoin，并获得相应报酬。

1. **挖矿** Filecoin矿工是Filecoin能够在未来成功的关键。他们可以帮助进行数据的存取，建立共识，完成交易并增强Filecoin系统的安全。所以Filecoin对矿工有特别的优待：**70%**的Filecoin币将会分发给Filecoin矿工，作为对矿工的奖励。这些分发到矿工手中的币将会在Filecoin区块链网络上线之后

2. **开发** Filecoin欢迎大家共同维护Filecoin的代码库，并丰富Filecoin的生态环境。所有Filecoin的代码都会在github上开源，希望各位开发者踊跃参与其中。



