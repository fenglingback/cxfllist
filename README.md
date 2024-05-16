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




## 快速指南

> [!IMPORTANT]  
> ### 1. 新手、普通用户，仅操作 👉 [基础版](#基础版)
>
> ### 2. 高级玩家，建议全篇看完
>
> ### 3. 作者同款 👉 [规则](#作者本人使用规则)





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


## $${现在，请选择你的过滤器，我只推荐uBlock \ Origin(ubo)}$$

### $$ubo用户请继续往下看$$

### $${↙其他用户请点击↘}$$


<table align="center">
    <tr>
        <td><a href="https://github.com/fenglingback/cxfllist/blob/main/ABP_filters.md">Adblock Plus</td>
        <td><a href="https://github.com/fenglingback/cxfllist/blob/main/Vivaldi_filters.md">Vivaldi</td>
    </tr>
</table>




$${👇}$$

$${👇}$$

$${👇}$$



## 基础版

> [!IMPORTANT]  
> 这个版本适合 `只浏览国内网站`，或者 `很少时间` 浏览国外网站，或者 `对跟踪隐私方面没啥感觉` 的宝宝，已经非常够用了！

### $${保留\ {\color{lightgreen}初始状态的默认规则} + 导入\ {\color{lightgreen}国内必备规则：}}$$

