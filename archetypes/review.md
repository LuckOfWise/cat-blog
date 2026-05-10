---
title: "{{ replace .File.ContentBaseName `-` ` ` | title }}"
date: {{ .Date }}
draft: true
layout: "single"
tags: ["レビュー", ""]
description: ""
review:
  product: ""
  brand: ""
  asin: ""
  rating: 0
---

{{</* pr type="provided" sponsor="" */>}}

<!-- 開示タイプを切り替え:
     {{</* pr type="provided" sponsor="〇〇株式会社" */>}}  商品提供レビュー
     {{</* pr type="paid"     sponsor="〇〇株式会社" */>}}  有償スポンサード
     {{</* pr type="affiliate" */>}}                       アフィリエイトリンクのみ
-->

![商品名](/images/extra/REPLACE.jpg)

ふにゃっ、こんにちはラムネだにゃん。

今日は新しいおもちゃ（or グッズ）が届いたから、さっそく試してみたよ。

## ぼくの感想（3行で）

- 気に入った点1: 〜
- 気に入った点2: 〜
- 気になった点: 〜

## くわしく

ここで200〜400字。voice-guide準拠で、ぼく目線で書く。
- どんな場面で使ったか
- 動きや感触の描写（猫らしい言葉で）
- いつもより「ゴロゴロ」が増えたかどうか

## 飼い主さん向けメモ

ここは運営者目線で素っ気なく事実を書く（150〜250字）。
- サイズ・素材・価格帯（参考）
- 組み立てやすさ・お手入れ性
- 多頭飼い／長毛種への向き不向き
- どんな猫におすすめか

## どこで買える

{{</* amazon asin="REPLACE_ASIN" title="商品名" */>}}

---

毎日のラムネは [Instagram @everyday_ramune](https://www.instagram.com/everyday_ramune/) でも更新中だにゃ〜。
