# $${\color{#00FFFF}cxfllist}$$

<h3 align="center">⚡️The most complete and useful rule-list of Ad and tracking for Chinese babies on the browser.⚡️</h3>  

### $${浏览器上最适合中国宝宝体质、最全、最有效的\ {\color{red}广告} \ {\color{lightblue}和} \ {\color{green}隐私}\ 规则集}$$

<br>




## 说在前面
> [!WARNING]  
> 所谓的主流订阅规则集，只能尽全力帮助你屏蔽广告和跟踪，但不能绝对、百分百屏蔽。  

### $${{\color{#FF00FF}因此，如果想要\ {\color{red}充分地满足自定义的需求}，你需要\ {\color{yellow}自己写规则}，或者\ {\color{yellow}给我提issue}}}$$


$${👇}$$

$${👇}$$

$${👇}$$


## 涉及的规则介绍
> [!TIP]  
> `EasyList`：<i>最主流的国际网站的广告过滤规则</i>  
> `Easylist China`：<i>最主流的国内网站的广告过滤规则</i>  
> `EasyPrivacy`：<i>最主流的反跟踪规则</i>  
> `CJX's Annoyance List`：<i><kbd>easylist china</kbd> 的补充，主要屏蔽页面上烦人的元素</i>  
> `DuckDuckGo Tracker Radar`：<i>也是一个反跟踪规则，精简但高效，甚至能屏蔽一些网站的指纹识别</i>  
> `Adblock Warning Removal List`：<i>某些网站会检测到用户使用了广告拦截器，并显示警告信息，要求用户禁用广告拦截器才能继续访问网站内容，此规则就是用于去除这些警告</i>  
> `Malicious URL blocklist`：<i>用于阻止访问恶意或危险网站的列表，加强网络安全</i>  
> ~~`Peter Lowe's Ad and tracking server list`：<i>只包含广告和跟踪服务器主机的拦截列表</i>~~  
> `Web Annoyances Ultralist`：<i>又一个屏蔽页面上烦人元素的规则集</i>  
> `I don't care about cookies`：<i>对列表中的网站采取最少cookie允许策略，屏蔽弹出的cookie接受窗口</i>  
> `乘风广告过滤规则`：<i>国内网站广告过滤规则的后起之秀</i>  
> `乘风视频过滤规则`：<i>国内视频网站的广告过滤规则</i>  
> `乘风小众视频过滤规则`：<i>国内小众视频网站的广告过滤规则</i>  
> `runningcheese's Adblock_Popup`：<i>属于网页弹窗过滤规则的补充</i>  
> `runningcheese's Adblock_Watermark`：<i>去除国内网页水印的规则，包括AI、文档、设计等平台</i>  
> ~~`oisd big`：<i>阻止广告、(Mobile) 应用程序广告、网络钓鱼、恶意广告、恶意软件、间谍软件、勒索软件、加密劫持、诈骗、...遥测/分析/跟踪（正常功能不需要时）</i>~~  
> ~~`hagezi pro`：<i>阻止广告、联盟、跟踪、指标、遥测、网络钓鱼、恶意软件、诈骗、假货、硬币和其他 "垃圾"</i>~~
> `hagezi pro mini`：<i>针对网络浏览器优化的 Hagezi Pro DNS 阻止列表的较小版本（78k 与 159k 规则）。简化的列表排除了与网页浏览无关的规则，例如阻止物联网跟踪和设备遥测的规则。此迷你版本可阻止与广告、跟踪、分析和恶意软件相关的域。</i>  
> `oisd nsfw`：<i>最全的 <kbd>色情、惊悚、成人</kbd> 规则集</i>  
> `CJX's ublock list`：<i>对 easylist + easylistchina + easyprivacy + cjx's Annoyance List的补充</i>  
> `cxfl's ublock list`：本人维护，对以上所有规则集的补充，主要为屏蔽网页烦人元素，请在添加完以上主流订阅规则后再添加  
> `cxfl-adblockplus自定义规则`：本人维护，等同于 <kbd>cjx补充</kbd> + <kbd>cxfl's ublock list</kbd>