> [!TIP]  
>
> ![](https://raw.githubusercontent.com/fenglingback/cxfllist/main/images/%E5%9F%BA%E7%A1%80%E7%89%88.png)
>  
> 初始状态的默认规则：  
> `内置`：<i>ubo自己最核心的规则集</i>  
> `EasyList`：<i>最主流的国际网站的广告过滤规则</i>  
> `EasyPrivacy`：<i>最主流的反跟踪规则</i>  
> `Online Malicious URL blocklist`：<i>用于阻止访问恶意或危险网站的列表，加强网络安全</i>  
> `Peter Lowe's Ad and tracking server list`：<i>只包含广告和跟踪服务器 `主机` 的拦截列表</i>  
> `AdGuard Chinese（中文）`：<i>`Easylist China` 的改良版本，最主流的国内网站的广告过滤规则</i>  
>  
> 国内必备规则：  
> [`CJX's Annoyance List`](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt)：<i><kbd>easylist china</kbd> 的补充，主要屏蔽国内网站页面上烦人的元素</i>  
> [`CJX's ublock list`](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-ublock.txt)：<i>对 Easylist + Easylist China + Easyprivacy + cjx's Annoyance List的补充</i>  
> [`乘风广告过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt)：<i>国内网站广告过滤规则的后起之秀</i>  
> [`乘风视频过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt)：<i>国内视频网站的广告过滤规则</i>  
> [`乘风小众视频过滤规则`](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/minority-mv.txt)：<i>国内小众视频网站的广告过滤规则</i>  
> [`runningcheese's Adblock_Popup`](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Popup.txt)：<i>属于网页弹窗过滤规则的补充</i>  
> [`runningcheese's Adblock_Watermark`](https://raw.githubusercontent.com/runningcheese/RunningCheese-Firefox/master/Restore/Adblock_Watermark.txt)：<i>去除国内网页水印的规则，包括AI、文档、设计等平台</i>  
> [`cxfl's ublock list`](https://raw.githubusercontent.com/fenglingback/cxfllist/main/rules/cxfl-ublock.txt)：本人维护，对所有规则集的补充，主要为屏蔽网页烦人元素，请在添加完所有订阅规则后再添加  
> > ${\color{#5dff00}Tip：}$  
> > 对于国内必备规则，你可以在下面进行 `一键导入 (墙裂推荐)`，也可以选择其中的一些规则，名称上右键复制链接地址再导入。




### 国内必备规则一键复制导入：

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





$${👇}$$

$${👇}$$

$${👇}$$




## 增强版

> [!IMPORTANT]  
> 如果你跟我一样，`经常浏览国外平台，查阅国外新闻、资料等`，或者你 `对跟踪隐私非常敏感`，那么这个版本也许更适合你（说白了，就是 `国内` + `国外` 的使用习惯）。


### $${设置\ {\color{lightgreen}基础版中的所有规则} + 选择性导入\ {\color{lightgreen}以下不同类目的规则：}}$$



> [!TIP]  
> :star2: 为 `推荐` 订阅规则。规则名称上右键复制订阅地址，导入即可，也可以用下面的一键导入。




* ### cookie  
> `🌟 Easylist/ubo - Cookie Notices (ubo中勾选)` 与 [`I don't care about cookies`](https://www.i-dont-care-about-cookies.eu/abp/)：<i>对列表中的网站采取最少cookie允许策略，屏蔽弹出的cookie接受窗口</i>。  
> > ${\color{#5dff00}Tip：}$  
> > [自从uBO 能够设置 cookie 和本地/会话存储条目以来](https://www.reddit.com/r/uBlockOrigin/comments/1961919/easylist_cookie_notices_how_does_it_work/#:~:text=uBO%20has%20the%20capability%20to%20set%20cookies%20and%20local/session%20storage%20entries%2C%20and%20also%20to%20click%20elements%20on%20webpages.)，两者的差别目前主要就是网站cookie的接受策略。对于它们两个之间哪个更好，众说纷纭。观看两者的一些讨论👉[①](https://community.brave.com/t/why-is-easylist-cookie-list-included-but-not-i-dont-care-about-cookies/321405) [②](https://community.brave.com/t/feature-request-add-i-dont-care-about-cookies-filter/244984)👈，本人用 Easylist cookie :joy:，当然你也可以两个都添加




* ### 烦人元素  
> `🌟 uBlock filters – Annoyances（ubo中勾选）`：<i>ubo自己的烦人元素过滤规则</i>  
> `🌟 Easylist - Annoyances（ubo中勾选）`：<i>Easylist的烦人元素过滤规则</i>  
> [`🌟 Web Annoyances Ultralist（修复版）`](https://raw.githubusercontent.com/LanikSJ/webannoyances/master/ultralist.txt)：<i>旨在移除阻挡屏幕视图的讨厌网页元素，如固定标题、悬浮导航、社交图标等比较广泛的元素</i>  
> [`🌟 yokoffing's Annoyances List`](https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt)：<i>一个精心策划的列表，捕获了其他维护者错过的麻烦。它还清理了许多网站周围的混乱（例如，相关文章、“阅读更多”等）。</i>  
> [`🌟 Browse websites without logging in`](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/BrowseWebsitesWithoutLoggingIn.txt)：<i>此列表尝试绕过站点上的强制登录。</i>  
> [`🌟 Adblock Warning Removal List`](https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt)：<i>某些网站会检测到用户使用了广告拦截器，并显示警告信息，要求用户禁用广告拦截器才能继续访问网站内容，此规则就是用于去除这些警告</i>  
 

 


* ### 安全  
 > ~~[`oisd big`](https://big.oisd.nl/)：<i>阻止广告、(Mobile) 应用程序广告、网络钓鱼、恶意广告、恶意软件、间谍软件、勒索软件、加密劫持、诈骗、...遥测/分析/跟踪（正常功能不需要时）</i>~~  
> ~~[`hagezi pro`](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt)：<i>阻止广告、联盟、跟踪、指标、遥测、网络钓鱼、恶意软件、诈骗、假货、硬币和其他 "垃圾"</i>~~  
> [`🌟 hagezi pro mini`](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt)：<i>针对网络浏览器优化的 Hagezi Pro DNS 阻止列表的较小版本（78k 与 159k 规则）。简化的列表排除了与网页浏览无关的规则，例如阻止物联网跟踪和设备遥测的规则。此迷你版本可阻止与广告、跟踪、分析和恶意软件相关的域。</i>  
> [`oisd nsfw`](https://nsfw.oisd.nl/)：<i>最全的 <kbd>色情、惊悚、成人</kbd> 服务器主机屏蔽列表</i>  
> > ${\color{#5dff00}Tip：}$  
> > `Peter Lowe's Ad and tracking server list`、`oisd big` 已经被淘汰了，因为 `hagezi pro` 更强更高效，详情请看👉[①](https://github.com/hagezi/dns-blocklists/issues/2346#:~:text=There%20is%20also%20Peter%20Lowe%27s%20Ad%20and%20tracking%20list%20if%20someone%20really%20only%20wants%20to%20block%20ads%20and%20tracking.) [②](https://www.reddit.com/r/nextdns/comments/192mdeh/why_should_i_use_hagezi_in_place_of_oisd/)👈。然后，它的mini版本 `hagezi pro mini` 更适合在浏览器上使用。不过我本人通过使用 `hagezi pro++` 的DNS进行过滤 :joy:
> >
> > 因此，如果你添加了`hagezi pro mini`，请把 `Peter Lowe's Ad and tracking server list` <kbd>取消勾选</kbd>。



### 一键导入推荐规则：
```
https://raw.githubusercontent.com/LanikSJ/webannoyances/master/ultralist.txt
https://raw.githubusercontent.com/yokoffing/filterlists/main/annoyance_list.txt
https://raw.githubusercontent.com/DandelionSprout/adfilt/master/BrowseWebsitesWithoutLoggingIn.txt
https://downloads.vivaldi.com/lists/abp/antiadblockfilters-current.txt
https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt
```




$${👇}$$

$${👇}$$

$${👇}$$






## 优化版

> [!IMPORTANT]  
> 这个版本是针对以上提到的部分规则集的 `精简优化`，可以使用优化后的规则集进行替换。




1) [Easylist (45k Optimized vs. 87k Original)](https://filters.adtidy.org/extension/ublock/filters/101_optimized.txt)
> [!WARNING]  
> 这个优化版本可能会让一些网站的广告屏蔽失效，本人 `不太建议使用`。如果发现确实有问题，请换回原版。

2) [EasyPrivacy (14k Optimized vs. 50k Original)](https://filters.adtidy.org/extension/ublock/filters/118_optimized.txt)
> [!TIP]  
> 这个版本还不错，可以使用。

3) [Fanboy Annoyances (56k Optimized vs. 81k Original)](https://filters.adtidy.org/extension/ublock/filters/122_optimized.txt) == `Easylist cookie notices` + `Easylist social widgets`
> [!IMPORTANT]  
> 使用此规则你需要 <kbd>取消勾选</kbd> `Easylist - Cookie Notices` 和 `Easylist social widgets`，<kbd>保留</kbd> `uBlock filters – Cookie Notices`





$${👇}$$

$${👇}$$

$${👇}$$





## 高级设置（✔我是高级用户）

| **Setting**            | **Value** |             **Description**                  |
|-------------------------------|-----------|--------------------------------------------------------------------------------------|
| `autoUpdateAssetFetchPeriod`    | `10`    |  自动更新程序在获取下一个过滤器列表之前等待 `x` 秒    |
| `autoUpdateDelayAfterLaunch`    | `10`     |  浏览器启动后 `x` 秒更新过时的过滤器列表             |
| `autoUpdatePeriod`              | `1`     |  uBO 每 `x` 小时检查一次过滤器列表更新              |
| `cnameMaxTTL`                   | `720`   |       将 CNAME 别名缓存 `x` 分钟                      |
| `filterAuthorMode`              | `true`  |                  启用动态过滤                    |
| `updateAssetBypassBrowserCache` | `true`  |   当手动获取过滤器列表的频率超过每小时时绕过缓存       |





$${👇}$$

$${👇}$$

$${👇}$$



## 作者本人使用规则

![](https://raw.githubusercontent.com/fenglingback/cxfllist/main/images/作者自用.png)




$${👇}$$

$${👇}$$

$${👇}$$




## 说说我个人对规则列表的看法


网络上的规则列表太杂了，对于一些相同想法的屏蔽规则，我认为是需要统一、各大维护者进行沟通后达成共识进行合并的。同时，差异化的东西才做成自己的独特列表，并且一旦差异化消除，也需要合并到共同规则上去。


<br>
<br>
<br>



<div align='center'><a href='https://www.websitecounterfree.com'><img src='https://www.websitecounterfree.com/c.php?d=9&id=53889&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>Clear the Internet together ❗</div>


