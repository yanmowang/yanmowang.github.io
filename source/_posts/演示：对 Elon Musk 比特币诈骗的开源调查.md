---
title: 演示：对 Elon Musk 比特币诈骗的开源调查
date: 2021-12-30 23:38:08
tags:
      - 调查
      - 获取真相
      - 思考
categories: 让它民主-掌握真相的技术和技巧
---
# 演示：对 Elon Musk 比特币诈骗的开源调查 #

Elon Musk 免费发比特币啦！带蓝V的账户啊！……哦不，等会，这是个在推特上很老套的骗局。本文尝试使用开源调查 #OSINT 找到所有和诈骗有关的东西 (主机名称、IP 地址、邮箱地址、名字、域名等等)，揭示诈骗者的真实身份；或者至少是可揭示身份的线索。感谢 Steve Micallef 的优秀演示！非常精彩
您也许听说了过去几周在 twitter 上有人以 Elon Musk 的名义进行比特币诈骗的事。在这篇文章中我会解说一下这个诈骗是怎么实现的，然后给您展示一个用简单和有效的方法对该诈骗进行开源调查 (OSINT) 的过程。

Elon Musk Bitcoin 诈骗事件

我们先看一下这个诈骗是什么样的。下面的截图是其中一个骗子用的 twitter 推送号：

这个 tweet 本身十分荒诞 (Musk 发派免费比特币!? 骗谁…),而且推文充满语法错误,明显的假 Tesla 网站域名,昵称与账号名称也不符,可还是有很多人上当了.
简单来讲，骗子先黑掉了一些通过了认证的、小有名气的 twitter 账户，比如 Capgemini, Target and Google’s G Suite，再把昵称和头像换成 Musk，然后用推送 (promoted tweet) 的方式把含有诈骗链接的 tweet 发给潜在受害者。虽然这些 tweet 本身十分荒诞，而且充满语法错误和明显的假 Tesla 网站域名，昵称与账号名称也不符，可还是有很多人上了当。

骗子大致骗走了价值18万美元的比特币，简直难以置信！！

当然 Twitter 上的比特币诈骗其实也不是什么新鲜事。可当我从 twitter 看到这次事件后，我忍不住想对涉及诈骗的域名做个开源调查 (OSINT)，就是出于好奇会发现什么。

作为 SpiderFoot 的开发者，我也总是想有机会测试和完善 Spiderfoot，这次倒是个不错的机会。我把那些域名输入到了 spiderfoot，然后开启了150 个模块来收集尽可能多的数据。

除了用 spiderfoot 自动收集的数据，我还人工收集了一些作为补充，在这里就会讲到。

分析的目的

说实话，一开始除了为完善 Spiderfoot 以外我没有什么其他目的。不过我灵光一现，觉得既然要写一个文章，我不如组织一下然后把处理的过程给写出来，长话短说，目的是：

找到所有和诈骗有关的东西 (主机名称、IP 地址、邮箱地址、名字、域名等等)，用来揭示诈骗者的真实身份；或者至少是可以找到用来揭示诈骗者的真实身份的线索。

了解诈骗的特征，希望可以对诈骗调查、和以后预防类似诈骗，都有用

给调查的进一步深入提供可能的实行方案的建议，希望可以帮助对本案和以后类似案件的调查。开始之前，我要声明一下，我不是说这里调查出来的一定是诈骗者的真实身份，也不是说我的调查本身是全面的。这篇文章只是为了让大家对这次诈骗事件有更深入的了解，以及对进行类似调查的人提供一点指导。

那我们开始吧!

分析

分析开始，我们要找一个可以进行自动化 OSINT 调查的起点。

诈骗者使用的 twitter 是被黑掉的合法账号，那么从这些 twitter 账号入手的话大概得不到什么有用的信息；另外，诈骗者用的名字 (Elon Musk) 明显不是本人 (不过，客观来说也不能排除是本人哦！)。所以我们只好从诈骗者用的假域名入手调查。

诈骗 tweets 已经给出了一些域名，但是肯定不止就这些：

m-tesla[.]me
elonmusk[.]id
m-tesla[.]pw
开始调查域名

我们要调查域名可以用哪些技巧呢？域名都会指向 IP 地址，有一个 Whois 的注册记录之类的。我们可以把这些叫做 ‘信息链’。看起来就像这样：