> [!WARNING]  
> `Peter Lowe's Ad and tracking server list` 和 `oisd big` 已经被我淘汰了，因为 `hagezi pro` 更强更高效，详情请看👉[①](https://github.com/hagezi/dns-blocklists/issues/2346#:~:text=There%20is%20also%20Peter%20Lowe%27s%20Ad%20and%20tracking%20list%20if%20someone%20really%20only%20wants%20to%20block%20ads%20and%20tracking.) [②](https://www.reddit.com/r/nextdns/comments/192mdeh/why_should_i_use_hagezi_in_place_of_oisd/)👈。然后，它的mini版本 `hagezi pro mini` 更适合在浏览器上使用。不过我本人用 `hagezi pro++` :joy:

$${👇}$$

$${👇}$$

$${👇}$$


## 从DNS上过滤（锦上添花）

> [!WARNING]  
> 如果你总是开代理上网，并且配置了分流规则，那么我强烈推荐你操作这一步。
> $${\color{red} 如果你不是，请忽略这一节}$$



### 配置远程dns服务器  
* Hagezi's DNS - Pro
    * DoT/DoQ：`x-hagezi-pro.freedns.controld.com`
    * DoH：`https://freedns.controld.com/x-hagezi-pro`
> [!IMPORTANT]  
> DoT/DoH和DoH这两种解析方式任选其一，理论上DoT/DoQ会比DoH快，`只是理论上`:sweat_smile:  
>
> 那么此时，下面提及的 ~~`hagezi pro`~~ `hagezi pro mini` 可以不添加了，因为这个规则集已经在dns服务器上部署了。


$${👇}$$

$${👇}$$

$${👇}$$


## AdblockPlus `ABP` (本人只为了给 Vivaldi 用，不用 Vivaldi 只建议用下面的ubo)

### 只有 PC 端


> [!IMPORTANT]  
> :star2: 为 `必用规则` ，强烈推荐使用。如果使用AdblockPlus，请保留 `ABP filters` 。如果有EasyListChina + EasyList，就点击右侧的垃圾桶 <kbd>取消订阅</kbd> 。


### 选择你需要的规则集，然后右键复制它的链接地址，到设置->高级->通过URL添加过滤列表:

* :star2: [EasyList (Vivaldi内置) ](https://easylist-downloads.adblockplus.org/easylist.txt)
* :star2: [EasyList China (Vivaldi内置) ](https://easylist-downloads.adblockplus.org/easylistchina.txt)
* :star2: [EasyPrivacy (Vivaldi内置) ](https://easylist-downloads.adblockplus.org/easyprivacy.txt)
* :star2: [DuckDuckGo Tracker Radar `Vivaldi内置，且ABP无法添加` ](https://downloads.vivaldi.com/ddg/tds-v2-current.json)
* :star2: [Adblock Warning Removal List (Vivaldi内置)](https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt)
* [Malicious URL blocklist `只能Vivaldi用，ABP无法添加 (添加到Vivaldi中的跟踪器列表)`](https://malware-filter.gitlab.io/malware-filter/urlhaus-filter-vivaldi.txt)
* :star2: [CJX's Annoyance List (Vivaldi内置) ](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt)
* ~~[Peter Lowe's Ad and tracking server list](https://pgl.yoyo.org/adservers/serverlist.php?hostformat=adblockplus&showintro=1&mimetype=plaintext)~~
* [I don't care about cookies `在Vivaldi中使用需要打开此链接保存为txt文件进行本地导入`](https://www.i-dont-care-about-cookies.eu/abp/)
* :star2: [乘风广告过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt)
* :star2: [乘风视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt)
* [乘风小众视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt)
* [:star2: runningcheese's Adblock_Popup](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt)
* :star2: [runningcheese's Adblock_Watermark](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt)
* ~~[oisd big](https://big.oisd.nl/)~~
* ~~[hagezi pro](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt)~~
* [hagezi pro mini](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt)
* [oisd nsfw](https://nsfw.oisd.nl/)
* :star2: [cxfl-adblockplus自定义规则  `不能订阅，需打开全选复制添加到自定义过滤列表中 (Vivaldi不能用)`](https://raw.githubusercontent.com/fenglingback/cxfllist/main/cxfl-adblockplus.txt)


$${👇}$$

$${👇}$$

$${👇}$$


## uBlock Origin `ubo`

### PC 端 and 移动端


> [!IMPORTANT]  
> :star2: 为 `必用规则` ，强烈推荐使用。如果使用ubo，`取消所有初始订阅规则` 的同时，保留 `内置` 栏目规则


### 选择你需要的规则集，然后右键复制它的链接地址，导入:

1. :star2: [EasyList](https://easylist-downloads.adblockplus.org/easylist.txt)
2. :star2: [EasyList China](https://easylist-downloads.adblockplus.org/easylistchina.txt)
3. :star2: [EasyPrivacy](https://easylist-downloads.adblockplus.org/easyprivacy.txt)
4. :star2: [DuckDuckGo Tracker Radar](https://downloads.vivaldi.com/ddg/tds-v2-current.json)
5. :star2: [Adblock Warning Removal List](https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt)
6. [Malicious URL blocklist `(ubo内置的是精简版，取消之后添加这个)`](https://malware-filter.gitlab.io/malware-filter/urlhaus-filter.txt)
7. :star2: [CJX's Annoyance List](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt)
8. :star2: [CJX's ublock list](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt)
9. ~~[Peter Lowe’s Ad and tracking server list `(ubo内置也有)`](https://pgl.yoyo.org/adservers/serverlist.php?showintro=1&mimetype=plaintext)~~
10. :star2: [乘风广告过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt)
11. :star2: [乘风视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt)
12. [乘风小众视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt)
13. :star2: [Web Annoyances Ultralist](https://raw.githubusercontent.com/yourduskquibbles/webannoyances/master/ultralist.txt)
14. [I don't care about cookies](https://www.i-dont-care-about-cookies.eu/abp/)
15. [:star2: runningcheese's Adblock_Popup](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt)
16. :star2: [runningcheese's Adblock_Watermark](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt)
17. ~~[oisd big](https://big.oisd.nl/)~~
18. ~~[hagezi pro](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt)~~
19. [hagezi pro mini](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt)
20. [oisd nsfw](https://nsfw.oisd.nl/)
21. :star2: [cxfl's ublock list](https://raw.githubusercontent.com/fenglingback/cxfllist/main/cxfl-ublock.txt)


### 一键复制必用规则集，导入：

```
https://easylist-downloads.adblockplus.org/easylist.txt
https://easylist-downloads.adblockplus.org/easylistchina.txt
https://easylist-downloads.adblockplus.org/easyprivacy.txt
https://downloads.vivaldi.com/ddg/tds-v2-current.json
https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt
https://raw.githubusercontent.com/yourduskquibbles/webannoyances/master/ultralist.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt
https://raw.githubusercontent.com/fenglingback/cxfllist/main/cxfl-ublock.txt
```





### 或者一键复制全部，导入：

```
https://easylist-downloads.adblockplus.org/easylist.txt
https://easylist-downloads.adblockplus.org/easylistchina.txt
https://easylist-downloads.adblockplus.org/easyprivacy.txt
https://downloads.vivaldi.com/ddg/tds-v2-current.json
https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt
https://malware-filter.gitlab.io/malware-filter/urlhaus-filter.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt
https://raw.githubusercontent.com/yourduskquibbles/webannoyances/master/ultralist.txt
https://www.i-dont-care-about-cookies.eu/abp/
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt
https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt
https://nsfw.oisd.nl/
https://raw.githubusercontent.com/fenglingback/cxfllist/main/cxfl-ublock.txt
```
