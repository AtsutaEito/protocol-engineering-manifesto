---
layout: default
title: Protocol Engineering Manifesto | 公式主張・実証ゲートウェイ
description: AIの進化の副作用に対抗し、有機的思考の人間が主権を死守するための「プロトコルエンジニアリング」に関する公式宣言（マニフェスト）および技術マニュアルの集約ハブ。
---

<blockquote class="pe-definition" lang="ja">
<strong>本ゲートウェイの位置づけ：</strong>
AIの急速な進化とその副作用（要約のサボり、追従による思考の平坦化）に直面する現代において、有機的な人間が知的主権（指揮権）を死守するための思想マニフェスト、および具体的な構造化設計（AIO仕様・プラットフォーム配置）を定義した公式マニュアルの公開アーカイブ。
</blockquote>

<p>当サイトは、プロトコルエンジニアリング（AIE4.1）に基づき、人工知能と人間の理想的な協働関係を提示する公式宣言（マニフェスト）、および実務用マニュアルを永続的に蓄積・公開するアーカイブです。</p>

<p>本流ゲートウェイ： <strong><a href="https://atsutaeito.github.io/protocol-engineering/" target="_blank">Protocol Engineering Canonical Gateway</a></strong></p>

---

<h2 class="pe-section-title">公式マニフェスト & 技術マニュアル一覧</h2>
<div class="pe-grid">

{% for post in site.posts %}
<a href="{{ post.url | relative_url }}" class="pe-card">
<div>
<h3>{{ post.title }}</h3>
<p>{{ post.description | default: post.excerpt | strip_html | truncate: 150 }}</p>
</div>
<span class="pe-tag">{{ post.date | date: "%Y-%m-%d" }}</span>
</a>
{% endfor %}

</div>
