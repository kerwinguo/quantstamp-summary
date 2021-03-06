# Quantstamp: 智能合约安全协议

~~本来想要直接翻译白皮书，后来发现工作量也不小，写个大概吧。去掉技术细节的晦涩部分，保留方便理解整个系统的部分~~

**Quantstamp是第一个智能合约安全审计协议。** 我们用可以确保智能合约安全性的技术来拓展以太坊。我们的团队是由一群软件测试专家组成，总共超过500个谷歌学者引用。

## 问题
区块链网络是安全的，但是智能合约并不安全。2016年6月，黑客从DAO项目中盗取了价值5500万美元的币，原因是智能合约中的一个缺陷。2017年7月，有黑客从加密公司盗取了价值超过3000万美元的代币，只因为Parity钱包的智能合约代码中的一个单词错误。这些安全问题损坏了对智能合约的信任，进一步也阻碍了以太坊网络被更广泛地使用。

当前人们对审计智能合作做的很不充分。从事安全咨询的公司需要人工专家去审核智能合约。这种处理方式昂贵且容易出错。并且依赖于一个公司，需要相信公司中没有任何坏角色。一个依赖于多种不同角色共识的分布式系统显著地更为安全。

人工审计的处理方式，无法应对智能合约的爆炸式增长。2017年6月到10月，智能合约的数量，从50万增长到了200万。我们可以预期1年内会增长为1000万。这对审计工作会有指数级的增长。如今我们没有足够的安全专家来审计所有的智能合约，并且这个短缺未来会更为严峻。

智能合约失败的潜在代价也会增长。仅仅2017年10月，约有32亿美元(1100万ETH)在智能合约中锁定这。而锁定在智能合约中的美元会随着以太坊和智能合约使用的增长而指数级增长。智能合约中漏洞的潜在带带也会相应增长。

## Quantstamp协议
Quantstamp协议通过创建可伸缩低成本的系统审计所有以太坊网络的网络的智能合约，来解决智能合约的安全问题。随着时间的推移，我们希望每一个以太坊智能合约都使用Quantstamp协议来执行安全审计，安全是最基本的。  

协议包含两部分：
- 一个自动且可升级的软件验证系统，用于检查Solidity程序。分布式SAT解析器会需要大量的算力，但随着时间推移，会捕获到更为复杂的攻击。
- 一个自动的赏金支付系统，用于奖励查找合约缺陷的人工参与者。这个系统的目的，是桥接起通往全自动化目标的隔阂。

Quantstamp协议依赖于参与者们的分布式网络，来减轻坏角色的作用，提供所需的算力，还有提供管治。每一个参与者都使用Quantstamp协议（QSP）令牌来支付，接收，或者提高验证服务。下面是不同类型的参与者。

- **贡献者** 为Solidity验证程序贡献软件，然后获得QSP令牌。所有贡献的带慕都会开源，这样社区可以对效率有所信任。绝大部分的贡献者将会是安全专家。贡献是通过管治机制来投票的。
- **验证器** 运行Quantstamp验证节点并获得QSP令牌。验证着只是贡献计算资源，不需要是安全专家。
- **缺陷寻找者** 提交智能合约缺陷，获得QSP令牌作为赏金。
- **合约创建者** 支付QSP令牌验证以验证智能合约。由于智能合约的数量在爆炸式增长，我们预计合约穿件这的需求也会相应增长。
- **合约使用者** 可以查看智能合约的安全审计结果。
- **投票者** 官职系统是协议的一个核心特性。验证被设计为模块化的并且可以基于令牌持有者的投票来升级。管治机制减少了升级分叉的可能性，也会随着时间推移，去中心化创建团队的影响。

## 动机

我们的团队致力于帮助开发人员编写更可靠的代码，代表多年在软件领域的综合研究和经验验证。将这些专业知识应用于下一代数字技术革命的机会对每个参与的人来说都是非常令人兴奋的。对于更安全的代码，有一个明确而迫切的需求。

智能合同的漏洞已经威胁到区块链技术和数字货币的应用。目前正在进行大量的工作是用来以扩大以太坊的规模，然而我们认为安全同样重要。因为没有智能合同的安全，人们很难信任他们是一种风险资本。我们对未来的展望是智能合约会成为人们使用的主流应用程序，并且会使人们的日常生活更便捷。我们将通过使用确保的技术扩展以太坊来确保智能合同的安全性从而实现智能合同的愿景。 

