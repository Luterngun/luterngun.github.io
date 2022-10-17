---

layout: post

title: 免注册浏览国际主流网站——隐私强化前端的简单应用

date: 2022-10-17

categories: Archive

tags: 隐私

description: 隐私强化型前端：免注册、免登陆、去 JavaScript、去广告（甚至免翻墙）访问 Twitter、YouTube、Google、Reddit 等墙外主流网站

---

credit：[2047｜libgen.eth：更隐私友好的 Google/Youtube/Reddit/Twitter/Wikipedia 镜像列表（新增 Zlibrary）](https://2047.one/t/17955)
 
## 介绍
在软件架构中，前端 (front-end) 与终端用户直接交互，后端负责数据存储、内容管理。以推特为例，前端可以理解为用户在网页或客户端 App 看到的界面。第三方前端可以理解为「新瓶装旧酒」——用户看到的仍是同样的内容，只是呈现方式不同。至于为什么需要「新瓶」，是因为各大国际主流网站的官方前端/「旧瓶」往往被追踪脚本和广告污染，或存在强制登录账号才能浏览全部内容等限制，而经过隐私强化的第三方前端针对性地去除了 JavaScript 和广告，允许用户【免注册】、【免登录】访问社交网站上的全部内容，有些还提供 RSS 订阅、下载内容等额外功能，使用户获得隐私友好的上网体验。隐私强化前端均为自由开源软件，在安全性上也有一定的保证。  

隐私强化前端的【去中心化】优势也使得它们可被用于绕过 GFW 对 Twitter/Reddit/YouTube 等网站的封锁——前端拥有众多实例，同时允许用户自托管（在自己的 VPS 上搭建服务）——等于变相为域名单一的中心网站建立了无数的【镜像站】，可让 GFW 防不胜防。不过 HTTPS 连接中的 SNI /域名信息对 GFW 仍是可见的，因此 GFW 可以在 SNI 检测后根据关键词进行封锁，比如对知名前端「nitter」、「whoogle」、「invidious」进行封锁（它们已经这样做了）。相比知名的中心化网站，在 GFW 的审查变得困难的同时，墙内民众获取去中心化镜像站的难度也随之上升了，因此将【隐私强化前端】用作【翻墙软件】的替代、在墙内【免翻墙】访问外网的方法未必能够普及。Luterngun 仍然建议先使用【翻墙软件】，再使用【隐私强化前端】锦上添花。如果你仍想用这种方式绕墙，无论是使用现有的前端实例，还是想自托管服务，都建议避免使用「nitter」等包含前端项目名字的明显字眼，以此增加 GFW 的审查难度。

以下是 [LibRedirect](https://libredirect.github.io/) 列举的主流网站及对应的隐私友好前端项目（部分项目顺序经过调整，并加入注释）：

- Twitter =>   
   [Nitter](https://github.com/zedeus/nitter)
- YouTube =>  
   [Invidious](https://github.com/iv-org/invidious),  
   [Piped](https://github.com/TeamPiped/Piped),  
   [Piped-Material](https://github.com/mmjee/Piped-Material),  
   [CloudTube](https://sr.ht/~cadence/tube/) [FreeTube](https://github.com/FreeTubeApp/FreeTube),  
   [Yattee](https://github.com/yattee/yattee)  
- Google Search =>  
   [Whoogle](https://benbusby.com/projects/whoogle-search/)  
   [SearXNG](https://github.com/searxng/searxng),  
   [SearX](https://searx.github.io/searx/),  
   [LibreX](https://github.com/hnhx/librex),  
- Instagram =>   
   [Bibliogram](https://sr.ht/~cadence/bibliogram/)（大多数不可用）  
- TikTok =>   
   [ProxiTok](https://github.com/pablouser1/ProxiTok)
- Reddit =>  
   [Libreddit](https://github.com/spikecodes/libreddit),  
   [Teddit](https://codeberg.org/teddit/teddit)  
- Imgur =>   
   [Rimgo](https://codeberg.org/video-prize-ranch/rimgo)  
- Wikipedia =>   
   [Wikiless](https://codeberg.org/orenom/wikiless)  
- YouTube Music =>  
   [Beatbump](https://github.com/snuffyDev/Beatbump),  
   [Hyperpipe](https://codeberg.org/Hyperpipe/Hyperpipe)  
- Medium =>   
   [Scribe](https://sr.ht/~edwardloveall/Scribe/)  
- Quora =>   
   [Quetre](https://github.com/zyachel/quetre)  
- Reuters =>   
   [Neuters](https://github.com/HookedBehemoth/neuters)  
- Peertube =>   
   [SimpleerTube](https://git.sr.ht/~metalune/simpleweb_peertube)  
- LBRY/Odysee =>  
   [Librarian](https://codeberg.org/librarian/librarian),  
   [LBRY Desktop](https://lbry.com/get)  
- IMDb =>   
   [libremdb](https://github.com/zyachel/libremdb)  
- Translate =>  
   [SimplyTranslate](https://git.sr.ht/~metalune/simplytranslate_web),  
   [LingvaTranslate](https://github.com/TheDavidDelta/lingva-translate),  
   [LibreTranslate](https://github.com/LibreTranslate/LibreTranslate)  
- Maps =>   
   [OpenStreetMap](https://www.openstreetmap.org/)  
- Send Files（Firefox Send 的后继，临时网盘/文件传输） =>   
  [Send](https://github.com/timvisee/send)  
  
## 应用

### 直接使用实例

你可以手动将上述受支持的主流网站的域名替换成隐私强化前端实例的域名，域名后的地址内容保持不变，比如，将 https://twitter.com/WhiteHouse 换成 https://nitter.net/WhiteHouse，将 https://www.youtube.com/watch?v=UKX0bpmRJxM 换成 https://invidious.tiekoetter.com/watch?v=UKX0bpmRJxM。

### 使用辅助工具
除了手动修改，你也可以结合使用集成式的浏览器扩展/插件或客户端 App 实现域名自动跳转/重定向。

- [LibRedirect](https://libredirect.github.io/) – Firefox/Chromium 浏览器扩展  
	- 源码：[GitHub](https://github.com/libredirect/libredirect)  
	- 下载地址：  
		- [Firefox 扩展](https://addons.mozilla.org/firefox/addon/libredirect/)  
		- [Chromium 扩展](https://github.com/libredirect/libredirect/blob/master/chromium.md)  
- [UntrackMe](https://framagit.org/tom79/nitterizeme) – 安卓客户端  
	- [源码](https://framagit.org/tom79/nitterizeme)  
	- 下载地址：[F-Droid](https://f-droid.org/app/app.fedilab.nitterizeme)   
- 隐私强化实例导航站：[Farside](https://farside.link/)｜[GitHub](https://github.com/benbusby/farside)（由 libgen 介绍）   
- 更多被封锁网站的镜像导航站：[https://unblockit.pages.dev](https://unblockit.pages.dev)（由 libgen 介绍）
- ~~[Privacy Redirect](https://github.com/SimonBrazell/privacy-redirect)~~ – 浏览器插件，不推荐理由：2021年12月至今未更新  

除了重定向插件，你也可以搭配 RSS 阅读器（参见：[ALL-about-RSS](https://github.com/AboutRSS/ALL-about-RSS)）使用那些提供 RSS 订阅的前端服务，比如 Nitter 和 Invidious，这样有利于信息集中统一管理、缓解信息焦虑、免受推荐算法操纵。