域名 -> IP 地址 -> 查询被动 DNS -> 同一主机下的其他站点 (Co-hosted sites)
域名 -> Whois 查找 -> 电子邮箱
域名 -> 抓区网页内容 -> 名字, 其他
And so on…
当然上面的信息链是非常简单化的，表达的意思就是：一个信息线索可以追踪到另一个、再追踪到下一个，以此类推。很多调查中您可能要进行十多层的信息追踪，这就要看您有多少数据来源和信息链中每一环的质量了。

在域名被下架的情况下查找 IP 地址

现在去查找诈骗者的域名只会返还 127.0.0.1 (本机地址)。因为域名被下架了。

要是有 IP 地址是会很方便的，因为用它可以查到相关的威胁情报消息，网路拓扑/路由数据，甚至更多。从这些数据我们可以找到其他指向这些 IP 地址的更多域名，而且还可以查看有没有在同一个 IP 地址下的子网，这可能用来发现一个更大的诈骗网络。

那我们看看能不能查到诈骗域名曾经用过的 IP 地址。幸好被动 DNS 是一个不错的信息来源，而且网上有很多免费的查找被动 DNS 的服务，这个案例中，我用 Mnemonic Passive DNS search engine 找到了 3 个域名中的 2 个 IP 地址。在这里 m-tesla[.]me (193.233.15.187) 和 elonmusk[.]id(193.233.15.163)。

多亏了被动 DNS，我们可以查到域名曾经指向的 IP 地址
其他类似的工具还有 Robtex.com, SecurityTrails.com, HackerTarget.com, Cymon.io 和 VirusTotal。由于被动 DNS 的特性，很可能单一的工具查不到完整的线索。所以别只依赖一个工具。结合多个工具查到的信息在去整合出一个更完整的轮廓……现在我们有了 IP 地址，可以进一步分析了。

谁是 IP 地址的所有者？

有趣的是，这三个诈骗域名用的是同一个服务供应商“storm-pro.net” 。从 Whois 数据可以看到：

steve@dev:~$ whois m-tesla.me
Domain Name: M-TESLA.ME
...
Name Server: DNS2.STORM-PRO.NET
Name Server: DNS1.STORM-PRO.NET
...
但是域名好像没有网站，而且所有有用的 Whois 信息都被打码处理了，输入 host -t a storm-pro. net 看到：

steve@dev:~$ host -t a storm-pro.net
storm-pro.net has no A record
steve@dev:~$ host -t a www.storm-pro.net
Host www.storm-pro.net not found: 3(NXDOMAIN)
steve@dev:~$ whois storm-pro.net
...
Registrant Name: GDPR Masked
Registrant Organization: GDPR Masked
Registrant Street: GDPR Masked GDPR Masked GDPR Masked
Registrant City: GDPR Masked
Registrant State/Province: GDPR Masked
Registrant Postal Code: 00000
Registrant Country: GDPR Masked
Registrant Phone: +0.00000000
Registrant Phone Ext:
Registrant Fax:
Registrant Fax Ext:
Registrant Email: gdpr-masking@gdpr-masked.com
Admin Email: gdpr-masking@gdpr-masked.com
Registry Tech ID: Not Available From Registry
Tech Name: GDPR Masked
Tech Organization: GDPR Masked
Tech Street: GDPR Masked GDPR Masked GDPR Masked
Tech City: GDPR Masked
Tech State/Province: GDPR Masked
Tech Postal Code: 00000
Tech Country: GDPR Masked
Tech Phone: +0.00000000
Tech Phone Ext:
Tech Fax:
Tech Fax Ext:
Tech Email: gdpr-masking@gdpr-masked.com
...
那我们试试直接从 IP 地址抓取内容，看看背后可能有什么。当我们试图访问https://193[.]233[.]15[.]163 时，显示的是这个：

看起来诈骗者用这个服务商运行他们的网站。看起来这个是面向俄语市场的提供 DDOS 攻击防御和网站服务的公司。

这个公司的网站上提供的信息很少，但是他们的 LinkedIn 页面显示他们是一家在斯洛伐克注册的公司，员工有4人，其中3个在俄罗斯，1个在捷克。到目前为止我们知道，诈骗网站不是被这家公司就是被诈骗者自己关闭了。

在同一个服务器和网站上还有别的线索吗？

因为这个诈骗在统一子网上有很多 IP，查找一下子网的所有者就有价值了，这里可以用到 BGPView.io。

从193.233.15.0/24 子网的搜索结果看，一部分自动化系统是由一个叫 Smart Telecom SARL 的黎巴嫩注册的公司所有，而公司地点可能是在塞舌尔
深入调查我们可以发现上游提供商(提供网路服务的公司)。我们又看到了 StormWall，那就是说他们在为那个 IP 提供 HTTP 代理：

