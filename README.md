$${\huge \color{#00FFFF}cxfllist}$$



$${\large ⚡️{\color{#ff00dd}The\ best\ rule\ lists\ of\ Ad\ block\ and\ privacy\ for\ Chinese\ babies\ on\ the\ browser}⚡️}$$



$${\large 浏览器上最适合中国宝宝体质、最全、最有效的\ {\color{red}广告拦截} \ {\color{lightblue}和} \ {\color{green}隐私}\ 规则集}$$



<br>



## 说在前面

> [!IMPORTANT]  
> 本文是基于 ![](https://img.shields.io/badge/uBlock-Origin-%23800000?logo=ublockorigin&logoColor=red&logoSize=auto) (简称 `ubo` ) 来写的，请在 `安装完` 后继续往下看。
>
> [Adblock Plus](./ABP_filters.md) ${\large \color{#ff8000}← 其他用户请点击查看对应文章 →}$ [Vivaldi](./Vivaldi_filters.md)
>
> ${\color{#5dff00} 安装ubo：}$  
> 如果你是 ![](https://img.shields.io/badge/Google-Chroium-%234285F4?logo=googlechrome&logoSize=auto) 内核的浏览器，点击👉 [这里](https://www.crxsoso.com/webstore/detail/cjpalhdlnbpafiamejdnhcphjbkeiagm)  
> 如果你是 ![](https://img.shields.io/badge/Firefox-Gecko-orange?logo=firefoxbrowser&logoSize=auto) 内核的浏览器，点击👉 [这里](https://www.crxsoso.com/firefox/detail/ublock-origin)





> [!WARNING]  
> 所谓的主流订阅规则集，只能尽全力帮助你屏蔽广告和跟踪，但不能绝对、百分百屏蔽。  
>
> ${\large {\color{#FF00FF}因此，如果想要\ {\color{red}充分地满足自定义的需求}，你需要\ {\color{yellow}自己写规则}，或者\ {\color{yellow}给我提issue}}}$



<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>




## 快速指南

> [!IMPORTANT]  
> ### 1. 新手、普通用户，建议 `仅` 操作 👉 [基础版](#基础版)
>
> 2. 高级玩家（需要一定的技术积累），建议全篇看完
>
> 3. 作者同款 👉 [规则](#作者本人使用规则)（新手不建议 ❌）



<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>




## 从DNS上过滤（锦上添花）

> [!WARNING]  
> 如果你 `总是开代理上网` ，并且 `配置了分流规则` ，那么我 `墙裂推荐` 你操作这一步。
> 
> ${\Large \color{red} 如果你不是，请忽略这一节。}$  

 


### 配置本地(直连)dns服务器

<table align="center">
    <tr>
      <th align="center">分类\性质</th><th align="center">优点</th><th align="center">缺点</th>
    </tr>
    <tr>
      <td align="center">运营商DNS</td><td align="center">理论解析最快、不用配置</td><td align="center">墙特别高、会投放广告、dns劫持多</td>
    </tr>
    <tr>
      <td align="center">国内大厂DNS</td><td align="center">较稳定、解析较快、不投广告</td><td align="center">不少大厂现在开始限速了（这是趋势）</td>
    </tr>
    <tr>
      <td align="center">国外大厂DNS</td><td align="center">较稳定、不限速、不投广告</td><td align="center">解析较慢、可能会被运营商劫持</td>
    <tr>
      <td align="center">小众公益DNS</td><td align="center">隐私保护好、不投广告且自带去广告、一般没有劫持</td><td align="center">稳定性一般</td>
    </tr>
</table>


* 国内大厂DNS

  * 🌟腾讯：限速，但限得不多，推荐

    * DoT/DoQ：`dot.pub`
    * DoH：`https://doh.pub/dns-query`

  * 阿里：限速，但设备使用还行，多设备限速明显

    * DoT/DoQ：`dns.alidns.com`
    * DoH：`https://dns.alidns.com/dns-query`


* 国外大厂DNS

  * 🌟思科：速度出奇好（可能跟地区有关），推荐

    * DoT/DoQ：`dns.opendns.com`
    * DoH：`https://doh.opendns.com/dns-query`

  * 谷歌：解析较慢，可能会被运营商假冒（广州联通）

    * DoT/DoQ：`dns.google`
    * DoH：`https://dns.google/dns-query`

  * cloudflare：解析较慢

    * DoT/DoQ：`security.cloudflare-dns.com`
    * DoH：`https://security.cloudflare-dns.com/dns-query`

* 小众公益DNS

  * 18bit

    * DoT/DoQ：`dns.18bit.cn`
    * DoH：`https://doh.18bit.cn/dns-query`


> [!TIP]  
>
> **Q/A**
> 
> 1. 运营商dns的坑？
> > 现在很多运营商的dns都由`南京信风`公司代理，也就是114dns的厂商，被扒过`投毒`、`监控`、`劫持`、`高墙`等问题，详情请看👉[这里](https://www.landiannews.com/archives/18431.html)
> 
> 2. 限速标准？
> > 阿里云：按照请求源 IP 进行并发数限制，单个 IP 的请求数超过 20QPS、UDP/TCP 流量超过 2000bps 将触发限速策略  
> > 
> > 腾讯云：对单个域名限制并发 20QPS（影响比阿里云小很多）
> 
> 3. 运营商假冒？
> > 广州联通，路由追踪8.8.8.8，没出地级市就到8.8.8.8了
> 
> 4. dot和doh的区别？
> > dot由于 TLS 协议的轻量级封装和较少的额外开销，`只在理论上dot会比doh快`:sweat_smile:，如果算上`墙的高度`等等因素，两者速度就见仁见智了，因为doh将 DNS 查询和响应封装在 HTTPS 请求中，`更易于穿透某些网络配置，尤其是防火墙和代理服务器`。两者的选择看实际情况，比如地区、运营商、网络环境等等因素。
> 
> 5. 选择其他dns？
> > `其他的国内不一定能用`，可在👉[adguard的公共dns列表](https://adguard-dns.io/kb/zh-CN/general/dns-providers/)、[dns评测](https://www.zyha.cn/select-a-good-public-dns-in-2024/) 中寻找。  




### 配置远程dns服务器  

* Hagezi's DNS - Pro

    * DoT/DoQ：`x-hagezi-pro.freedns.controld.com`
    * DoH：`https://freedns.controld.com/x-hagezi-pro`  

> [!IMPORTANT]  
>
> 配置了此dns后，下面提及的 ~~`hagezi pro`~~ `hagezi pro mini` 可以不添加了，因为这个规则集已经在dns服务器上部署了。





<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>





## 基础版

> [!IMPORTANT]  
> 这个版本适合 `只浏览国内网站`，或者 `很少时间` 浏览国外网站，或者 `对跟踪隐私方面没啥感觉` 的宝宝，已经非常够用了！



> $${\Large {保留\ {\color{lightgreen}初始状态的默认规则} + 导入\ {\color{lightgreen}国内必备规则：}}}$$


$${👇}$$


<details>

<summary align="center"><h3><code><strong>🌟详细说明</strong></code></h3></summary>

<br/> 


${\color{#5dff00} 初始状态的默认规则：}$  

| 规则列表 | 介绍 |
| :--------: | :-------: |
| `内置` | <i>ubo自己最核心的规则集</i> |  
| `EasyList` | <i>最主流的国际网站的广告过滤规则</i> |  
| `EasyPrivacy` | <i>最主流的反跟踪规则</i> | 
| `Online Malicious URL blocklist` | <i>用于阻止访问恶意或危险网站的列表，加强网络安全</i> | 
| `Peter Lowe's Ad and tracking server list` | <i>只包含广告和跟踪服务器 `主机` 的拦截列表</i> | 
| `AdGuard Chinese（中文）` | <i>`Easylist China` 的改良版本，最主流的国内网站的广告过滤规则</i> | 

${\color{#5dff00} 国内必备规则：}$  

| 规则列表 | 介绍 |
| :--------: | :----------: |
| [`CJX's Annoyance List`](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt) | <i><kbd>easylist china</kbd> 的补充，主要屏蔽国内网站页面上烦人的元素</i> | 
| [`CJX's ublock list`](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt) | <i>对 Easylist + Easylist China + Easyprivacy + cjx's Annoyance List的补充</i> | 
| [`轻量广告拦截规则`](https://raw.githubusercontent.com/damengzhu/banad/main/jiekouAD.txt) | <i>主要去除色情悬浮广告</i> |  
| [`NoAppDownload`](https://raw.gitmirror.com/Noyllopa/NoAppDownload/master/NoAppDownload.txt) | <i>去除各种网页上的 APP 下载或跳转提示</i> |
| [`乘风广告过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt) | <i>国内网站广告过滤规则的后起之秀</i> | 
| [`乘风视频过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt) | <i>国内视频网站的广告过滤规则</i> | 
| [`乘风小众视频过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt) | <i>国内小众视频网站的广告过滤规则</i> | 
| [`runningcheese's Adblock_Popup`](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt) | <i>属于网页弹窗过滤规则的补充</i> | 
| [`runningcheese's Adblock_Watermark`](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt) | <i>去除国内网页水印的规则，包括AI、文档、设计等平台</i> | 
| [`cxfl's ublock list`](https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt) | 本人维护，对所有规则集的补充，主要为屏蔽网页烦人元素，包括对某些规则的修复，请在添加完所有订阅规则后再添加 |

> ${\color{#5dff00}Tip：}$  
>
> 对于国内必备规则，你可以在下面进行 `一键导入 (墙裂推荐)`，也可以选择其中的一些规则，名称上右键复制链接地址再导入。

</details>

$${👇}$$



### 国内必备规则一键复制导入：

```
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt
https://raw.githubusercontent.com/damengzhu/banad/main/jiekouAD.txt
https://raw.githubusercontent.com/Noyllopa/NoAppDownload/master/NoAppDownload.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt
https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt
```


> $${\Large \color{red}新手、普通用户到此结束}$$
---


<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>



## 增强版

> [!IMPORTANT]  
> 如果你跟我一样，`经常浏览国外平台，查阅国外新闻、资料等`，或者你 `对跟踪隐私非常敏感`，那么这个版本也许更适合你（说白了，就是 `国内` + `国外` 的使用习惯）。



> [!WARNING]  
> 这个版本 有可能会造成某些网站页面 `排版异常`，需要有一定的 `规则书写知识`，`找到造成异常的规则并修复`，用起来才会舒服。
> 
> ${\Large \color{red}否则，建议你使用基础版。}$


<br>


> $${\Large {设置\ {\color{lightgreen}基础版中的所有规则} + 选择性导入\ {\color{lightgreen}以下不同类目的规则：}}}$$


$${👇}$$


<details>

<summary align="center"><h3><code><strong>🌟详细说明</strong></code></h3></summary>


<br/>


> ${\color{#b83eff}Important：}$  
> 
> :star2: 为 `推荐` 订阅规则。规则名称上右键复制订阅地址，导入即可，也可以用下面的一键导入。


<br/>



* cookie  

| 规则列表 | 介绍 |
| :----: | :----: |  
| `🌟 Easylist/ubo - Cookie Notices (ubo中勾选)` 与 [`I don't care about cookies`](https://www.i-dont-care-about-cookies.eu/abp/) | <i>对列表中的网站采取最少cookie允许策略，屏蔽弹出的cookie接受窗口</i> |  


> ${\color{#5dff00}Tip：}$  
> 
> [自从uBO 能够设置 cookie 和本地/会话存储条目以来](https://www.reddit.com/r/uBlockOrigin/comments/1961919/easylist_cookie_notices_how_does_it_work/#:~:text=uBO%20has%20the%20capability%20to%20set%20cookies%20and%20local/session%20storage%20entries%2C%20and%20also%20to%20click%20elements%20on%20webpages.)，两者的差别目前主要就是网站cookie的接受策略。对于它们两个之间哪个更好，众说纷纭。观看两者的一些讨论👉[①](https://community.brave.com/t/why-is-easylist-cookie-list-included-but-not-i-dont-care-about-cookies/321405) [②](https://community.brave.com/t/feature-request-add-i-dont-care-about-cookies-filter/244984)👈，本人用 Easylist cookie :joy:，当然你也可以两个都添加



<br/>


* 烦人元素  

| 规则列表 | 介绍 |
| :----: | :----: |
| `🌟 uBlock filters – Annoyances（ubo中勾选）` | <i>ubo自己的烦人元素过滤规则</i> | 
| `🌟 Easylist - Annoyances（ubo中勾选）` | <i>Easylist的烦人元素过滤规则</i> | 
| [`Web Annoyances Ultralist（修复版）`](https://raw.githubusercontent.com/LanikSJ/webannoyances/master/ultralist.txt) | <i>旨在移除阻挡屏幕视图的讨厌网页元素，如固定标题、悬浮导航、社交图标等比较广泛的元素</i> |
| [`🌟 yokoffing's Annoyances List`](https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt) | <i>一个精心策划的列表，捕获了其他维护者错过的麻烦。它还清理了许多网站周围的混乱（例如，相关文章、“阅读更多”等）。</i> | 
| [`🌟 Browse websites without logging in`](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/BrowseWebsitesWithoutLoggingIn.txt) | <i>此列表尝试绕过站点上的强制登录。</i> | 
| [`🌟 Adblock Warning Removal List`](https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt) | <i>某些网站会检测到用户使用了广告拦截器，并显示警告信息，要求用户禁用广告拦截器才能继续访问网站内容，此规则就是用于去除这些警告</i> |

> ${\color{#5dff00}Tip：}$  
> 
> 其中的 `Web Annoyances Ultralist` 对部分国外网站的损坏严重，`不建议` 使用。
 

<br/>


* 安全  

| 规则列表 | 介绍 |
| :----: | :----: |
| ~~[`oisd big`](https://big.oisd.nl/)~~ | ~~<i>阻止广告、(Mobile) 应用程序广告、网络钓鱼、恶意广告、恶意软件、间谍软件、勒索软件、加密劫持、诈骗、...遥测/分析/跟踪（正常功能不需要时）</i>~~ | 
| ~~[`hagezi pro`](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt)~~ | ~~<i>阻止广告、联盟、跟踪、指标、遥测、网络钓鱼、恶意软件、诈骗、假货、硬币和其他 "垃圾"</i>~~ | 
| [`🌟 hagezi pro mini`](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt) | <i>针对网络浏览器优化的 Hagezi Pro DNS 阻止列表的较小版本（78k 与 159k 规则）。简化的列表排除了与网页浏览无关的规则，例如阻止物联网跟踪和设备遥测的规则。此迷你版本可阻止与广告、跟踪、分析和恶意软件相关的域。</i> | 
| [`oisd nsfw`](https://nsfw.oisd.nl/) | <i>最全的 <kbd>色情、惊悚、成人</kbd> 服务器主机屏蔽列表</i> | 
> ${\color{#5dff00}Tip：}$  
> 
> `Peter Lowe's Ad and tracking server list`、`oisd big` 已经被淘汰了，因为 `hagezi pro` 更强更高效，详情请看👉[①](https://github.com/hagezi/dns-blocklists/issues/2346#:~:text=There%20is%20also%20Peter%20Lowe%27s%20Ad%20and%20tracking%20list%20if%20someone%20really%20only%20wants%20to%20block%20ads%20and%20tracking.) [②](https://www.reddit.com/r/nextdns/comments/192mdeh/why_should_i_use_hagezi_in_place_of_oisd/)👈。然后，它的mini版本 `hagezi pro mini` 更适合在浏览器上使用。不过我本人通过使用 `hagezi pro++` 的DNS进行过滤 :joy:
>
> 因此，如果你添加了`hagezi pro mini`，请把 `Peter Lowe's Ad and tracking server list` <kbd>取消勾选</kbd>。


<br/>


* AI

| 规则列表 | 介绍 |
| :----: | :----: |
| [`Huge AI Blocklist`](https://raw.githubusercontent.com/laylavish/uBlockOrigin-HUGE-AI-Blocklist/main/list.txt) | <i>过滤Google、DuckDuckGo、Bing中部分涉及AI网站的屏蔽规则</i> |

> ${\color{#5dff00}Tip：}$  
> 
> `Huge AI Blocklist` 这个列表的初心其实是为了屏蔽AI生成的图像，但它的写法却直接把属于 AI 领域的域名的所有链接都屏蔽了，只能说写法不够好吧，只适合那些完全不想看到任何一点有关 AI 的用户。


</details>

<br/>

$${👇}$$

<br/>


### 一键导入推荐规则：
```
https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt
https://raw.githubusercontent.com/DandelionSprout/adfilt/master/BrowseWebsitesWithoutLoggingIn.txt
https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt
https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt
```



<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>


## 优化版

> [!IMPORTANT]  
> 这个版本是针对以上提到的部分规则集的 `精简优化`，可以使用优化后的规则集进行替换。


<br>
<br>


1) [Easylist (45k Optimized vs. 87k Original)](https://filters.adtidy.org/extension/ublock/filters/101_optimized.txt)
> [!WARNING]  
> 这个优化版本可能会让一些网站的广告屏蔽失效，本人 `不太建议使用`。如果发现确实有问题，请换回原版。

2) [EasyPrivacy (14k Optimized vs. 50k Original)](https://filters.adtidy.org/extension/ublock/filters/118_optimized.txt)
> [!TIP]  
> 这个版本还不错，可以使用。

3) [Fanboy Annoyances (56k Optimized vs. 81k Original)](https://filters.adtidy.org/extension/ublock/filters/122_optimized.txt) == `Easylist cookie notices` + `Easylist social widgets`
> [!IMPORTANT]  
> 使用此规则你需要 <kbd>取消勾选</kbd> `Easylist - Cookie Notices` 和 `Easylist social widgets`，<kbd>保留</kbd> `uBlock filters – Cookie Notices`



<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>




## 高级设置（✔我是高级用户）

| **Setting**            | **Value** |             **Description**                  |
|-------------------------------|-----------|--------------------------------------------------------------------------------------|
| `autoUpdateAssetFetchPeriod`    | `10`    |  自动更新程序在获取下一个过滤器列表之前等待 `x` 秒    |
| `autoUpdateDelayAfterLaunch`    | `10`     |  浏览器启动后 `x` 秒更新过时的过滤器列表             |
| `autoUpdatePeriod`              | `1`     |  uBO 每 `x` 小时检查一次过滤器列表更新              |
| `cnameMaxTTL`                   | `720`   |       将 CNAME 别名缓存 `x` 分钟                      |
| `filterAuthorMode`              | `true`  |                  启用动态过滤                    |
| `updateAssetBypassBrowserCache` | `true`  |   当手动获取过滤器列表的频率超过每小时时绕过缓存       |



<br>

$${👇}$$

$${👇}$$

$${👇}$$

<br>



## 作者本人使用规则


<details>


<summary><h3><code><strong>点击展开</strong></code></h3></summary>

<br>


> ![](https://raw.githubusercontent.com/fenglingback/cxfllist/main/images/作者同款.png)
>
> 勾选 `内置`、`EasyList`、`Online Malicious URL blocklist`、`EasyList/uBO - Cookie Notices`、`Easylist - Annoyances`、`uBlock filters - Annoyances`、`AdGuard Chinese（中文）`，导入以下自定义规则订阅链接：
>
>
> ```
> https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
> https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt
> https://raw.githubusercontent.com/damengzhu/banad/main/jiekouAD.txt
> https://raw.githubusercontent.com/Noyllopa/NoAppDownload/master/NoAppDownload.txt
> https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt
> https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt
> https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt
> https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt
> https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt
> https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt
>
> https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt
> https://raw.githubusercontent.com/DandelionSprout/adfilt/master/BrowseWebsitesWithoutLoggingIn.txt
> https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt
> https://filters.adtidy.org/extension/ublock/filters/101_optimized.txt
> https://filters.adtidy.org/extension/ublock/filters/118_optimized.txt
> ```
>


<br>



</details>



$${👇}$$

$${👇}$$

$${👇}$$



<br>



## 说说我个人对规则列表的看法


网络上的规则列表太杂了，对于一些相同想法的屏蔽规则，我认为是需要统一、各大维护者进行沟通后达成共识进行合并的。同时，差异化的东西才做成自己的独特列表，并且一旦差异化消除，也需要合并到共同规则上去。否则，列表参差不齐，维护困难还浪费资源。


<br>
<br>


$${\Large {\color{red}Let's}\ {\color{white}Clear}\ {\color{#00bfff}the}\ {\color{#ffa600}Internet}\ {\color{#1bb32b}together} ❗}$$


<br>



[![https://gafam.info](https://ptrace.gafam.info/unofficial/img/color/lqdn-gafam-poster-en-color-5x1-2560x.png)](https://gafam.info)



<br>
<br>
<br>



<div align='center'><a href='https://www.websitecounterfree.com'><img src='https://www.websitecounterfree.com/c.php?d=9&id=53889&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>Since &nbsp;2024.05.15</div>


