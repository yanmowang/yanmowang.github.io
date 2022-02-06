---
title: 根据位置搜索telegram群组、在互联网上跟踪人、可视化影响力关系网络、及其他：新生情报工具（10
date: 2021-12-31 23:38:08
tags:
      - 工具
      - 技术
      - 技巧
categories: 新生情报工具
---

# 根据位置搜索telegram群组、在互联网上跟踪人、可视化影响力关系网络、及其他：新生情报工具（10） #

如果您忘记了本系列内容的由来、或者还没有读过以前的内容，可以在下面回顾：

《新生情报工具（1）：人脸识别身份挖掘、推特分析热点事件、暗网爬虫和调查抖音》
《新生情报工具（2）：刮刀、打破推特限制、情报资源机器人、和袜子木偶管家》
《新生情报工具（3）：挖掘推特、搜查加密货币、刮刀和定向追踪》
《新生情报工具（4）：战术培训、狩猎推特、瑞士军刀 — 针对特定目标人的侦查利器》
《新生情报工具（5）：翻译间谍、头像中的秘密、连锅端利器、和追踪资金往来》
《新生情报工具（6）：广泛搜集、地理定位、我知道你的猫住在哪》
《新生情报工具（7）：全球搜人、免费手机短信、放大照片不损质量、快速查找相关视频》
《去模糊化、挖人际关系、自动社交工程攻击、监视信息战：新生情报工具（8）》
《实时钓鱼、快速提取、游行调查、跨站追踪、便携式瑞士军刀：新生情报工具（9）》
今天的内容会开始添加一些方法。工具已经很多了，它们完全可以帮助您完成了不起的调查需求；于是我们会添加更多的方法在本系列中，但继续沿用这一系列的传统标题，以便于查找。

依旧希望今天的内容能对您有用。

1、如何根据位置搜索telegram群组（aware-online）
自从去年6月telegram更新以来，就可以根据其位置搜索用户和群组。这意味着您可以在搜索结果中从与自己相同位置的用户和群组中获得建议。

因此，作为调查者，您可以简单地检查哪个用户和群组在哪个区域中处于活动状态。

👉那么，您是否要不停地旅行才能将用户和所有群组映射到具体位置？当然不必，那也太费劲了。您可以通过简单的位置欺骗来解决此问题。

也就是说，相当于手动将位置设置为其他位置。还记得我们介绍过的浏览器方法吗？在下面看到：

《如何使用位置欺骗扩展追踪约会网站上的目标私密信息？》
那么，您需要的是什么？

实际上只需要一部（虚拟）电话、Telegram 的移动应用程序和 Telegram 上的帐户。就行了。

就如下面的示例中这样，使用“Android模拟器”，这是一种虚拟电话，其功能与普通电话大致相同。当然，你还可以为此使用 NoxPlayer、Bluestacks 或 Genymotion。选择哪种取决于自己的喜好。

例如，您可以在虚拟机 Virtual Box 中创建 Genymotion，也或许您发现 NoxPlayer 可以更好或更快速地工作。当然您也可以使用预付费电话。

好了电话已有，现在就下载 Telegram 吧。

您可以通过 Android 模拟器 + 伪造的 Gmail 帐户，通过 Google Playstore 进行此操作，这取决于您所使用的设备。

此示例继续使用 Android Emulator NoxPlayer，因此，如果您使用其他设备，则步骤可能会略有不同。思路是一样的。

第一步：打开虚拟设备；

第二步：打开Goog​​le Playstore；

第三步：下载telegram。如果一切正常您的虚拟手机环境将如下图所示。

第四步：点击左侧的三个点，然后选择“ V-loc”；

第五步：选择一个虚拟位置。示例中选择了荷兰的“鹿特丹”位置。单击右下角的 “Move here” 以保存位置。

请注意：这种方法不适用于“普通”手机。如果您不使用Android模拟器而是使用普通手机，则可以下载移动应用程序来欺骗位置。在下载移动应用程序时还要注意避免恶意软件。

第六步：打开 Telegram。

第七步：单击左侧的三个条纹，然后选择“联系人”；

第八步：点击 “添加附近的人”，即可根据您的位置查看分组结果。

就是这样。您学会了吗？

2、在互联网上跟踪人 （社交工程攻击/渗透测试服务/开源情报侦查）
Trape 是开源情报跟踪工具，它使人们可以实时跟踪和执行高效的社交工程攻击。创建此工具的主要目的是向人们展示攻击者如何在不了解目标人的情况下获取机密信息。

作为安全专家，您肯定知道有多种方法可以获取有关目标的信息，其中一种方法是运行远程扫描并检查打开的端口或任何暴露的漏洞。而有针对性的社交工程攻击是第二种非常普遍使用的方式。如果您对第二种感兴趣，那么 Trape 是您的最佳选择。

此工具提供了许多很棒的功能。在您为自己的组织执行的渗透测试期间，使用此工具将很有用，以通过网络钓鱼和社交工程攻击来测试目标，并查看目标如何与链接交互。