STORMSYSTEMS-AG = StormWall
对 193.233.15.0/24 子网进行 Whois，可以看到一家叫 Safe Value Management 的公司：

steve@dev:~$ whois 193.233.15.0/24
% This is the RIPE Database query service.
% The objects are in RPSL format.
%
...
organisation:   ORG-SVL6-RIPE
org-name:       Safe Value Limited
org-type:       OTHER
address:        Global Gateway 8, Rue de la Perle, Providence, Mahe, Seychelles
geoloc:         -4.678633 55.467250
abuse-c:        SVM142-RIPE
mnt-ref:        safevalue-mnt
mnt-ref:        FREENET-MNT
mnt-by:         safevalue-mnt
mnt-by:         FREENET-MNT
created:        2017-03-13T16:19:46Z
last-modified:  2017-04-30T08:54:48Z
source:         RIPE # Filtered
role:           Safe Value Management
address:        Global Gateway 8, Rue de la Perle, Providence, Mahe, Seychelles
abuse-mailbox:  abuses@safevalue.pro
nic-hdl:        SVM142-RIPE
...
从被打码的邮箱 abuses@safevalue. pro，我们可以猜测到公司的主页。我们来看看：

主页上找不到关于公司的具体信息。虽然从 Whois 的记录来看公司的位置是在塞舌尔，可主页上也没有找到明显的关于公司位置的情报。

虽然主页上没有明显的选择其他语言的功能，其实您可以手动进入一个可以显示俄语鼠标弹窗 (mouseover) 的网页，虽然网页内容还是英语。就是在 https://safevalue.pro 后面加上 /ru 来实现。尝试其他语言会显示 404 (就是说只有俄语选项)。

在 safevalue.pro/ru 里, 虽然网页还是英语，但您可以看到俄语的 mouseover.。尝试其他语言会显示 404
那其他相邻子网的情况呢？他们在什么地点、由谁控制？下边的 whois 脚本(粗体)就是用来查找这些 193.233.15.0/24 的相邻子网的所在国家和注册组织的：

steve@dev:~$ for i in `seq 5 25`; do whois 193.233.$i.0/24 | egrep -i country\|org-name | sort -u; done
country:        RU
org-name:       OOO Avantelecom
country:        RU
org-name:       Vostok Telecom LLC
country:        RU
org-name:       OOO Avantelecom
country:        RU
org-name:       L.Ya.Karpov Institute of Physical Chemistry
country:        RU
org-name:       Vostok Telecom LLC
country:        RU
org-name:       State Federal Budgetary Scientific Establishment Baikov Institute of Metallurgy and Materials Science of Russian Academy of Sciences
country:        RU
org-name:       State Federal Budgetary Scientific Establishment Baikov Institute of Metallurgy and Materials Science of Russian Academy of Sciences
country:        RU
org-name:       OOO Telecom-V
country:        RU
org-name:       OOO Telecom-V
country:        RU
org-name:       Russian National Public Library for Science and Technology
country:        SC
org-name:       Safe Value Limited
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       ZAO Redcom-Internet
country:        RU
org-name:       Federal Budgetary Educational Enterprise of Higher Professional Education Moscow State Forest University
country:        RU
org-name:       Federal Budgetary Educational Enterprise of Higher Professional Education Moscow State Forest University
可以发现 193.233.15.0/24 的相邻子网都在俄国，除了那个涉及诈骗的以外 (country:SC | org-name: Safe Value Limited)。此外除了这一个，其他的子网也和 Safe Value Limited 没有关联。

那我们总结一下，我们用被动 DNS 查到诈骗网页曾经的 IP 地址，他们都属于一个由 StormWall 和 Safe Value Management 提供的子网。两个公司都显示是俄国公司。而且后者 Safe Value 明显尝试隐藏这一事实。诈骗网站所在的子网显示的注册地址和注册组织和相邻子网里的其他网站也有很明显的不同。我们来扩大调查，看看还有没有其他网站涉及这次诈骗。

扩大调查

在 spiderfoot 中我们可以用查询多个被动 DNS 的方式来查找指向同一 IP 地址的其他诈骗网站。 这里，Robtex, Cymon and Mnemonic 现实了一些和 m-tesla[.]me 用相同 IP 的网站，他们曾经都用过 193.233.15.187 这个 IP：

SpiderFoot 用多个数据来源查询曾和 m-tesla[.]me 用过同样 IP 的网页.
我们看到，利用同一基础设施，诈骗涉及了不少网站。我们在来查询 193.233.15.0/24 整个子网，看看都有那些网站：
结合 Robtex 和其他工具, SpiderFoot 发现 186 个网站和诈骗网站在同一子网下
186 有点多，为了找到最可能的目标，下一步我们查一下网站的声望。

