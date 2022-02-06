---
title: 隐私型开源推特前端、追踪热点事件、邦德在哪、冠状病毒和抗体、搜警用无线电、网络摄像头dorks、暗网搜索 ……：新生情报工具（19）
date: 2021-12-31 23:38:08
tags:
      - 工具
      - 技术
      - 技巧
categories: 新生情报工具
---

# 隐私型开源推特前端、追踪热点事件、邦德在哪、冠状病毒和抗体、搜警用无线电、网络摄像头dorks、暗网搜索 ……：新生情报工具（19） #


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
《搜电影、书、开放课程、Twitterlists、GPS、挖Skype、开源情报虚拟机、挖抖音、双语搜索 ……：新生情报工具（16）》
《反向面部识别、实时开源情报、推特可疑账户、网络摄像头地图、挖坟 ……新生情报工具（17）》
《深挖推特工具超长列表、寻找独立新闻源、物联网Dorks、泄漏数据、挖 Telegram、机器学习数据集、大牌流媒体资源 …… 新生情报工具（18）》
这里是第19集，依旧希望今天的内容能对您有用。

1、开源情报框架
OWASP Maryam 是一个基于 Recon-ng 的使用 Python 编写的开源情报工具框架。如果您具有 Metasploit 或 Recon-ng 的经验技能，完全可以轻松地直接使用它；如果没有，这里有一份快速指南。

从搜索引擎提取电子邮件、Docs、子域、社交网络
从Web来源提取 Links、CSS和JS文件、CDN链接、电子邮件、关键字
查找和暴力破解DNS、TLD
爬网搜索您的 RegExp
识别 WebApp、WAF、感兴趣的重要文件
并获得多种格式的报告
links：https://github.com/saeeddhqan/Maryam

2、开源推特前端 —— 专注于隐私
这是一个免费的开源替代 Twitter 前端，专注于隐私。

没有JavaScript或广告
防止Twitter跟踪您的IP或JavaScript指纹
非官方API（无速率限制，不需要开发者帐户）
轻量级（36KB，twitter.com是 580KB）
RSS feeds
移动支持（响应式设计）
在这里看到：https://github.com/zedeus/nitter

3、映射全球俄罗斯军事基地
Status-6 制作了一份文档，映射全球俄罗斯军事基地；包括军事单位，情报中心，国防研究基地等军事单位，情报中心，国防研究基地等。

如果您对军事方面的地缘政治感兴趣，这也许是一份很重要的资料。

绿色代表海军，蓝色代表空军，红色是地面部队及其他。

可以在这里下载它：https://mega.nz/file/o34z3aZY#nnA8_AioA35c-Jtq3dY0nqr52aH0PuU218Oa8ocoBJY

您可以使用 WinRAR 程序打开 zip 文件。

4、追踪事件的平台
对于调查者和公民记者来说会很有用，您将能够在这里看到对特定的主题标签、关键字或位置进行广泛的Twitter分析，这对追踪热点事件的工作是很有意义的：https://www.trendsmap.com/

5、用电影练习侦探挑战追踪：邦德在哪
还记得我们曾经做过的使用电影来练习追踪定位的方法吗？在这里看到《使用电影做侦探挑战演示：开源调查游戏》。当然，这篇演示中的题目难度较高。

bushidotoken 演示了一个类似的侦探挑战，与上述不同，这次它非常简单；但是，它足够体现开源情报调查中一些重要的技巧使用，尤其是思考方式/思路顺序 —— 他尝试使用开源情报技巧寻找 007 James Bond。

思路顺序的第一步就是，检查尽可能全面的线索。题目就是下图。

您看到了什么？显然第一眼看到的就是世界上最明显的地标：大本钟。还可以看到带有灰绿色屋顶的白色建筑物和邦德对面的维多利亚时代建筑。

因此，您可以在 Google Maps 上轻松找到大本钟。但仍然不知道邦德在哪。从视角上邦德似乎是从侧面看的，因为您可以在背景中看到威斯敏斯特宫。

更仔细检查图像，您可以看到一栋带有灰绿屋顶的建筑，即国防部（MoD），其后部是老式的办公大楼。因此，有了这个，您就可以知道这里是一个叫做白厅的地区，目标已经接近。

（Whitehall 是伦敦威斯敏斯特市内的一条大道，自特拉法加广场向南延伸至国会广场，亦为英国A3212号公路。这很容易在地图上看到，即便您不熟悉英国也没关系）

如果使用街景图来确认位置，您可以看到位于邦德前方的老式建筑。

来看一下 Shard Day 360 Photography，以收集更多的情报。这是一台摄像机，可以从欧洲最高的建筑物 — Shard 碎片大厦上对伦敦进行360度全景拍摄。

因此您可以发现皇家骑兵卫队大楼后面的陆军部大楼。

好了，现在可以确切定位邦德在哪了。重新看一下最初的照片。

显然，邦德是站在国贸部的屋顶上，在那里可以俯瞰白厅。

就是这么简单。它真的体现了思路，即：首先尽可能找到一切您可以利用的线索；其次从最显著的线索入手，如果行不通，那就退回去换另一个线索；每一个线索的采用您都需要在头脑中有清晰的判断，关于使用什么工具能进一步挖掘它。不要错过下面的思考方式介绍，它很重要：