我们相信自动化的安全审计将帮助开发人员部署公众可以信任的代码，而无需编写包含更多代码行的正式规范除了程序本身。我们的目标是尽可能地自动化检查和属性验证。每一个目标都应该有助于实现一个更健康的区块链生态系统，这个解决方案才是底层标准。 
 
我们的策略是创建一个基本的协议，最终可以直接并入以太坊平台，为第一个以太坊杀手级应用创造一个安全的环境。 
 
本文档的其余部分详细说明了为什么安全协议是必要的技术提升，并提供平台的高级架构。 

## 智能合约改进

我们如何改进智能合同基础设施 该协议允许对智能契约代码进行自动安全检查，并以一个不可靠的方式执行。


### 我们如何改进智能合约架构
### 我们如何改进开发者流程
### Quantstamp示例

## 技术
本实施安全审计的技术建立于对验证算法和区块链技术的前沿研究。其基础系由Quantstamp开发，并经过反复修改的验证器节点，其中包括应用常规方法的分析工作包。
### 校验协议
本安全审计的验证协议将奖励提供给对智能合约进行检查的计算资源的参与者。这些检查由验证器节点运行。该验证协议确保对智能合约的认证是“验证证明”的一部分。
通过引入一个基于以太坊的中介托管/治理智能合约，该系统可以确保计算费用的交易安全。如果接收到的智能合同未通过验证器的验证，托管人将控制交易直到验证完成。如果验证失败，令牌被自动返回发送者或持有至安全违规被修正。
Quantstamp节点是Ethereum网络的合作伙伴。以太坊处理网络和交易协议，而Quantstamp节点处理验证协议，以确保安全审核并将其添加到数据字段或交易。

#### 设计
本验证协议处理分布式计算和一致性。这个协议专注于网络中的节点如何执行自动化软件验证和奖赏奖励机制。
我们协议的核心主张价值在于其无需相互信任并组织坏角色操纵审计结果。它也可以通过QSP令牌的去中心化治理进行升级。这就是我们如何设计协议以实现这些目标。
##### 协议治理
我们计划将Quantstamp协议作为具有治理系统的可升级协议，并且由QSP令牌持有者控制。该套治理系统控制更新验证智能合约和验证节点。验证智能合约被设计为模块化和可升级。如发展路线图所详述，在实现核心功能后，治理制度本身将被添加到智能合约。

一个时间锁定的多重签名被用于管理升级。在提出的途径中，交易可以由任何成员发起，交易被越多成员赞成，越能更早可以执行。一个成员可以投票反对升级，这意味着他会退出一项其他人通过的签名。已经全部成员通过的升级可以在1小时后执行。每5％成员不投票，所需时间翻倍；如果投票反对则增加四倍。
治理是一个关键的功能，因为验证着和贡献者需要升级协议。治理机制降低升级频率，允许协议兼顾贡献者升级和确保用户间的一致性。随着时间推移和贡献者加入社区，去中心化的治理特征允许社区参与并稀释创始团队的影响力。例如：验证者想通过投票改变工作量贡献方式，为了增加收入的潜力；用户想要通过投票引入高并发的算法，让协议更快执行。

##### 加密经济激励
为了防止坏角色操纵系统，我们构建了一个激励机制，其策略在于让发起攻击代价昂贵，以防止流氓验证节点改变审计结果。验证者通过QSP令牌中的交易费激励，处理一部分计算。所提议的协议要求拜占庭容错2/3。如果没有达到2/3的共识，则不支付令牌。我们保留在测试和验证阶段改进此设计的权利。以下部分将更详细地说明容错设计。

##### 对抗攻击与分布式计算
单一的坏成员不能操纵网络，因为其他演员由经济驱动防止攻击。   为了分配我们的计算，每个成员只收到一个整体验证问题的组成部分。对于分布式计算，我们目前在考虑使用t-masking quorum系统，其中两个quorum在至少2t +1服务器中交互。该quorum系统可以处理至少有t个节点的故障系统。由于没有一个演员能够访问整个验证过程，所以通过计算过程的分布进一步阻止了坏的演员。

##### 囚徒困境
在游戏理论中，囚徒的困境是一个悖论，其中两个人以自己的利益为由选择了一种不会导致理想结果的行为。两者都选择牺牲另一方以使自己受益，但两者最终都比通过合作更糟。 