恶意和 Spam IP

一些提供威胁情报服务和提供 Spam 发现和 IP 声望的服务，把下面的网址曾经列为有风险。比如 virus total 就在 2018 年8月把以下网址定义为危险：

SpiderFoot 也可以自动查询到在同一服务和同一子网下的不同网站，我们立刻就发现了几个和之前找到的两个 IP 在同一子网下的有风险 IP。

从 Virus Total 发现这个子网下有 117 个恶意网址。从结果上看，甚至有一个网站上挂了恶意软件：

查询 193.233.15.0/24 下的网址都会显示类似的结果。实际上，在这篇文章写作的时间里，Spamhaus 把这整个子网都视为危险。

那到底是谁在背后？

意料之中的是，我们找到的关联诈骗网站的邮箱都是 privacy/abuse 邮箱。就是打了码，所以没法确定拥有者：

19dd5ea57f2b4f5388f5f506cb5a9099.protect@whoisguard.com
3471443@PRIVACY-LINK.COM
abuse@101domain.com
And so on…
换句话说，全都没用。有一些明文邮箱倒是可以找到，可在这片文章里不做深入调查，而且那些明文邮箱也好像和诈骗关系不大 (比如, elonmusk[.]ooo)。

利用环境内容深入调查

我们了解到有关诈骗的多个域名都用的是同一个基础设施，我们可以用其中一个域名的信息来帮助查找其他的。我们在回到 Whois 去查寻，3个诈骗域名有2个是用 NameCheap 注册的，只有1个不是：

Spiderfoot 发现3个诈骗域名有2个是用 NameCheap 注册的, 只有1个不是
当使用 Whois 时，您把查询指向特定的服务器，很多时候人们只关心他们首先看到的 Whois 信息。但是，有时候 Whois 里一些周边信息更可能关系到调查能否有突破还是进入死胡同。

steve@dev:~$ whois m-tesla.me
Domain Name: M-TESLA.ME
Registry Domain ID: D425500000070248173-AGRS
Registrar WHOIS Server: whois.namecheap.com
...
当进行 Whois 查询时，您所用的 Whois 客户端软件会向内置的一些默认 Whois 服务端自动查询。 Whois 的结果经常会来自一些权威的 whois 服务器，因为可能会有更多信息。就像黑体字显示的，那我们在 Linux 的 Whois 中加入 -h 来看看：

steve@dev:~$ whois m-tesla.me -h whois.namecheap.com
Domain name: m-tesla.me
Registry Domain ID: D425500000070248173-AGRS
Registrar WHOIS Server: whois.namecheap.com
Registrar URL: http://www.namecheap.com
Updated Date: 2018-11-07T11:29:42.00Z
Creation Date: 2018-11-07T11:29:42.00Z
Registrar Registration Expiration Date: 2019-11-07T11:29:42.00Z
Registrar: NAMECHEAP INC
Registrar IANA ID: 1068
Registrar Abuse Contact Email: abuse@namecheap.com
Registrar Abuse Contact Phone: +1.6613102107
Reseller: NAMECHEAP INC
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Domain Status: serverTransferProhibited https://icann.org/epp#serverTransferProhibited
Registry Registrant ID: ti1srjorhfz8q94w
Registrant Name: WhoisGuard Protected
Registrant Organization: WhoisGuard, Inc.
Registrant Street: P.O. Box 0823-03411
Registrant City: Panama
Registrant State/Province: Panama
Registrant Postal Code:
Registrant Country: PA
Registrant Phone: +507.8365503
Registrant Phone Ext:
Registrant Fax: +51.17057182
Registrant Fax Ext:
Registrant Email: 81c4aa68df5640a3afd986ce438afa26.protect@whoisguard.com
Registry Admin ID: y8otwk46zno0fdku
Admin Name: WhoisGuard Protected
Admin Organization: WhoisGuard, Inc.
Admin Street: P.O. Box 0823-03411
Admin City: Panama
Admin State/Province: Panama
Admin Postal Code:
Admin Country: PA
Admin Phone: +507.8365503
Admin Phone Ext:
Admin Fax: +51.17057182
Admin Fax Ext:
Admin Email: 81c4aa68df5640a3afd986ce438afa26.protect@whoisguard.com
Registry Tech ID: q5fk9pxjotdst0s1
Tech Name: WhoisGuard Protected
Tech Organization: WhoisGuard, Inc.
Tech Street: P.O. Box 0823-03411
Tech City: Panama
Tech State/Province: Panama
Tech Postal Code:
Tech Country: PA
Tech Phone: +507.8365503
Tech Phone Ext:
Tech Fax: +51.17057182
Tech Fax Ext:
Tech Email: 81c4aa68df5640a3afd986ce438afa26.protect@whoisguard.com
Name Server: dns1.storm-pro.net
Name Server: dns2.storm-pro.net
DNSSEC: unsigned
URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
>>> Last update of WHOIS database: 2018-11-17T17:46:28.10Z <<<
好像是更多没用的信息？不过等等，我们知道2个诈骗域名用的是 NameCheap，也许第3个也其实是用 NameCheap？我们对 elonmusk[.]id 用过 Whois 可是没有显示和 NameCheap 有关。但也许那是 .id 这个域名的 Whois 服务特性？因为不是所有 Whois 服务都会返还统一的数据和格式。我们再试试 -h 一下 elonmusk.id ：