使用方式

首先：

git clone https://github.com/jofpin/trape.git

cd trape

python2 trape.py -h
如果不起作用，请尝试安装 requirements.txt 中的所有库：

python2 -m pip install -r requirements.txt
执行示例：

Example: python2 trape.py --url http://example.com --port 8080
帮助和选项：

user:~$ python2 trape.py --help

usage: python trape.py -u <> -p <> [-h] [-v] [-u URL] [-p PORT]                                                   

                                              [-ak ACCESSKEY] [-l LOCAL] 

                                              [--update] [-n] [-ic INJC]
optional arguments:  

-h, --help            show this help message and exit  

-v, --version         show program's version number and exit  

-u URL, --url URL     Put the web page url to clone  

-p PORT, --port PORT  Insert your port

-ak ACCESSKEY, --accesskey ACCESSKEY

                      Insert your custom key access  

-l LOCAL, --local LOCAL

                      Insert your home file  

-n, --ngrok           Insert your ngrok Authtoken

-ic INJC, --injectcode INJC

                      Insert your custom REST API path  

-ud UPDATE, --update UPDATE

                      Update trape to the latest version
您可以在此处阅读更多信息并下载该工具：https://github.com/jofpin/

3、可视化影响力关系网络
这是调查信息战和挖掘旋转门的有效工具。实例报告：

《深层政治：Facebook金字塔的人形肌理 — — 仅仅依靠开源数据，扒开利维坦的内裤》
《追踪谷歌的政治旋转门：开源调查》
Oligrapher 是可视化影响网络的工具。Oligrapher 最初是为了与 LittleSis 数据一起使用而开发的。现在，可以安装它与其他数据集一起使用。

只要数据格式符合正确的标准，Oligrapher 的最新版本即可与非LittleSis数据集一起运行。

特征包括：

全屏和嵌入式地图
可自定义的节点、边线和文本
轻松创建和显示网络图
添加图像、标签、链接和标题
通过拖动节点和边缘来定制图形布局
从 LittleSis 和其他API导入数据
撤消和重做对图形的编辑
可以在所有现代网络浏览器上运行
在下面看到演示视频：





链接：https://github.com/skomputer/oligrapher

4、抓取评论的工具
这是一个站点，可以轻松将 Facebook、Instagram 或 Twitter 帖子中的所有评论导入到CSV文件。

对于追踪和调查 trolls/信息战 来说比较有用 —— 因为大多数信息战账户只评论不发帖。

《看清信息战：2019全球有组织社交媒体操纵清单》
《如何分辨：机器人、僵尸网络和 trolls》
您只需要把准备抓取的帖子链接贴进去就行了。

链接：https://exportcomments.com/

5、直接进入目标人的Google相册
用户 pal737 分享了指向 Google 相册的直接链接。只需在以下URL中填写用户ID，即可带您进入 Google 帐户的相册：

https://get.google.com/albumarchive/ 用户ID
还有另一个链接，可以显示拍摄照片的位置。再次，只需填写Google用户ID，只要其中包含位置信息，它就会弹出一个带有相册位置的 Google Map：

https://maps.google.com/maps/contrib/userID/photos
6、终极 Facebook 抓取工具
该机器人可抓取 Facebook 用户个人资料的几乎所有内容，包括用户时间轴上可用的所有公共帖子/状态、上传的照片、带标签的照片、视频、朋友列表、及其个人资料照片（包括关注者、关注的人、工作朋友、大学朋友等）。

数据以有组织的格式被抓取，以供研究人员用于教育/研究目的。此抓取工具不使用 Facebook 的 Graph API，这意味着没有速率限制问题。

您需要的是：

安装最新版本的 Google Chrome。
安装 Python 3
具有未启用 2FA 的 Facebook 袜子木偶帐户
$ git clone https://github.com/harismuneer/Ultimate-Facebook-Scraper.git
$ cd Ultimate-Facebook-Scraper

# Set up a virtual env
$ python3 -m venv venv
$ source venv/bin/activate

# Install Python requirements
$ pip install -e .
该工具仅用于研究目的。因此，此工具的开发人员对使用此工具收集的任何数据的滥用概不负责。许多研究人员和开源情报分析人员使用它。

👉如果您的袜子木偶帐户是使用2FA设置的，则此工具将无法使用。您必须先禁用它，然后再使用。

关于如何制作袜子木偶：《如何快速创建一个假人？简易版分身术 — 调查人员使用》。

GitHub：https : //github.com/harismuneer/Ultimate-Facebook-Scraper

7、快速跟进消息
这是一个新的自定义搜索引擎，可从 Twitter、Reddit 和 4Chan 中挖掘包含 Google Map 链接的搜索结果。上图是示例。

如果您要搜索特定事件并希望紧跟最新的消息，这是一个很好用的工具。

链接：https://cse.google.com/cse?cx=015328649639895072395:sbv3zyxzmji#gsc.tab=0