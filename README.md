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
> ~~`DuckDuckGo Tracker Radar`：<i>也是一个反跟踪规则，精简但高效，甚至能屏蔽一些网站的指纹识别</i>~~  
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
> `yoko`
> `CJX's ublock list`：<i>对 easylist + easylistchina + easyprivacy + cjx's Annoyance List的补充</i>  
> `cxfl's ublock list`：本人维护，对以上所有规则集的补充，主要为屏蔽网页烦人元素，请在添加完以上主流订阅规则后再添加  
> `cxfl-adblockplus自定义规则`：本人维护，等同于 <kbd>cjx补充</kbd> + <kbd>cxfl's ublock list</kbd>

> [!WARNING]  
> `Peter Lowe's Ad and tracking server list`、`oisd big`、`DuckDuckGo Tracker Radar` 已经被淘汰了，因为 `hagezi pro` 更强更高效，详情请看👉[①](https://github.com/hagezi/dns-blocklists/issues/2346#:~:text=There%20is%20also%20Peter%20Lowe%27s%20Ad%20and%20tracking%20list%20if%20someone%20really%20only%20wants%20to%20block%20ads%20and%20tracking.) [②](https://www.reddit.com/r/nextdns/comments/192mdeh/why_should_i_use_hagezi_in_place_of_oisd/)👈。然后，它的mini版本 `hagezi pro mini` 更适合在浏览器上使用。不过我本人用 `hagezi pro++` :joy:

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


$${现在，请选择你的过滤器，我只推荐uBlock Origin(ubo)}$$

$$ubo用户请继续往下看$$

$${↙其他用户请点击↘}$$


<table align="center">
    <tr>
        <td><a href="">Adblock Plus</td>
        <td><a href="">Vivaldi</td>
    </tr>
</table>




$${👇}$$

$${👇}$$

$${👇}$$



## uBlock Origin `ubo` （PC 端 and 移动端）



### 基础版

> [!IMPORTANT]  
> 这个版本适合 `只浏览国内网站`，或者 `很少时间` 浏览国外网站，或者 `对跟踪隐私方面没啥感觉` 的宝宝，已然非常够用了！

$${保留\ {\color{lightgreen}
初始状态的默认规则} + 导入\ {\color{lightgreen}国内必备规则：}}$$

> [!TIP]  
> ![](https://raw.githubusercontent.com/fenglingback/cxfllist/main/images/%E5%9F%BA%E7%A1%80%E7%89%88.png)




#### 国内必备规则一键复制导入：

```
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt
https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt
https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt
https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt
https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt
```




#### 你也可以选择其中的一些，右键复制链接地址，导入：

* [CJX's Annoyance List](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt)
* [CJX's ublock list](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt)
* [乘风广告过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt)
* [乘风视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt)
* [乘风小众视频过滤规则](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt)
* [runningcheese's Adblock_Popup](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt)
* [runningcheese's Adblock_Watermark](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt)
* [cxfl's ublock list](https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt)









$${👇}$$

$${👇}$$

$${👇}$$


### 增强版


* :star2: [Adblock Warning Removal List](https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt)
6. [Malicious URL blocklist `(ubo内置的是精简版，取消之后添加这个)`](https://malware-filter.gitlab.io/malware-filter/urlhaus-filter.txt)

9. ~~[Peter Lowe’s Ad and tracking server list `(ubo内置也有)`](https://pgl.yoyo.org/adservers/serverlist.php?showintro=1&mimetype=plaintext)~~

13. :star2: [Web Annoyances Ultralist](https://raw.githubusercontent.com/yourduskquibbles/webannoyances/master/ultralist.txt)
14. [I don't care about cookies](https://www.i-dont-care-about-cookies.eu/abp/)

17. ~~[oisd big](https://big.oisd.nl/)~~
18. ~~[hagezi pro](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt)~~
19. [hagezi pro mini](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt)
20. [oisd nsfw](https://nsfw.oisd.nl/)
21. [yokoffing's Annoyance List](https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt)








### 或者一键复制全部，导入：

```
https://easylist-downloads.adblockplus.org/easylist.txt
https://easylist-downloads.adblockplus.org/easylistchina.txt
https://easylist-downloads.adblockplus.org/easyprivacy.txt
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
https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt
https://raw.githubusercontent.com/fenglingback/cxfllist/main/cxfl-ublock.txt
```
