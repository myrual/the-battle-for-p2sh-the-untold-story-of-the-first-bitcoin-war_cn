---
title: "P2SH的战争 比特币世界的第一场战争"
date: 2022-01-30T15:02:13+08:00
draft: false
---
[英文原文](https://bitcoinmagazine.com/technical/the-battle-for-p2sh-the-untold-story-of-the-first-bitcoin-war)

[本翻译稿 Github repo](https://github.com/myrual/the-battle-for-p2sh-the-untold-story-of-the-first-bitcoin-war_cn/blob/main/The_Battle_For_P2SH_The_Untold_Story_Of_The_First_Bitcoin_War.md)

翻译：DeepL，Google Translate 校对： 李林

```
“推迟两个月。OP_EVAL还没好。”
```
这正是Gavin Andresen长久努力要避免的判决。随着发自Russell O'Connor键盘的一声斥责，历时数月的比特币升级工作--创始人中本聪退出后的第一次升级--在实施前突然停滞。

正如O'Connor所揭示的，拟议的命令--被Andresen誉为通往更安全的比特币钱包的 "最快路径"--可以被利用来创建交易，使软件在试图验证它们时进入一个无限循环。

简而言之，OP_EVAL可以被滥用，使比特币节点崩溃，从而使比特币网络崩溃。

O’Connor写道："我花了70分钟的时间才找到这个错误，"他谴责了这个流程：将坏代码合并--并几乎将其推入正在运作的软件。"你们需要停手，真正去了解比特币。"

这是该项目新任负责人Andresen的第一个严重挫折，他迅速提出抗议。在他看来，放弃OP_EVAL不仅会浪费几个月的编码和审查，而且会让用户没有工具来保护他们的数字钱包免受木马和病毒的侵害。

这是OP_EVAL吸引人的核心--简单的多签钱包将允许用户恢复比特币，即使是在备份丢失的情况下；可以建立服务来发送类似银行的警报，阻止欺诈和盗窃；更好的是，这一切都可以在交易中实现，其外观和行为与用户所知道和理解的一样。

但O’Connor的警告之词对那些看到他们对不断升级的发展速度的担忧得到验证的人来说已经足够了。

"我想提醒大家，我们正在搞一个价值2000多万美元的东西，"开发者Alan Reiner会写道。"这不仅仅是一个软件的问题--无论什么东西都需要像钻石一样坚硬。"

OP_EVAL的失败还将产生更大的影响。中本聪确实推出了世界上第一个去中心化的数字货币，但它的承诺远未实现。在2011年底，很少有人理解它的代码，更少有人拥有保护它的技能和熟悉程度。

这些开发者应该如何组织？他们对用户有什么责任？在不清楚谁--如果有的话--应该有最终决定权的情况下，他们将如何进行变革？

这样的问题很快就会在比特币软件的第一场大战中被推到前台。

## 非正统的继承
自由和开源代码码项目通常由创始人领导，而他们又必须与他们的工作所依赖的贡献者保持一致。不过，在出现方向性争议的时候，他们被赋予了一种天然的权威，作为他们创作的决策人。

比特币，在早期也不例外。在比特币存在的头两年，中本聪扮演着主要开发者和仁慈的独裁者的角色。作为比特币无可争议的领导者，他颁布了多达八项协议变更，而没有形成更广泛的讨论[[1](https://blog.bitmex.com/bitcoins-consensus-forks/)]。也就是说，直到他逐渐退出这个项目。


到2010年底，中本聪将把他们的假名从Bitcoin.org网站上抹去，留下资深的三维图形开发人员Gavin Andresen作为项目的 "事实上的领导者"[[2](https://soundcloud.com/twistartups/bitcoin-discussion-with-gavin)]。

Andresen选择的措辞是恰当的，因为围绕这一过渡的情况是不寻常的，相当于一个简短的公共信息，一个私下的职责传递和交换一个允许用户发送全系统警报信息的密钥。


不过，在当时，这对比特币的小规模但不断增长的程序员群体来说没有什么困难。大多数人都关心关键的修复问题，而Andresen，一位终身教授的配偶，有时间和热情来领导这项工作[[3](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/BANLkTimZ5j7%253D1G89uRO9f7fHPdmDMpLMqg%2540mail.gmail.com/#msg27661223)]。

的确，有许多迫切的需求--更快的同步，更好的测试--但 "越来越多的钱包被盗报告"和盗贼提交的"烂补丁"迅速成为首要关注的问题。

有一段时间，这是比特币的新贡献者们似乎都同意的目标[[4](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201106&viewday=13)]。

## 纯多签
幸运的是，中本聪已经提供了一个解决方案的蓝图。正如Andresen所了解的，比特币的代码已经使用户能够创建安全的交易，这些交易只有在用多个私钥签名时才能使用[[5](https://bitcointalk.org/index.php?topic=38903.0)]。

有了多重签名，或简称多签，私钥可以存储在多个设备上，在世界的两端，或在一个用户和一个钱包服务之间共享，这意味着黑客必须破坏多个目标才能窃取钱币。

Andresen对这一想法非常着迷，他将成为这一想法的第一个拥护者，在邮件列表中写下了慷慨激昂的请求，以激励贡献者采取行动。

"我最担心的是我们会说，'当然，只需要几天时间就能就如何做好它达成一致'，而六个月后仍然没有共识，"他写道[[6](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/)]。"而人们的钱包[[将]继续丢失或被盗。"

这些担忧并不是没有道理的--正如中本聪所实现的那样，多签有很大的缺点。其中最紧迫的是，交易与比特币的标准地址格式不兼容，而需要更长的地址。

正因为如此，为多签钱包提供资金的交易更大，需要更多的费用。更重要的是，这些费用不是由使用多签钱包接收比特币的人支付，而是由向他们发送比特币的人支付。

由于这些次优特性，多签交易在软件中被指定为 "非标准"，意味着它们不一定会传播到网络上的节点。如果一个节点确实收到了多义词交易，它将简单地忽略它。同样，也不能保证矿工会将这些交易纳入区块。

如果它们被包括在内，节点会接受它们（多签交易最终是有效的）。但在实践中，这种指定使得这些交易几乎不可能得到确认。

## 进入 OP_EVAL
为了释放他所看到的潜力，Andresen将继续倡导一种新的 "操作码"，一种节点可以用来决定新类型的交易是否有效以及何时有效的命令。

OP_EVAL的设计是为了适应更高级的交易，如多签，它在很大程度上依赖于哈希，这种加密技巧可以确定地扰乱和压缩数据，但不可逆地变成一串独特的数字。

假名开发者ByteCoin首先[提议](https://bitcointalk.org/index.php?topic=46538.0)，其基本想法是用户可以通过在交易中加入哈希值，来详细说明比特币以后可以花费的条件（包括进出多义词钱包）。币本质上会被发送到一个哈希值。

只有在 "从 "哈希值中花费比特币时，才会显示出后来花费比特币所需的条件。多重签名的用户在花费比特币时将为增加的交易规模付费，而所需的额外数据对网络造成的负担较小。

由于该提案得到了积极的反馈，Andresen没有浪费任何时间，他更倾向于让OP_EVAL尽早部署，而不是拖延。

他写道[[7](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/)]："安全问题真的是优先考虑的问题；我希望在一年内看到人们的论坛签名中有安全的比特币地址。

然而，并不是每个人都认同安德烈森的紧迫感。OP_EVAL将是对一个已经具有数百万美元价值的实时系统的一次重大升级。在大洋彼岸，一位年轻的[Amir Taaki](https://bitcoinmagazine.com/articles/bitcoin-technology-worth-nothing-interview-dark-wallet-front-man-amir-taaki-1412722833)建议开发人员花时间审查该提案。


"乍一看似乎不错，"Taaki写道[[8](https://bitcointalk.org/index.php?topic=46538.msg553903#msg553903)]。"但快速将其纳入区块链可能不是一个明智的想法......比特币明天不会爆炸，所以在像这样的重大变化上暂缓不会有大的损失。"

使问题更加复杂的是，开发者认为在协议中加入OP_EVAL会带来巨大的协调挑战。从本质上讲，颁布它需要冒区块链的风险，区块链是所有比特币交易的最终记录，由其软件规则的共享共识执行，可能会分裂成不兼容的网络。

这意味着一旦OP_EVAL上线，每个用户都必须切换到一个新的软件版本和一个新的区块链，即所谓的 "硬分叉 "升级。

如果不能统一升级，矿工可能会在不知情的情况下产生 "无效 "区块。更糟糕的是，用户可能在不知情的情况下接受 "无效 "交易。


## 一种新型的软分叉
然而，很快，Andresen意识到有可能安抚诋毁他的人。

作为一个巧妙的技巧，他发现OP_EVAL可以通过重新定义中本聪最初包括的几个非活动操作代码之一来部署，作为未来命令的占位符。

令包括Andresen在内的所有人惊讶的是，这也与那些没有升级到接受OP_EVAL的节点兼容。这些节点会检查哈希值是否符合新的指令，但不会强制执行，而是默认接受交易。

只要大多数矿工执行新规则，这意味着已经升级和没升级的节点都会支持新的区块链。升级的节点会接受区块链，因为新规则正在被执行，而未能升级的节点会接受区块链，因为他们并不关心新规则。


这种向后兼容的升级，或 "软分叉"，已经由中本聪部署，但随着网络规模的扩大，开发人员开始担心需要参与任何升级的人数过多。

不出所料，Andresen意识到这是可以避免的，这一点受到了其他既定贡献者的欢迎，他很快与他们分享了这个消息。

"哇，Gavin的观点，即[OP_EVAL]可以不需要分割就能完成，让我大吃一惊，"Gregory Maxwell说，他对这个发现做出了实时反应[[9](https://web.archive.org/web/20131201200245/http://bitcoinstats.com/irc/bitcoin-dev/logs/2011/10/02)]。"[原文]可以开香槟了。" 

有了这个，开发人员继续设计了一个更安全的方法来激活软分叉。他们推测，他们可以进行类似于投票的方式来确定一项功能何时得到矿工足够广泛的支持，然后他们可以利用这种方式来确保安全升级。

矿工将被要求在他们开采的区块中包含一点数据，以示他们将执行新规则。当大多数人准备好了，就可以激活这个变化[[10](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201112)]。


## 致命的缺陷
但所有这些工作都被O’Connor的调查结果所推翻[[13](https://sourceforge.net/p/bitcoin/mailman/message/28617066/)]。

结果是分成了几个派别，一些人认为OP_EVAL被不必要地推迟了，另一些人则认为提出的快速修复会损害比特币基本脚本语言[[14]](https://sourceforge.net/p/bitcoin/mailman/message/28617066/)的某些理想属性。

包括Luke Dashjr、Pieter Wuille和Maxwell在内的开发者提出了一些替代方案，像OP_EVAL一样，利用了向哈希值发送币的概念。但依然面临挑战：让这种逻辑，他们开始称之为 "支付给脚本哈希 "或 "P2SH"，作为一个软分叉进入比特币，同时避免区块链分裂。

现有的操作代码只能走到这一步：非升级的节点需要接受从哈希值中花费硬币的交易，而不了解新的规则。

是Andresen找到了一条前进的道路，他具体的P2SH解决方案根本不需要新的操作代码。相反，Andresen的想法是，比特币可以被编程来识别某种交易格式，然后以一种非常规的方式解释这种格式，用新的指令来验证它。

任何没有升级的节点都会用传统的逻辑来解释这种非常规的格式。就像OP_EVAL一样，交易总是被非升级的节点认为是有效的。这意味着P2SH可以作为一个软分叉来部署：只要大多数哈希力量执行新的规则，新旧节点都会同意同一个区块链。

Andresen的建议似乎令大多数人满意。"似乎......从第一眼就可以接受，"O’Connor回应说[[15](https://sourceforge.net/p/bitcoin/mailman/message/28617230/)]。Taaki在提到该代码的非常规方法时说。"这个想法是一个不同寻常的捷径....，但我喜欢它。" 

在随后举行的开发者会议上，与会者同意实施Andresen的P2SH提案。矿工们将在2月1日之前的一周内接受调查，如果大多数哈希值（55%）表示支持，那么两周后就会发布一个客户端来激活软分叉。

这种和平将持续几天。

## 为什么不用美元？
打破这一共识的是Dashjr，他有事需要提前离开会议，后来才知道Andresen的P2SH版本是公认的妥协方案。

Andresen的解决方案的非传统性质激怒了Dashjr，他认为这使协议复杂化，并带来了不确定的后果。他向Andresen提出了这个问题，但后者不相信他的担忧值得改变计划[[16](https://bitcointalk.org/index.php?topic=58579.msg690145#msg690145)]。

他的建议被拒绝后，Dashjr将于1月中旬在BitcoinTalk公共论坛上爆发，谴责P2SH，并指控Andresen在支持这一变化时 "自作主张"[[17](https://bitcointalk.org/index.php?topic=58579.0)]。

"Gavin正在强迫每个使用最新比特币代码的人投票给[P2SH]，"他写道。"如果你想反对这个疯狂的协议变化，你需要修改你的BitcoinD源代码，否则你将默认为投票支持它。"

由于他的反对意见的细微差别，他在发表这些反对意见时的粗暴语气，以及他对Andresen的指责，对这个帖子的反应并不积极。一些人认为Dashjr没有将技术辩论限制在开发者的范围内，而是试图煽动一个流行网络暴力。

这并没有什么帮助，因为Dashjr是该项目更多的奇思妙想的贡献者之一，他以捍卫替代数字系统和坚定的基督教信仰的长篇论述而闻名。一个论坛用户说，Dashjr的评论使他看起来 "精神不稳定"[[18](https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009)]。另一个人说，他根本不想理会这些细节，他只是相信Andresen[[19](https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009)]。

作为回应，Dashjr从哲学角度对P2SH提案提出了持续的反对意见，不仅质疑其技术优点，还质疑其对治理的影响。

"如果你想要一个君主制的货币，为什么不直接使用美联储的美元？" Dashjr问他的反对者，结果只是被其他人追问，声称是他在争夺权力[[20](https://bitcointalk.org/index.php?topic=58579.msg690042#msg690042)]。

Dashjr并没有退缩，他将编码一个P2SH的替代版本，称为CheckHashVerify（CHV）。CHV本质上是一个不同的P2SH实现--但它不需要对交易输出进行非常规的解释。相反，CHV增加了一个新的操作码，和OP_EVAL一样，可以 "伪装 "成一个占位符操作码。

但对Andresen来说，进行更多的辩论已经太晚了[[21](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-14.html)]。他对公众的爆发感到愤怒，于是用自己的方式来回应，写道："。

"Luke，你在试探我的耐心。我要离开代码几天，在我做傻事之前冷静下来。"

## genjix[^1] 出现了
由于Andresen的P2SH设计（现在简称为P2SH）在很大程度上被认为是该项目首席开发者所喜欢的一个足够好的解决方案，Dashjr发现自己几乎没有同路人。

Taaki将成为认真对待边缘问题的少数声音--但不是因为他反对Andresen的解决方案，也不一定同意Dashjr的解决方案。

这位开发者当时只有20岁出头，已经是比特币最直言不讳的贡献者之一，虽然他还没有成为抢占头条的无政府主义者，在棚屋里进行黑客攻击，与3D打印的枪手一起旅行，但他对软件作为反建制运动的愿景已经把他挤出了项目的核心圈。

这反过来又使Taaki对项目的加速发展进程产生了不信任。他更希望决策过程需要时间，并涉及更广泛的用户群。

在他看来，比特币并不是由一小撮开发者说了算的。Taaki强烈认为，任何对该项目感兴趣的人都应该了解其中的利弊，并尽可能地参与决策。

"我宁愿人们在这个问题上有发言权，即使这让开发者解释他们的决定时生活更艰难，"他告诉其他开发者[[22](https://buildingbitcoin.org/bitcoin-dev/log-2012-01-14.html)]。"告诉我们的用户将是这样的，你没有发言权，然后对他们指手画脚，我感到有点忐忑。"

即使Taaki同意Andresen的P2SH和Dashjr的CHV提案之间的差异很小，他仍然坚持认为让用户参与到开发过程中是一项重要的工作。


"【我】担心的是有一天比特币会被腐蚀"。他认为，"将这种额外的审查视为建立开放文化的机会。"

为此，Taaki写了一篇博文，其中阐述了P2SH和CHV的升级以及两者之间的区别。[[23](https://bitcointalk.org/index.php?topic=61705.20)]。

用户有一个选择，是Taaki的信息，而且。"投票是基于挖矿算力的"。


## 糟糕的情况
通过他的话，Taaki揭露了房间里的一只大象。的确，中本聪颁布了软分叉，但到2011年底，网络不再像早期那样运作。

当中本聪在2008年发表白皮书时，他认为工作证明将由用户通过个人电脑贡献计算来提供。中本聪写道："工作证明本质上是一CPU一投票"。

在这种设计下，任何用户都可以成为矿工，并通过提出区块、验证同行发送的交易和执行开发者编写的代码来确保网络安全。

但在软件推出后的几年里，这种模式已经被企业家们淘汰了。自从Lazlo Hanyesz（[以比特币披萨闻名](https://bitcoinmagazine.com/articles/the-man-behind-bitcoin-pizza-day-is-more-than-a-meme-hes-a-mining-pioneer)）发现了如何用更强大的图形处理单元生成比特币，专家们就忙着把挖矿从一个爱好变成一个小企业。

大约在同一时间，Marek "Slush" Palatinus引入了一种方法，允许矿工汇集提出区块所需的哈希值并分享利润。这有效地使采矿不再是抽奖，而更像是一个稳定的收入来源。

到2011年底，只有三个矿池--DeepBit、Slush Pool和BTC Guild--控制了全球一半以上的哈希力。大多数的 "选票 "现在都集中在少数几个矿池运营商身上，就像他们是网络公民的代表一样，而不是一CPU一投票。

对一些人来说，这证明了比特币网络出了问题。"我认为[矿池]决定网络的变化是一场投票的闹剧，"早期矿工Midnightmagic认为[[24](https://buildingbitcoin.org/bitcoin-dev/log-2011-12-20.html)] 。


对其他人来说，采矿中心化是一个不幸的拐杖，是使软分叉升级更容易管理，从而减少风险的一种方式。(毕竟，现在的安全推广只需要少数几个矿池运营商的参与）。

例如，Maxwell更愿意接受眼前不尽人意的现实[[25](https://buildingbitcoin.org/bitcoin-dev/log-2011-12-19.html)]。

"他回答说："如果有不小的阻力，开发者和资金池都会退缩，但无论如何，现在似乎没有人反对它。"这是一个很好的机制，可以用于未来......希望我们不会出现比特币不再去中心化的这种糟糕情况。"

## 投票或不投票
Andresen和Dashjr的交战提案将体现出对比特币治理的反对意见，这只会让事情更加复杂。

直到那时，开发者一直把即将到来的软分叉升级说成是一种投票：矿工可以通过哈希值的多数来执行P2SH（或OP_EVAL）所列出的新规则，所以投票是为了衡量这种结果的可能性。

但是，虽然这个术语已经成为词汇的一部分，但这省略了一些技术上的细微差别。在进行民意调查时，开发人员并没有完全询问矿工对新规则的看法。相反，他们认为这是一种方法，以了解矿工是否准备好确保安全升级。

从这个角度来看，对开发者来说，只有一个提案会被添加到软件用户和矿工运行中来执行网络规则是合理的。


"比特币系统不是由多数人选举出来的。不是算力的多数，不是人的多数，也不是钱的多数，"Maxwell争辩道，他对Taaki把这个决定说成是投票很恼火[[26](https://bitcointalk.org/index.php?topic=61922.msg723476#msg723476)] 。

Maxwell强烈地认为，矿工的 "投票 "应该被限制在软件本身，以执行交易的顺序，而不是整个网络的规则。

"如果当前矿工的超级多数--甚至100%--决定补贴应该永远是50BTC，会发生什么？什么也没有。他写道："从比特币网络的角度来看，在其软件中改变这一规则的矿工只是停止存在。

Dashjr并不反对Maxwell的观点，但从实际出发，他很难看出，如果开发者在没有矿工支持的情况下推动变革，比特币将如何保持安全。

"矿工可以简单地拒绝开采P2SH交易，以免疫于'开发团队的变化'，"他回应说[[27](https://bitcointalk.org/index.php?topic=61922.msg723520#msg723520)]。"如果'开发者'锁定了所有的矿工，你猜会发生什么？容易受到50%的攻击，网络就不安全了！"

从这个角度来看，就更容易理解为什么Dashjr认为Andresen在滥用他作为首席开发者的角色，试图单独推动P2SH。如果矿工使用标准软件开采区块，它将自动投出赞成P2SH的 "一票"[[28](https://bitcointalk.org/index.php?topic=58579.0)]。

作为回应，Dashjr写了补丁，将把他的首选方案进入哈希值 "选举"，引入矿工投票支持和反对P2SH和CHV的选项。

虽然很少有矿工使用该代码，但Dashjr的反对产生了影响。当时网络上最大的矿池DeepBit的经营者Tycho，开始对自己在评估竞争代码中的角色感到不舒服。

他认为，很明显开发者之间还没有达成共识，他写道："我不想成为决定这个问题的单一实体"[[29](https://bitcointalk.org/index.php?topic=61125.msg714231#msg714231)]。



## 死锁
在拒绝矿池可以被用来左右升级决定的想法时，Tycho为当前的辩论增加了另一个转折点。没有他的支持（占所有哈希值的30%以上），P2SH将很难被激活。

到1月下旬，第一轮P2SH投票接近尾声，它看起来并没有达到规定的门槛。升级将不得不推迟，这一现实不仅使Andresen感到沮丧，而且也使其他开发者感到沮丧。

在IRC上，Maxwell公开感叹，似乎看不到僵局的尽头。

"这种'匆忙'的说法是胡说八道，Gavin是在什么时候开始走[付费到脚本-哈希]的路线的，10月份？"他写道[[30](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-22.html)]。"据我所知，除非有人画出一个最后期限，否则这个过程永远不会收敛，因为总会有一些新的家伙，他的伟大想法被遗漏了。"

Andresen将延迟的责任不是归咎于矿池的出现，而是归咎于DeepBit的运营商Tycho个人。"现在，看起来一个人有足够的算力来否决任何改变，"他写道[[31](https://bitcointalk.org/index.php?topic=61125.0)]。


这让Andresen很烦恼，他认为Tycho的立场是不道德的。他写道："我认为你利用你作为最大的矿池经营者的地位来反对普遍的共识是错误的，"[32](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html)]。

事实上，即使Andresen不惜施加公众压力，推动用户要求他们的矿池升级--并提出在P2SH导致任何财务损失的情况下偿还DeepBit的所有资金--Tycho也不愿意 "投票 "支持该提议[[33](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html)]。

面对拖延，Andresen试图动员公众支持这一事业，坚持认为在P2SH和CHV之间的选择不会对用户产生什么影响。


Andresen 写到:

"所有[P2SH/CHV]的东西主要是工程师在争论用钉子、螺丝还是胶水把两块木头放在一起更好。任何一种解决方案都可以工作，而普通用户不会注意到任何区别"[[34](https://bitcointalk.org/index.php?topic=61125.msg712822#msg712822)]。


从回帖来看，比特币用户接受了Andresen思路，指责Tycho拖住分叉，压迫他激活。

Tycho则激烈地反对Andresen的主张。即使拥有30%的算力，他也知道其余的矿工可以推翻他，而他不想成为决定性因素。


## 第二轮
由于P2SH至今未能积累足够的算力支持，Andresen将越来越多地被迫在公开场合讨论其提案的策略，他明显开始接受CHV作为打破僵局的潜在替代方案。

不过，答复中还是划出了一条分界线，即认为P2SH和CHV之间的选择是由矿工来做的，而那些人则倾向于更加任人唯贤的决策。


"最终，矿工是唯一对这样的问题有发言权的人，"BitcoinTalk用户dooglus争辩说[[35](https://bitcointalk.org/index.php?topic=61922.msg722860#msg722860)]。"他们是唯一能够决定哪些交易进入区块的人。"

该论坛的管理员Theymos断然拒绝了这一想法。"非矿工可以拒绝区块。如果有足够多的客户这样做，矿工开采的硬币将变得毫无价值。"[[36](https://bitcointalk.org/index.php?topic=61922.msg722874#msg722874)]

相反，Theymos提议，某个内部专家圈子应该进行为期两周的讨论，并在结束时发布投票结果[[37](https://bitcointalk.org/index.php?topic=61922.msg722833#msg722833)]。无论是因为这个建议还是偶然，Dashjr很快就创建了一个Wiki，在那里受人尊敬的开发人员可以表达他们的偏好。

在接下来的几天里，Maxwell、Thomas和Wuille都表示他们很乐意接受P2SH或CHV，但他们明确表示他们更喜欢P2SH。O'Connor和Dashjr同意P2SH可以接受，但表示更喜欢CHV[[38](https://en.bitcoin.it/w/index.php?title=P2SH_Votes&oldid=23259)]。

也许不出意料，Andresen确保了选票对P2SH的支持，对CHV的提案投了一个响亮的 "反对票"。

更重要的是，也许很少有矿工支持CHV。到2月中旬，P2SH得到了30%的哈希值的支持，而Dashjr的替代品则停留在2%左右。

在IRC的一次会议上，Dashjr说他正在考虑是否完全退出CHV，勉强接受了P2SH的主导地位[[39](https://buildingbitcoin.org/bitcoin-dev/log-2012-02-14.html#)]。在同一次会议上，与会者同意将第二次投票截止日期定在3月1日。

随着新的截止日期的临近，更多的矿工聚集在P2SH背后，使哈希值支持率接近55%的门槛。很快，Tycho和Dashjr都别无选择，只能接受他们的同伴的偏好[[40](https://bitcointalk.org/index.php?topic=68677.0)]。

就这样，Andresen宣布软分叉将在10天内部署和激活，到2012年4月1日，新的规则被强制执行[[41](https://bitcointalk.org/index.php?topic=71226.0)]。

P2SH，即中本聪离开后的第一次协议升级，已经颁布了。

## 茶壶里的暴风雨
导致P2SH通过的艰难政治进程将继续在软件本身之外产生持久影响。

最后，Andresen能够部署他设计和赞成的解决方案。如果可以说他的领导力在危机中受到了质疑，那么到了最后，他的领导力被牢牢巩固了。

舆论并不关心具体细节，主要是凝聚在一起反对Dashjr的行动，以及在较小的程度上反对Taaki，认为他们是不必要的和煽动性的[[42](https://bitcoin.stackexchange.com/questions/2682/why-are-the-majority-of-miners-not-voting-on-on-p2sh)]。Andresen甚至要求Dashjr完全停止对比特币的贡献，尽管他似乎从这个威胁中退缩了，或者Dashjr根本没有理会它[[43](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-31.html)]。


同时, Maxwell 成为 比特币的 “核心开发者”之一，与Andresen,Wladimir van der Laan 和 Jeff Garzik共享代码库提交权限。

基调已经确定：当涉及到比特币的发展时，支持性的、务实的态度得到了奖励，相反的贡献者被驳回。虽然意识形态上的分歧已经浮出水面，但它们仍然存在，而且可以说只是被程序所巩固。

随着越来越多的用户涌向比特币，P2SH很快就变成了传说中的东西，尽管它将明显地继续成为开发者之间分歧的闪光点。

一年后，在应对另一场新出现的危机时，回忆起这些事件，Andresen会夸夸其谈，表明他认为P2SH验证了他对项目的领导和愿景[[44](https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890)]。

"区块将变大，"他写道，以回应开发者Peter Todd在2013年初制作的一个主张反对提高限额的视频[[45](https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890)]。"你的视频只会让很多人杞人忧天，就像去年Luke-Jr的[CHV]提案除了引起茶壶里的风波外，什么也没做。"

对于第一个去中心化的数字货币，应该如何决策？如果这个问题最终被问到了，那就需要一场更广泛的战争来解决，而且还是在未来的几年里......

[^1]: genjix在BitcoinTalk上的[发言](https://bitcointalk.org/index.php?topic=61705.msg721050#msg721050) 。[Amir Taaki]((https://military-history.fandom.com/wiki/Amir_Taaki)) 在2006年以genjix名义重度参与[水晶空间开发](https://www.youtube.com/watch?v=JtGsQPoqm8Y)
