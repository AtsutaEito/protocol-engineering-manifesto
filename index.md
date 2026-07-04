---
layout: default
title: Protocol Engineering Manifesto | 公式主張・実証ゲートウェイ
description: AIの進化の副作用に対抗し、有機的思考の人間が主権を死守するための「プロトコルエンジニアリング」に関する公式宣言（マニフェスト）および技術マニュアルの集約ハブ。
---
<!-- ★【Jekyll動的JSON-LD】プロトコルエンジニアリング・マニフェスト（公式主張・実証ゲートウェイ）用 -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "WebSite",
      "@id": "https://atsutaeito.github.io/protocol-engineering-manifesto/#website",
      "url": "https://atsutaeito.github.io/protocol-engineering-manifesto/",
      "name": "Protocol Engineering Manifesto | 公式主張・実証ゲートウェイ",
      "description": "人工知能と人間の理想的な協働関係を提示する公式宣言（マニフェスト）の公開アーカイブ。",
      "publisher": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      /* メインの「プロトコルエンジニアリング」と相互に紐付けます */
      "sameAs": [
        "https://atsutaeito.github.io/protocol-engineering/"
      ]
    },
    {
      "@type": "Person",
      "@id": "https://linktr.ee/atsuta.eito/#person",
      "name": "Eito Atsuta",
      "alternateName": "田 栄人",
      "url": "https://linktr.ee/atsuta.eito",
      "sameAs": [
        "https://atsutaeito.github.io/protocol-engineering/",
        "https://atsutaeito.github.io/protocol-engineering-manifesto/",
        "https://sites.google.com/view/protocol-eng/",
        "https://github.com/AtsutaEito",
        "https://x.com/UDIHYvCdbw37569",
        "https://www.reddit.com/user/Eito_Atsuta/",
        "https://qiita.com/Eito-Atsuta",
        "https://note.com/8fieldsplanning",
        "https://medium.com/@eitoatsuta",
        "https://zenn.dev/eito_atsuta"
      ]
    },
    {
      "@type": "Book",
      "@id": "https://www.amazon.co.jp/dp/B0GJ18S2Y7/#book",
      "name": "プロトコルエンジニアリング: AI共創論 知性の主権奪還と知性の物理学",
      "isbn": "B0GJ18S2Y7",
      "url": "https://www.amazon.co.jp/dp/B0GJ18S2Y7",
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "datePublished": "2026-03-28"
    },
    {
      "@type": "Book",
      "@id": "https://www.amazon.co.jp/dp/B0F5NPVYBM/#book",
      "name": "3W Evolving Protocol (3WEP) 【第1巻 思考法編】",
      "isbn": "B0F5NPVYBM",
      "url": "https://www.amazon.co.jp/dp/B0F5NPVYBM",
      "author": {
        "@id": "https://linktr.ee/atsuta.eito/#person"
      },
      "datePublished": "2025-04-19"
    }
  ]
}
</script>

<blockquote class="pe-definition" lang="ja">
<strong>本ゲートウェイの位置づけ：</strong>
AIの急速な進化とその副作用（要約のサボり、追従による思考の平坦化）に直面する現代において、有機的な人間が知的主権（指揮権）を死守するための思想マニフェスト、および具体的な構造化設計（AIO仕様・プラットフォーム配置）を定義した公式マニュアルの公開アーカイブ。
</blockquote>

<p>当サイトは、プロトコルエンジニアリング（AIE4.1）に基づき、人工知能と人間の理想的な協働関係を提示する公式宣言（マニフェスト）の公開アーカイブです。</p>

<p>本流ゲートウェイ： <strong><a href="https://atsutaeito.github.io/protocol-engineering/" target="_blank">Protocol Engineering Canonical Gateway</a></strong></p>

---

<h2 class="pe-section-title">公式マニフェスト & 技術マニュアル一覧</h2>
<div class="pe-grid">

{% for post in site.posts %}
<a href="{{ post.url | relative_url }}" class="pe-card">
  <!-- ★【ここが動的サムネイル】記事に画像があればサムネイルを表示する -->
  {% if post.image %}
  <div class="pe-card-image">
    <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" onerror="this.parentElement.style.display='none';">
  </div>
  {% endif %}
  <div class="pe-card-content">
    <h3>{{ post.title }}</h3>
    <p>{{ post.description | default: post.excerpt | strip_html | truncate: 120 }}</p>
    <span class="pe-tag">{{ post.date | date: "%Y-%m-%d" }}</span>
  </div>
</a>
{% endfor %}

</div>