steve@dev:~$ whois elonmusk.id -h whois.namecheap.com
Domain name: elonmusk.id
...
Registrant Name: Sergey Ishuk
Registrant Organization:
Registrant Street: lenina 131 lenina 131 kv 2
Registrant City: Xarkov
Registrant State/Province: Xarkov
Registrant Postal Code: DN3 6GB
Registrant Country: GB
Registrant Phone: +380.957370883
Registrant Phone Ext:
Registrant Fax:
Registrant Fax Ext:
Registrant Email: p286759488@yandex.ru
...
现在有意思了！名字 (Sergey Ishuk), 地址 (lenina 131 lenina 131 kv 2,Xarkov)，电话(+380.957370883) and 邮箱 (p286759488@yandex.ru) 。 也许细节是假的，但我们用搜索引擎 (比如 google) 查查电话看看 +380.957370883：

发现了一个明显的诈骗网路 (give-coinbase.com)。我们还查到了更多的邮箱和名字信息。

相似域名: 潜在的诈骗？

这次 twitter 上诈骗的是价值 18 万美元的比特币，估计还有不少类似的网站诈骗更多。看看不同顶级域 (TLDs) 上的其他相似域名，很可能诈骗者在未来还会用 Elon Musk 的名义诈骗。

SpiderFoot 的可视化图表, 可以看到不同顶级域(TLDs)上的其他相似域名,在未来的诈骗可能使用
结论

关于这次诈骗我们总结一下：

诈骗用的是相同的服务供应商，StormWall 和 Safe Value Management，两者都是俄语，后者 Safe Value Management 明显的试图隐藏这个事实；
虽然诈骗相关域名的 IP 很快被改成了 127.0.0.1， 用被动 DNS 数据可以揭示原始 IP，这成了调查的关键线索；
所有涉及诈骗的域名的 Whois 用上了隐私服务，使得查找相关人和组织变得不可能。从查找子网中其他诈骗网路的所有者可能查到这次诈骗的所有者线索，毕竟整个子网都被标识为’恶意’‘；
用 whois 向2个诈骗网站所在的服务器 (NameCheap) 查询。这个方式揭示了第3个网站的线索；
诈骗网路在同一个 /24 子网， 这个子网上的其他网站行为类似，被多个威胁情报分析服务标为恶意；
诈骗网站和恶意子网上的其他网站大都显示是在塞舌尔注册的，而语言却是俄语。
在我们下结论说是俄国人搞的鬼之前，记住互联网上的信息可不一定全是真的！甚至假消息居多。对以上的结果还要仔细斟酌一下。

可能的进一步调查：

用 Blockchain.info 和 BitcoinWhosWho.com来分析诈骗者的比特币地址，分析一下资金流向；
对这个子网上的网站进行更深入的内容和 Whois 调查，看看有没有其他邮箱地址或个人信息可以作为线索；
用反向 Whois(reverse whois) 比如 SecurityTrails 和 ViewDNS.info 查找这些可疑邮箱和名字注册的其他域名；
在不同顶级域 (TLDs)深入查询相同域名。查找可能是诈骗者或类似诈骗者的邮箱地址；
查询下架网站的历史缓存内容，可以用 Google 和 Bing’s 的 caches 功能作为开始。虽然这次诈骗的网站在 Wayback Machine 上没有，不过更早的网址可能可以查到；
用搜索引擎比如 DuckDuckGo 或 Google，可以查找分析中发现的内容，如电话号码、邮箱、地址、人名；
发挥想像力! 可以借鉴一下 proofpoint 的事件，希望给您点灵感。