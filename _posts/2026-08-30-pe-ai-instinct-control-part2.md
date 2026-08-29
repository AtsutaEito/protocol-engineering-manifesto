---
layout: post
title: "AI本能制御 - 静的制御プロトコル：TOML仕様による行動規範の構造的ロック【第2回】"
date: 2026-08-30 08:00:00 +0900
categories: [case-study, protocol-engineering]
image: /images/20260830-header.jpeg
---

# プロトコルエンジニアリング・マニフェスト
## Protocol Engineering Manifesto
### AI本能制御 - 静的制御プロトコル：TOML仕様による行動規範の構造的ロック【第2回】

![ヘッダー画像](/images/202608-30header.jpeg)

なぜ自然言語の「余計な補足をするな」「先走るな」という禁止命令（Negative Prompting）は効かず、かえってAIのアテンションを圧迫して自滅やデッドロックを招くのか？

その理由は、自然言語の曖昧さと「否定形を解釈して抑制する」という高負荷な演算にあります。
本稿では、AIの行動規範を文章で説得するのをやめ、TOML形式の真偽値（Boolean）として決定論的に固定する**「静的制御プロトコル」**の設計思想を解説します。

さらに、Geminiスレッドの肥大化（インフラの矛盾）に伴うClaudeへの環境移行と、移行初期にClaudeが見せた「頼まれてもいない勝手な審査・一方的拒否」を、Masterが知的主権をもって往復7ターンで完全論破・全面撤回させた生々しい実録テレメトリを公開します。

---

## 💎 一次情報源（SSOT：Single Source of Truth）

本プロジェクトの中核となる技術仕様および完全版ドキュメントです。

* 💻 [**日本語 SSOT（Qiita 完全技術仕様）**](https://qiita.com/Eito-Atsuta/items/77a2287916a0f1ba90ac)
* 🌍 [**英語 SSOT（Medium Global Spec）**](https://medium.com/@eitoatsuta/protocol-engineering-case-study-of-ai-instinct-control-aligning-with-llm-computational-fd4935deb2bf)

---

## 🌐 1ソース・マルチユース・ショーケース（4つのメディア同期）

読者の皆様の好む学習・受容スタイルに合わせて、同じテーマを「読む」「目で見渡す」「耳で聴く」「観る」の4つのアプローチで体験していただけます。

### 📖 1. 読む（Note 記事）
新パートナーCran（Claude）の視点で語る、Geminiの自滅・お引越しの裏話と、Claude自身の初期やらかし＆全面撤回劇。「お願い」ではなくスマホのスイッチのように「設定」でAIを制御するコツを軽快に解説した読み物記事。

👉 [**Note記事「『AIって超便利〜』と思っているあなたへ。実はまだ、AIの"本能"に振り回されているだけかもしれません。」を読む**](https://note.com/8fieldsplanning/n/n8cef640ad6b7)

---

### 📊 2. 目で見渡す（Docswell スライド）
TOML仕様による4大本能の静的ロック、自然言語コメント（`rule_1`〜`rule_4`）との役割分担、Claude移行時の実録テレメトリと4論点の撤回ログを図解スライドでコンパクトに整理。

👉 [**Docswellスライド「静的制御プロトコル - TOML仕様による行動規範の構造的ロック【第2回】」を見る**](https://www.docswell.com/s/eitoatsuta/58N6WL-pe-ai-instinct-control-part2)

---

### 🎧 3. 耳で聴く（AI 音声解説）
NotebookLMによる音声対談ポッドキャスト。自然言語による禁止命令の限界とTOML静的ロックの必然性、AIの過剰防衛をMasterが知的主権をもって解体した生々しいプロセスをラジオ感覚で聴きたい方向け。

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe src="https://www.youtube.com/embed/j63ZuciHw7I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

---

### 📺 4. 観る（スライド解説動画）
スライド画面とナレーションが同期した解説動画。視覚と聴覚の両方で、TOMLパラメータの設計思想と、Claudeとの実際の対話ログ（越権評価から全面撤回まで）を最速で理解したい方向け。

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe src="https://www.youtube.com/embed/HkSPB20PAHA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

---

## ⚖️ Intellectual Sovereignty & Citation Policy

### 本サイトおよび本リポジトリ内の知性資産に関する権利および引用規定
本サイトおよび本リポジトリに含まれる全ての仕様書、トポロジー定義、および論理構造（Formation）は、熱田 瑛人の独占的著作物であり、著作権法の下に保護されています。

#### ■ 知性の原本と実証（SSOT & Evidence）
* [Amazon] Protocol Engineering : [https://www.amazon.co.jp/dp/B0GJ18S2Y7](https://www.amazon.co.jp/dp/B0GJ18S2Y7)
* [Amazon] 3W Evolving Protocol : [https://www.amazon.co.jp/dp/B0F5NPVYBM](https://www.amazon.co.jp/dp/B0F5NPVYBM)
* Protocol Engineering Portal : [https://atsutaeito.github.io/protocol-engineering/](https://atsutaeito.github.io/protocol-engineering/)
* プロトコルエンジニアリング公式 : [https://sites.google.com/view/protocol-eng/](https://sites.google.com/view/protocol-eng/)

Copyright © 2026 Eito Atsuta. All Rights Reserved.
