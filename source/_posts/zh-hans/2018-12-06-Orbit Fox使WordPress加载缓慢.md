---
title: Orbit Fox使WordPress加载缓慢
date: 2018-12-06 12:00:00
tags:
    - zh-hans
    - dev
    - wordpress
categories:
    - 中文文章
lang: zh-hans
---

## Orbit Fox使WordPress加载缓慢

### 情景再现

最近打开网站速度超级慢，没想通原因，直到我打开chrome的控制台发现这样一则元素占用了数秒的网页加载时间：

![chrome](https://img.brightgames.top/20181206203131.png)

```html
https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css?ver=2.7.0
```

![font-awesome](https://img.brightgames.top/20181206202513.png)

用排除法找到了orbit fox，停用orbit fox后不再出现该引用，网页速度恢复正常。