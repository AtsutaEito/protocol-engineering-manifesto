---
layout: post
title: "[AI共創]で解決 #1：対話が長くなると忘れたり、当たり障りのない応答を防ぐには"
date: 2026-07-15
image: "images/20260715-header.png"

# =====================================================================
# [SSOT: 単一の信頼源] 外部メディアの各ID・URL変数は、ここで一元管理（同期）します
# =====================================================================
note_id: "n56bde65ba241"
docswell_id: "K27WG7"
youtube_audio_id: "6ZgtbVK2yqw"
youtube_video_id: "M5nCb8TLokk"
# =====================================================================
---

「AI共創」という言葉に耳障りの良いポジティブなファンタジーや、お気持ち重視の考え方の記事が多くありませんか？
実際にAI共創を行うと思った通りに対話できないという現実に直面することありますよね。
AIが指示を忘れる、ルールを無視する、サボるという限界性能が顔を見せる。それを防げるのは人間側のハンドリングなんです。
プロトコルエンジニアリング視点で、ハンドリングのヒントをお届けしていきます。

---

## 1ソース・マルチユース・ショーケース（4つのメディア同期）

読者の皆様の好む学習スタイルに合わせて、同じテーマを「読む」「目で見渡す」「耳で聴く」「観る」の4つのアプローチで体験していただけます。

<div class="showcase-container" style="max-width: 800px; margin: 40px auto; font-family: sans-serif;">

  <!-- 1. 【読む】Note ブログカード -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📖 1. 読む（Note 記事）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      テキスト論理と思想。なぜ長距離走の対話が破綻するのか、詳細な背景を深く読みたい方向け。
    </p>
    <iframe class="note-embed" 
            src="https://note.com/embed/notes/{{ page.note_id }}" 
            loading="lazy" 
            style="border: 0; display: block; max-width: 100%; width: 100%; height: 400px; border-radius: 4px;">
    </iframe>
  </div>

  <!-- 2. 【目で見渡す】Docswell スライドプレイヤー -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📊 2. 目で見渡す（Docswell スライド）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      構造化されたドキュメントと図解。情報の論理的な繋がりや、TOMLによる制御の全体像を一瞬で掴みたい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px;">
      <iframe src="https://www.docswell.com/slide/{{ page.docswell_id }}/embed" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- 3. 【耳で聴く】YouTube Music ポッドキャスト -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">🎧 3. 耳で聴く（AI 音声解説）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      NotebookLM自動生成によるポッドキャスト。通勤中や他の作業をしながら、2人のAIホストによる知的でリアルな対談を楽しみたい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 8px;">
      <iframe src="https://www.youtube.com/embed/{{ page.youtube_audio_id }}" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- 4. 【観る】YouTube スライド解説動画 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📺 4. 観る（AI スライド解説動画）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      スライドと音声ナレーションが同期したNotebookLM自動生成動画。視覚と聴覚の両方で、解決策のプロトコルを最速で理解したい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border-radius: 4px;">
      <iframe src="https://www.youtube.com/embed/{{ page.youtube_video_id }}" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
  </div>

</div>
