---
title: 搜电影、书、开放课程、Twitterlists、GPS、挖Skype、开源情报虚拟机、挖抖音、双语搜索 ……：新生情报工具（16）
date: 2021-12-31 23:38:08
tags:
      - 工具
      - 技术
      - 技巧
categories: 新生情报工具
---

# 搜电影、书、开放课程、Twitterlists、GPS、挖Skype、开源情报虚拟机、挖抖音、双语搜索 ……：新生情报工具（16） #


欢迎回来！

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
《根据位置搜索telegram群组、在互联网上跟踪人、可视化影响力关系网络、及其他：新生情报工具（10）》
《实时新闻地图、Twitter 情报分析、电话号码追踪、电子邮件侦查及其他：新生情报工具（11）》
《种子、暗网、区块链、抖音、telegram、数据集…… ：新生情报工具（12）》
《社交媒体情报、追踪电邮电话号码、挖抖音、搜网络摄像头……：新生情报工具（13）》
《挖抖音、泄漏密码、漏洞、人脸识别工具、假身份生成器、事实核查 ……：新生情报工具（14）》
《挖 Telegram 群组、搜脸、搜人、蜂窝塔、网络摄像头、物联网、黑客新闻 ……：新生情报工具（15）》
依旧希望今天的内容能对您有用。

1、TikTok（抖音）数据挖掘
AwareOnline 分享了一个提示，内容涉及如何查看 TikTok 用户的 JSON 数据，包括关注者和被关注数量、清晰版的头像（ 720×720）、以及其他信息。只需使用以下 URL 即可检索 JSON 中的数据：

https://www.tiktok.com/node/share/user/@UserName
将 {username} 替换为目标用户名。就是这么简单。


如果想要 1080×1080 的图像呢？

转到 TikTok 个人简历 tiktok.com@{username}
打开开发者工具 (F12)
选择 “Network tab”
刷新页面（F5）
选择“ XHR”标签
双击 “api/user/detail/”
打开 “AvatarLarger” 链接
完成
2、ClustrMaps
ClustrMaps 是一个网站，收集基于美国的数据集，并在线提供给您搜索。有一些数据集可免费查找地址、人员和公司。

测试了一下，多数情况下有效，但并非所有目标人都能找到。因此，它可能不像 Pipl 那样的站点能做到的广泛程度，但是对于以美国为基地的侦查目标来说，很高兴能找到完全免费的东西:)


Link: https://clustrmaps.com

3、评估您的虚拟环境
InviZzzible 是一种以简单可靠的方式评估您的虚拟环境的工具。它包含最新的检测和规避技术以及针对它们的修复程序。而且您可以自己添加和扩展现有技术。

支持：

Cuckoo Sandbox
Joe Sandbox
VMWare virtualization products
VirtualBox
Hyper-V
Parallels
QEMU
BOCHS
Xen
VirtualPC
Sandboxie
Wine
link：https://github.com/CheckPointSW/InviZzzible

4、开源情报虚拟机
DORA是基于 Michael Bazzell 最新版书推出的虚拟机。该虚拟机是使用 Packer 构建的，生成的构建文件可以导入 Virtualbox。操作系统是XFCE作为桌面环境的64位Debian。

该项目旨在提供一种自动执行VM创建的方法以及该书第5章中的一些软件安装步骤。用户仍然需要完成 Firefox 的配置并安装所需的附件。


上图中这本书在这里下载：https://t.me/iyouport/6614

link：https://github.com/axlshear/dora-osint-vm

5、使用两种语言搜索 Google 的简单方法
单一语种往往只能抓取到片面的内容。也是为什么我们会建议您使用不同语种交替进行搜索。

分头搜索也许很麻烦，但现在有一个方便的方法能够让您一次性以两种语言搜索谷歌，可以试试看。在这里：https://2lingual.com/

6、补充搜索工具系列
▶️ 搜资源 —— 电影、书、艺术、餐饮、信仰、思想、文化…… 等等：

everfest.com

wikido.com

evensi.com

allevents.in

Googleforevents.com

gstlst.com

festivalloon.com

skiddle.com

hanghawk.com

▶️ 使用关键字来搜索视频：kyro.ms

▶️计算机视觉数据集搜索引擎：visualdata.io

比如下面这样，输入中国的结果：


▶️ 通过动画可视化数据的工具（很好玩，试试看？）：visualgo.net

▶️ 大规模开放在线课程搜索：

classcentral.com

classpert.com

my-mooc.com/en/

opencourser.com

coursera.org

coursebuffet.com

coorsy.com

elearning.club

udemy.com

mooc-list.com

不要错过：《650个名校免费在线课程，你马上就可以开始》
▶️ Twitter List 搜索引擎（当然这个搜不到那种被设置为私密的 lists）：

jump.sh

bit.ly/2rutgq2

▶️ 视频、电视电影搜索引擎：embedy.cc

▶️ 世界上第一个离线搜索引擎，您可以使用您最喜欢的语言进行搜索：github.com/OpenGenus/quark

▶️ 挖 Skype 的工具：

speed-friends.com/site/index

findonlinecontacts.com/skype-usernames

dizkover.com/map/skype

dizkover.com/tags/funny

dizkover.com/skype

findusernames.com/list/Skype

avatar.skype.com/v1/avatars/ Image URL

attend-noam.broadcast.skype.com

site:broadcast.skype.com CompanyName

▶️ Whois IP DNS：

dnsviz.net

centralops.net/co/

intodns.com

dnsdumpster.com

robtex.com/dns-lookup/

whois.net

whois.domaintools.com

dnslytics.com

pulsedive.com

▶️ IP查找工具：

find-ip.net

ipgeolocation.io

iplocation.com

iplocation.net

iplocationfinder.net

iplocation.io