假设发现错误的验证者可以选择不获取赏金，并利用它来获取未来的收益。然而，我们的经济激励措施驱使验证者追求赏金，而不是试图利用错误。验证者若想试图利用错误而不是报告错误，必须假设没有其他验证者会发现同一个错误和报告它，并修复错误。由于难以协调的验证者数量很大，很可能是其他验证者会发现这个错误，然后去获得赏金。因此，该机制设计下，验证者在个人利益驱使下将追求赏金。
### 安全审计引擎

安全审计引擎采用一个非验证的智能合约作为输入，执行自动的安全及漏洞检查并生成报告。验证结果会和一个proof-of-audit（审计证明）哈希结合起来，这个哈希会有一个版本代码从那个版本的安全库中追踪范围检查。

在安全库中运行完整测试所需的时间与智能合约代码的复杂性相关，因此，验证奖励与计算时间成正比。验证者需要奖励来激励其参与这一过程，因此发行令牌让使用者可以使用这些功能。

当知道智能合约被通过共识的方式透明验证时，公众越来越有信心，从而激励开发者使用这些特性。整体信心则会由于尝试找到重大缺陷的赏金猎人的努力得到进一步提升。

此外，随着新的漏洞被发现，安全库将会不断改进和发布新版本。用户将有机会用最新版本的安全库重新验证其使用的智能合约，确保他们的代码不会受到新发现的漏洞的攻击。这类似于软件用户下载补丁修复安全漏洞或用户更新其防病毒软件。

### 架构图

Quantstamp协议（QSP）是一个可扩展的系统来审计所有的基于以太坊的智能合约项目。我们对Quantstamp安全协议的愿景是它将成为以太坊协议其中的一部分。

QSP分为三个概念类别：

1.	基于以太坊的Quantstamp校验智能合约
2.	由被高度修正的以太坊节点组成的Quantstamp网络（QN）
3.	Quantstamp报告（数据承载于智能合约交易中）

QN是一个验证者节点的网络，以共识的方式生成安全报告。作为一种效用，QSP与平台无关——安全库可以有许多变体，其中之一包括Solidity（用于以太坊），以及可能涵盖其他不同平台的智能合约语言的变体。

#### Quantstamp校验智能合约

最终用户可以访问以下功能列表。

注册（）
用户可以注册一个以太坊地址，该地址警告Quantstamp网络监控注册地址的API命令。


审计（）
用户可以为一个安全审计提交源代码以及令牌赏金费用。成功后，智能合约被数字签署以证明其通过关键的安全检查。在此刻，就可以获取一份加密的安全报告。bug赏金仍然在合约上，从而激励查找bug的人，直到到达指定的时间限制。

升级（）
升级现有的智能合同。新版本的智能合同必须通过安全审计。现有的赏金向前滚动。


#### Quantstamp网络

Quantstamp网络（QN）是一种专用协议，能够监视与注册的智能合约相关的、涉及到调用Quantstamp校验智能合约的交易。

#### Quantstamp报告

 “Quantstamp报告”提供了QN执行的安全审计的公开视图。这些报告将通过qsscan.io上的基于Web的用户界面展示。

报告可以是公共的或私人的。每个人都可以看到并阅读到公共报告。注册用户则可以用公共密钥对私人报告进行加密，只有注册用户可以阅读报告的内容。一旦智能合约被部署，智能合约的最终的安全报告是公开的。这样可以让投资者和其他用户在提交资金前查阅这些报告。

智能合约的所有者被鼓励在安全报告中加入注释。智能合约所有者被鼓励对所有已发布的安全警告和被标记的问题进行回复。答复可能是简单的“这是假阳性”或“我们不关心这个问题”，也可能是非常详细的。所有者的责任是向那些想要阅读安全报告来提高信任度的人提供尽可能多的信息。 基于对在安全报告中的发现、赏金的额度、赏金已经生效时间的长度以及社区的反馈，每个智能合约都将被计算得到一个“信任评分”。

### 交换方式
#### 计算机辅助推理工具
##### SAT解析器
##### SMT解析器
#### 模型检查
#### 静态程序分析
#### 符号执行及Concolic testing
### 增量发布和订阅模型
### 缺陷查找器
### 安全泄露策略
### 分布并行SAT
#### 可满足性问题(SAT)
#### 并行SAT解析器
#### 并行SAT与共识
### 以太坊/Solidity的常见漏洞
## 财务计划
## 团队调研贡献
### Demo:定位Parity多方签名漏洞
## 常见问题与解答
## 详细履历
## 附录A
## 附录B
## 附录C






