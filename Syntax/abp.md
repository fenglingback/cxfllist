# ABP的一些高级语法（摘自 [ABP官方文档](https://help.adblockplus.org/hc/en-us/articles/360062733293-How-to-write-filters#elemhide-emulation)）

## 属性选择器

Some advertisers don't make it easy for you — their text advertisements have neither an ID nor a class attribute. You can use other attributes to hide those, for example `##table[width="80%"]` hides tables with a width attribute set to 80%. If you don't want to specify the full value of the attribute, `##div[title*="adv"]` hides all `div` elements with a title attribute containing the string `"adv"`. You can also check the beginning and the end of an attribute, for example `##div[title^="adv"][title$="ert"]` hides div elements with title starting with `"adv"` and ending with `"ert"`. As you see, you can also use multiple conditions — `table[width="80%"][bgcolor="white"]` matches tables with a width attribute set to 80% and `bgcolor` attribute set to white. 




## 扩展 CSS 选择器（特定于 Adblock Plus）(`#?#`)

Sometimes the standard CSS selectors aren't powerful enough to hide an advertisement. For those cases, we’ve added some new selectors, namely:  

*   `:-abp-has()`
*   `:-abp-contains()`
*   `:-abp-properties()` (Adblock Plus 1.13.3 or higher for Chrome and Opera is required.)  

When writing an element hiding filter that makes use of these extended selectors, you must use the `#?#` syntax, e.g. `example.com#?#selector`. It's important to note, however, that doing so creates a performance impact, so do so sparingly and make sure those filters are specific to as few domains and elements as possible.  

### `:-abp-has()`

The `:-abp-has(selector)` selector selects elements based on their content. For example, `:-abp-has(> div > a.advertiser)` selects elements that contain, as a direct descendant, a `<div>` that contains an `<a>` with the class advertiser. The inner selector can be relative to the element scope and can use any pseudo-selectors, including `:-abp-has()`, to determine whether the selection will occur.  


> [!TIP]  
>
> The filter `example.com#?#:-abp-has(.sponsored)` hides all pages because the class is also contained somewhere in the `<body>`. To avoid hiding all pages, simply add `>` or `+`.  



> **Example** 
> 
> If you add the filter `eyeo.com#?#:-abp-has(code)` on https://help.eyeo.com/en/adblockplus/how-to-write-filters and hard refresh, everything is blocked. This is because the `<body>` contains `<code>`. To fix this, change the filter to `eyeo.com#?#:-abp-has(> code)`. After a hard refresh, only parent elements of `<code>` are blocked.  



### `:-abp-contains()`

The `:-abp-contains(text)` selector selects elements based on their text content. For example, `div.sidebar > span:-abp-contains(Advertisement)` selects the elements within a `<div>`, with a class of sidebar that contains the word "Advertisement". In practice, you'd want to combine this with a `:-abp-has()` to select the outer container (something like `div.sidebar > div:-abp-has(span:-abp-contains(Advertisement))` to select the container that contains an advertisement label).  


> **Example**  
>
> If you add the filter `eyeo.com#?#:-abp-contains(filters)` on https://help.eyeo.com/en/adblockplus/how-to-write-filters and hard refresh, nothing changes. If you change the filter to `eyeo.com#?#div:-abp-contains(filters)` and hard refresh, `div.outer` (which contains the middle section of the page) is blocked because somewhere within the `<body>` is the word "filters". To fix this, change the filter to `eyeo.com#?#.article-heading:-abp-contains(filters)`. After a hard refresh, only the headings of each article are hidden.  


### `:-abp-properties()`

The `:-abp-properties(properties)` selector selects elements based on stylesheet properties. For example, `:-abp-properties(width:300px;height:250px;)` selects elements that have a corresponding CSS rule in a stylesheet which sets the width and height to the values 300px and 250px, respectively. Property names are matched case-insensitively. Furthermore, wildcards can be used so that `:-abp-properties(width:*px;height:250px;)` matches any width specified in pixels and a height of 250 pixels.  


You can also use [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) by surrounding the properties expression with "/". For example, `:-abp-properties(/width:30[2-8]px;height:250px;/)` matches widths between 302 and 308 pixels and a height of 250 pixels.  


> [!TIP]  
>
> The [old syntax](https://adblockplus.org/development-builds/new-css-property-filter-syntax) for the CSS property filters is deprecated and will be automatically converted to the new format. The syntax to select the style properties remains the same.  

> [!TIP]  
>
> When using the `background-color property`, use the rgb() notation. For example, instead of `:-abp-properties(background-color: #3D9C4F;)`, use `:-abp-properties(background-color: rgb(61, 156, 79))`.  

> **Example**  
>
> `[-abp-properties='width:300px;height:250px;']` is converted to `:-abp-properties(width:300px;height:250px;)`. `:-abp-properties()` also selects elements using the style properties found in their pseudo-elements, like ::before and ::after. For example, `:-abp-properties(content:'Advertisement')` matches elements where the string `Advertisement` is found either `::before` or `::after` pseudo element.  


## 例外规则（`#@#`）

Exception rules can deactivate existing rules on particular domains. These are mostly useful to filter subscription authors who are extending another filter subscription that they cannot change. For example, the rule `##.textad` can be deactivated on example.com using the exception rule `example.com#@#.textad`. The combination of these two rules has exactly the same effect as the single rule `~example.com##.textad`. It’s recommended that you use exception rules only when you cannot change an overly general element hiding rule. In all other cases, limiting this rule to the necessary domains is preferable. These exceptions will be applied to [extended CSS selector rules](#elemhide-emulation) as well.  
例外规则可以停用特定域上的现有规则。这些对于过滤订阅作者来说非常有用，这些作者正在扩展他们无法更改的另一个过滤器订阅。例如，可以使用例外规则 `example.com#@#.textad` 在 example.com 上停用规则 `##.textad` 。这两个规则的组合与单个规则 `~example.com##.textad` 具有完全相同的效果。建议您仅在无法更改过于通用的元素隐藏规则时才使用例外规则。在所有其他情况下，最好将此规则限制到必要的域。这些例外也将应用于扩展 CSS 选择器规则。

Example  
例子

If you add the filter `##aside.info` on https://help.eyeo.com/en/adblockplus/how-to-write-filters, `eyeo.com#@#aside` will not allowlist anything. If you add the filter `##aside`, `eyeo.com#@#aside.info` will not allowlist anything. The filters must be exactly the same, i.e. `eyeo.com#@#aside.info`.  
如果您在 https://help.eyeo.com/en/adblockplus/how-to-write-filters 上添加过滤器 `##aside.info` ， `eyeo.com#@#aside` 将不会将任何内容列入允许名单。如果您添加过滤器 `##aside` ， `eyeo.com#@#aside.info` 将不会将任何内容列入白名单。过滤器必须完全相同，即 `eyeo.com#@#aside.info` 。



## 片段过滤器（`#$#`）

Snippet filters allow running specialized code snippets (written in JavaScript) on pages with the list of specified domains. The body of the filter contain the snippet commands to run.  

Please refer to the [snippet filters tutorial](https://help.adblockplus.org/hc/en-us/articles/1500002338501) for a more detailled guide on how to write snippet filters.  

> [!TIP]
>
> For security reasons, snippet filters can only be added to a user's custom filters list or in the [ABP Anti-Circumvention Filter List](https://gitlab.com/eyeo/anti-cv/abp-filters-anti-cv), the latter being vetted and reviewed.  