iptrackerlocation.com

ipgp.et

iptrackeronline.com

ip-address.org

▶️ GPS搜索：

satnavhere.com

gps.gov

latlong.net

gps-coordinates.net

gps-coordinates.org

geoplaner.com

findlatitudeandlongitude.com

map-gps-coordinates.com

itilog.com

▶️ 搜在线报纸：

newspapersglobal.com

newspaperabstracts.com

newspapers101.com

newspaperlists.com

usanewspapers.com

newspapers-usa.com

world-newspapers.com

findnewspapers.com

us-newspapers-online.com

newslink.org

▶️ telegram 情报

WhatsApp 群组被谷歌挖出震惊了很多人，其实 telegram 也可以使用 dorks，这样:

site:t.me [username]

site:telegram.im [channel]

site:tglist.co [search terms] ‘机器人社区频道’

site:telegram.me messenger

site:tgram.io [group]

▶️ telegram 搜索工具：

搜一切 qilyzem.com

搜频道 telegramchannels.me

搜群组 telegram-group.com/en/

深度搜索 search.buzz.im

搜帖子 tgstat.ru/en/search/

▶️API 搜索 apisio.scalingo.io

▶️API Directories

apis.guru/browse-apis/

api-rest.com/apis/discover

any-api.com

apilist.fun

api-search.io

apiforthat.com

▶️搜监视摄像头

听说很多读者对窥探监视摄像头更感兴趣。是的，Shodan 可以做到，但要想熟练使用它，可能需要一些基础。事实上在线查找网络摄像头的工具和技术方法非常多，包括 Evans 曾经推荐过的最简单的 dorks 都可以做到。

不要错过《搜远程桌面、摄像头、打印机、家用设备 … 等一切的超级Shodan搜索：恐怖指南》
以下是一个列表，帮您总结一下 **网络摄像头搜索工具**：也许仍不全面，但都可以使用。

如今是遍地监视摄像头的时代，相关调查工具的开发也处于热潮中。


上图中这本书在这里下载：https://t.me/iyouport/7042

列表：

hereinreality.com/webcams/

webcamtaxi.com/en/

webcam.nl

worldcams.tv

world-webcams.nsspot.net

kroooz-cams.com

webcamsmania.com

camhacker.com

opentopia.com

camvista.com

webcamhopper.com

camsecure.co.uk

webcamsabroad.com

public-camera.com/en/

mylivestreams.com

pictimo.com

livefromiceland.is

the-webcam-network.com

iplivecams.com

ip-24.net

leonardsworlds.com

whatsupcams.com/en/

wxyzwebcams.com

webcamlocator.com

123webcam.com

goandroam.com

hdontap.com

city-webcams.com

camscape.com

gobefore.me

explorewebcams.com

hereinreality.com/webcams/

myworldwebcams.com

liveincam.com

geocam.ru/en/

onlinewebcameras.com

webcambiglook.com

bit.ly/37M3Qou

cse.google.com/cse?cx=partner-pub-2526982841387487:1817040253&ie=UTF-8

cse.google.com/cse?cx=004985303091853907970:enq82n069w8

👉 “新生情报工具” 系列收纳在 <列表-5 “直接行动” 中的 “开源情报”> 部分，于是，您知道它的目的。

▶️ 卫星图像搜索工具：

zoom.earth

search.landinfo.com

terrapattern.com

earthexplorer.usgs.gov

search.remotepixel.ca

worldview.earthdata.nasa.gov

apps.sentinel-hub.com/eo-browser/

discover.digitalglobe.com

imagery.geocento.com

▶️Wi-Fi 搜索引擎：

instabridge.com/free-wifi/

wiman.me

freewifinearbyme.com

wififreespot.com

wigle.net

wifimap.io

globalconnectwifi.com/hotspot-finder

hotspothaven.com

▶️ GPS搜索工具：

whatsmygps.com

mapcoordinates.net/en

geoplaner.com

latitude.to

gps-latitude-longitude.com

getlatlong.net

itilog.com

gps-coordinates.net

twcc.fr/en/

▶️ IOT 搜索引擎查找可以用来攻击的设备 — — 黑客侦查第一步：

shodan.io

thingful.net

censys.io

onyphe.io

zoomeye.org

不要错过 “黑客主义行动力” 系列：

《Mr.Robot 如何摧毁邪恶公司？- 黑客主义行动力（1）》
《Elliot 如何骇客邪恶公司并保证无法被反向追踪：黑客主义行动力（2）》
《如何全面间谍任何人的智能手机私密活动 — 黑客主义行动力（3）》
《如何在音频文件中隐藏秘密信息：黑客主义行动力（4）》
《如何破解蓝牙打开监狱大门：黑客主义行动力（5）》
《”融化” 所有债务 ……如何构建黑客树莓派 — 黑客主义行动力（6）》
《充分了解你的攻击目标：进行电子邮件侦查的简单方法 — 黑客主义行动力（7）》
《如何获取任何人的Wi-Fi密码而无需破解：黑客主义行动力（8）》
持续更新中
▶️ 搜索数据集的工具：

gapminder.org

search.openedition.org

data.worldbank.org

webdatacommons.org

openpaymentsdata.cms.gov

zenodo.org

public.enigma.com

visualdata.io

datasetlist.com

gdeltproject.org/data.html

datausa.io

datahub.io/search

registry.opendata.aws

openicpsr.org/openicpsr/

opendatani.gov.uk

opendatanetwork.com

data.oecd.org

msropendata.com

datasearch.gesis.org

figshare.com

dataone.org

data.europa.eu/euodp/en/home

search.datacite.org

opendata.cern.ch

dataportals.org

academictorrents.com

datasetsearch.research.google.com

data.gov

usgs.koordinates.com

geoseer.net