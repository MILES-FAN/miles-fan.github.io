---
title: Orbit FoxによるWordPressのロード遅延
date: 2018-12-06 12:00:00
tags:
    - ja
    - dev
    - wordpress
categories:
    - 日本語記事
lang: ja
---

## Orbit FoxによるWordPressのロード遅延

### 再現

最近、ウェブサイトの開く速度が極端に遅く、原因が分からなかった。しかし、Chromeのコンソールを開いたところ、以下の要素が数秒間のページ読み込み時間を占めていることが判明した：

![chrome](https://img.brightgames.top/20181206203131.png)

```html
https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css?ver=2.7.0
```

![font-awesome](https://img.brightgames.top/20181206202513.png)

排除法を用いて、orbit foxが原因であることを突き止めた。orbit foxを停止すると、この参照がなくなり、ウェブページの速度が通常に戻った。