《开源调查应该是一种心智：得到它你需要几个步骤》
我们汇总的 “侦探挑战游戏” 是很重要的思考方式和经验展示，您可以从中学到很多前辈的智慧。目前的内容您可以在下面回顾：

《好玩的间谍挑战》
《收集信息追踪钱的轨迹 — — 开源情报基础和一个调查示例》
《侦探挑战小游戏》
《让阴影说话：开源调查小游戏》
《使用电影做侦探挑战演示》
《侦探挑战：间接证据和排除法》
《在互联网上识别和追踪一个人的基本方法》
《侦探挑战游戏：快速地理定位的两种方法》
《那辆军车正驶向哪里？：侦探挑战时间》
《侦探挑战时间：让井盖和自行车说话》
《情报眼：细节越多暴露越大 — 侦探挑战游戏》
《空荡荡的蓝天上掠过一架飞机……你能知道地理位置吗？- 史上最难的侦探挑战》
《神探应该拥有很棒的直觉：侦探挑战小游戏演示追踪》
《一扇窗子能告诉你什么？：侦探挑战游戏》
持续更新中！更多好玩的演示相见 列表-5 直接行动 之 “开源情报”
6、挖掘推特的技能挑战
AwareOnline 发布了一个新的开源情报技能测验。测试您挖掘推特情报的能力。

您知道如何充分理由推特吗？如何使所有答案正确无误？可以测试一下您的水平：https://www.aware-online.com/quizzes/osint-twitter-challenge-en/

👉挖掘推特的基本方法在这里找到：

《从推特中挖掘真相不需要太复杂的工具：一个常用工具的全面指南》
在 列表-5“开源情报”板块中可以找到更多技巧：https://start.me/p/1kod2L/iyp-direct-action5

7、追踪极右翼
5月，有一台或多台Discord服务器遭到入侵和刮取。现在，145台服务器的大约1000万条消息全部可由DDoSecrets索引，并可通过其网站进行搜索。

于是它变成了一个宝库。

如果您对极右翼的内幕感兴趣，这里可以挖到别处没有的东西：https://whispers.ddosecrets.com/

8、继续补充分类工具列表
▶️搜警用无线电的工具 — — 实时收听警察、消防、EMS、航空和铁路音频源

scannerchannels.com

broadcastify.com/listen/

liveatc.net

onlinepolicescannerhq.com

police-frequencies.com

scannerbuddy.com

scannerfrequencies.com

▶️ 人脸识别搜索引擎：

pimeyes.com/en/

pictriev.com

how-old.net

ilooklikeyou.com

facesaerch.com

▶️博客搜索引擎

blogs.botw.org

bforblogging.com

blogs.bing.com

blogdire.com

blogville.us

blog-directory.org

blogflux.com

blog-search.com

blogtopsites.com

blogarama.com

bloggeries.com

bloggernity.com

bloggernow.com

bloggingforboomers.com

bloghub.com

bloglog.com

blogs-collection.com

showcase.joomla.org

ukblogdirectory.co.uk

theblogscope.com

blogdumps.com/index.php

createandgo.com/blog-search/

bloggingfusion.com

technorati.com

blawgsearch.justia.com

fishing4tech.com/mtbos.html

thevital.net

blogsearchengine.org

searchblogspot.com

yougotblogs.com

▶️ 区块链/比特币搜索引擎

blocksearchengine.com Blockchain Search Engine

blockchainola.com/blockchain-search-engine/ Blockchain search engine

blockchair.com Bitcoin search engine

blocks.press Blockchain Search Engine

coinmio.com Crypto Coin Search Engine

enjinx.io blockchain search

seekoin.com bitcoin search engine

spendabit.co bitcoin search engine

▶️冠状病毒搜索引擎

coronasearch.net academic papers

covidsearch.sinequa.com scientific content

covidscholar.com research

covidexplorer.in stats etc

covidsearch.korea.ac.kr real time question answering

covidseer.ist.psu.edu/search open research search

discovid.ai/search scientific knowledge

covidex.ai AI search

tmcovid.com text mining

covid-search.doctorevidence.com doc evidence

p2med.shinyapps.io/Cov19-Monkey/

cord-19.apps.allenai.org full-text search engine

kaggle.com/covid-19-contributions data & tools from kaggle community

ushospitalfinder.com Find and search Hospitals

symptoma.com Symptom checker

emergencycare.inccrra.org COVID-19 Emergency Provider Search

cord19.vespa.ai Covid-19 search engine

biocompare.com/Antibodies/ Antibody search

▶️ 冠状病毒研究工具

一个专门查找冠状病毒相关学术论文的搜索引擎 Covid-19：https://coronasearch.net/ 多语种

以及，搜抗体的工具：

antibodies.com

antibodies-online.com

citeab.com

biocompare.com/Antibodies/

labome.com/index.html

antibodyregistry.org

biozol.de/de

linscottsdirectory.com

abclonal.com

▶️生物医学资源搜索引擎：

biokde.com Biomed literature

