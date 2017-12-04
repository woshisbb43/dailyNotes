# Dfinity: Blocchain Nervous System

## why we do this (Raison d’être）

1. Bitfinex theft. 

Tradational code is law blockchain network can hardly prevent this.

2. the dao and faulty systems

2. Accelerating evolution

quicker release?

### 应用。
（no concept of hard fork）
dfinity 将ethereum client 封装起来，让Dapps通过反向代理连接这些client。 反向代理知道BNS的存在，并接受BNS的指示进行系统升级，协议更新（当前是硬分叉）等操作。当BNS指示区块链在某个高度升级时，反向代理会暂时缓存各种Dapp的用户请求，并自动进行升级。这样就不会打扰用户。
（我的理解是，这样的操作，可能在现有区块链上是不可能实现的？ **BNS指示**）

4. More security and better economics

### 威胁

bitocin，ehterum 采用简单的经济学模型，币价通常是币需求的直接，主要体现。所以当需求大幅波动，投机盛行时，币价会出现周期性的，不稳定的大幅波动。

proof-of-work 耗电来决定谁厉害。 proof-of-stake比的是谁拥有token数量多。对于dfinity这种准POS系统，就会比较危险：如果大盘蹦了，那么坏人就能很轻松的用比较少的资源产生：有资质注册了的的矿工。

BNS可以解决这个问题：在大盘要崩掉的时候，BNS可以通过改变一些系统中的经济参数来实现对系统稳定性的控制。比如说提升POS的定金数量（增加坏人控制的难度），提升挖矿奖励（不知道为啥），暂时冻结新矿工入场（把坏人挡在门外）。

5. killing assassination markets， et al

### 例如奴隶市场，这种应用，我们该怎么禁止

BNS 可以冻结这些邪恶的人Dapp，帮助政府进行相应调查等。 （这真的是一个trade off）。需要谨慎考虑


## how it works

1. 创建 Neurons
任何人（我估计是mining client）可以跑neurons，并赚取（thought mining）。如何创建：

- client向bns打一定数量的代币
- 在三个月的时间内帮助进行decision making （防止垃圾proposal）

2. 赚取奖励（thought mining）

奖励和client在BNS内存储的押金是成比例的。 也和在一定时间内参与的decision making成比例。
举个例子：假设BNS的回报百分比是10%。
如果一个neuron压了100dfinity，在1000个区块高度内参与了所有decision making，那么他获得10dfinity作为回报。如果参与了5%的decision making，那么获得5dfinity作为回报。

3. 跑neurons

neuron建立时有两个key生成：**delegate** 和 **master**
delegate key 允许neuron投票， master key 用作化解neuron (??),取回deposit， 或者授权新 delegate。

4. 人工投票

如果有个proposal（economics, policy, protocol, client upgrades...）还没被决定，那么neurons就可以进行投票。投票的比重同样由押金决定。用户可以通过：adopt， reject， pass三种选择进行投票。

5. 通过Follows机制自动投票

大部分neuron 的所有人，可能并不愿意每个proposal都去进行投票。而且也不是所有的proposal都适合投票，比如说important & complex protocol改变。让没有专业知识的人进行这方面的投票也挺危险的。所以可以通过跟随投票机制，在不同领域选择自己认为**可以做出正确选择**的neuron使用自己的投票权。

6. Follow图和级联至决定。

有一个细节：（Voting power is easily hidden — a person can publicize a neuron containing a single dfinity, and follow it with another private neuron containing their main deposit.） 不知道为啥？？？ 
上文是neurons 会在很多地方发布自己的广告。

如果一个neuron controller 在timeout前没有人工投票且没有Follow任何人，那么BNS会查看在某一话题中优先级最高（权重最大）的neuron是否投票了，投了的话会跟他一起。若没投看top two neurons的投票情况。

7. acting on decisions

passive action & active action.

passive action 处理伤筋动骨的事情，例如更改protocol, 更改neuron规则的宪法，更改挖矿回报等等

active action 处理一些可以直接处理的东西。例如BNS可以接受：冻结某个smartcontract （例如slave market）的 proposal

8. proposal fees 和 押金

有的porposal可能会用到大量的资源，因此BNS会收费。 proposal 会分几个阶段被evaluate：
- 人工检查interiry 例如到proposal的twitter， reddit去看是否属实
- 验证确实是问题，并检查代码。多个人工validator 需要参与并分析并确认。
- 这些人工检查员可以是bns雇佣的人。