pubplus.org Biomed literature

bmlsearch.com Biomed literature

openi.nlm.nih.gov Biomed image search

pubnet-svc.gersteinlab.org Pub Graph Utility

▶️补充网络摄像头dorks：

intitle:”live view” intitle:axis

intitle:”webcamXP 5”

inurl:view/index.shtml

intitle:”EvoCam” inurl:”webcam.html”

intitle:”Are living View / — AXIS”

intitle:axis intitle:”video server”

inurl:axis-cgi/jpg

▶️被警察杀死的人 — 地图数据库

killedbypolice.net

▶️ 暗网搜索引擎

boogle.store Genesus Search

darksearch.io

deepwebsearch.co

onionlandsearchengine.com

onionsearchengine.com

ahmia.fi

▶️社交媒体情报 — YouTube搜索引擎：

mattw.io/youtube-geofind/

channelcrawler.com

ytcomment.kmcat.uk Comment Finder

tagsyoutube.com

0px.moe/samplesearch/

▶️ 社交媒体情报 — Instagram 搜索引擎：

findtagz.com

gramvideoz.com

gramplaces.com

taginsta.com

gramfind.com

gramlook.com

gramuser.com

gramchecker.com

mixagram.com

▶️ 一站式：一次性在多个平台上搜索的工具 Query，您只需要输入关键字，选择想要的平台即可：query.vandesm14.ml

▶️ 查找最佳编程教程和编码资源：hacksource.xyz

▶️搜索数据泄露：

breachrecon.com

dehashed.com

evileaks.su

leakedsource.ru

monitor.firefox.com

ghostproject.fr

hacked-emails.com

hacknotice.com

haveibeenpwned.com

haveibeensold.app

haveibeencompromised.com

leaked.site

breachalarm.com

leak-lookup.com

leakcheck.io

databreach.es

scatteredsecrets.com

spycloud.com

nuclearleaks.com

databreaches.net

vigilante.pw

▶️搜索视频剪辑的工具：

vlipsy.com

getyarn.io

wingclips.com

▶️无线频率搜索工具

digitalfrequencysearch.com

shure.com/en-US/support/tools/frequency-finder

fccid.io/frequency-explorer.php

frequencycheck.com

interceptradio.com

wigle.net

freqfinder.akg.com

cellmapper.net/map

▶️查找用户ID的工具：

lookup-id.com Facebook

caius.github.io/github_id/

tweeterid.com

gettwitterid.com

otzberg.net/iguserid/ Instagram

注：关于Facebook User Id，可以参见这里的演示《搜人、照片、视频、位置 …… 大全：新的FB”图谱搜索”替代方案 — — 尤其强调防御》

▶️ 基于位置的搜索引擎

piperpal.com

taskiy.net

snaptrends.com

▶️地理定位训练

如果您想练习自己的地理定位技能，可以选择众多收集该信息并提供帮助的网站之一，例如：

itsfilmedthere.com/2012/05/my-top-10-most-wanted-missing-locations.html

地理定位是一套思考方式，而不仅仅是技术工具/思考方式可以复制，但必须有创新和应变能力，这样才能才能将它真正变成您自己的技能。

▶️ 文件共享网站搜索引擎

ddlsearch.free.fr

filediva.com

zippysharesearch.com

filejokersearch.com

uvrx.com

filesearchengine.blogspot.com

googledrivesearch.com

sharedigger.com

anyfiles.org

▶️ 搜索数据集的工具

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

▶️ 缓存工具

cachedview.com

viewcached.com

cachedviews.com

pagecached.com

cache.nevkontakte.com

cachedwebpages.com

cachedpages.com

cachearchive.com

▶️ 推特位置工具 （分析人、人群、热点议题和热点事件）

tweepsmap.com

trendsmap.com

onemilliontweetmap.com

socialbearing.com/geo

app.teachingprivacy.org

geosocialfootprint.com

keitharm.me/projects/tweet/ Tweet Mapper

seekatweet.com

tweeplers.com

▶️ 关键字查询工具

keywordtool.io

keyword.io

semscoop.com

keywordtool.net

app.kparser.com

mykeyworder.com

serpstat.com

keywordsheeter.com

▶️ 反向链接查询工具 #SEO

serpstat.com/backlinks/

neilpatel.com/backlinks/

webmeup.com

linkquidator.com

backlinkshitter.com

backlinkr.net

ranksignals.com

backlinkwatch.com

real-backlinks.com/en

▶️ 查找Google自定义搜索引擎

site:google.com inurl:cse search engine

site:google.com inurl:cse inurl:cx=

publicurl:cse.google.com/cse?cx= search engine

inurl:cse inurl:cx= custom search engine

▶️ URL恶意软件分析工具

urlscan.io

virustotal.com/gui/home

hybrid-analysis.com

sitecheck.sucuri.net

global.sitesafety.trendmicro.com

metadefender.opswat.com

joesandbox.com

urlvoid.com

getlinkinfo.com

▶️Wiki 搜索平台：

wiktionary.org

wikinews.org

wikiversity.org

wikivoyage.org

wikipedia.org

wikibooks.org

wikiquote.org