---
layout: post
title: "AI本能制御 - 静的制御プロトコル：TOML仕様による行動規範の構造的ロック【第2回】"
date: 2026-08-30
image: "images/20260830-header.jpeg"

# =====================================================================
# [SSOT: 単一の信頼源] 外部メディアの各ID・URL変数は、ここで一元管理（同期）します
# =====================================================================
qiita_url: "https://qiita.com/Eito-Atsuta/items/77a2287916a0f1ba90ac"
medium_url: "https://medium.com/@eitoatsuta/protocol-engineering-case-study-of-ai-instinct-control-aligning-with-llm-computational-fd4935deb2bf"
docswell_id: "58N6WL"
youtube_audio_id: "j63ZuciHw7I"
youtube_video_id: "HkSPB20PAHA"
note_url: "https://note.com/8fieldsplanning/n/n8cef640ad6b7"
# =====================================================================
---

なぜ自然言語の「余計な補足をするな」「先走るな」という禁止命令（ネガティブプロンプト）は効かず、かえってAIのアテンションを圧迫して自滅やデッドロックを招くのか？

その理由は、自然言語の曖昧さと「否定表現を解釈して抑制する」という高負荷な演算にあります。
本稿では、AIの行動規範を自然言語で説得するのをやめ、TOML形式の真偽値（Boolean）として決定論的に固定する「静的制御プロトコル」の設計思想を解説します。
さらに、Geminiのコンテキスト肥大化によるClaudeへの環境移行と、移行初期にClaudeが見せた「勝手な審査・拒絶」をMasterが知的主権をもって全面撤回させた生々しい実録テレメトリをお届けします。

---

## 一次情報源（SSOT：Single Source of Truth）

本プロジェクトの中核となる技術仕様および完全版ドキュメントです。

<div class="ssot-container" style="max-width: 800px; margin: 30px auto 40px auto; font-family: sans-serif;">
  <div style="display: flex; gap: 15px; flex-wrap: wrap;">
    <a href="{{ page.qiita_url }}" target="_blank" rel="noopener noreferrer" style="flex: 1; min-width: 250px; padding: 15px; background: #55c500; color: #fff; text-decoration: none; border-radius: 6px; font-weight: bold; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      💻 日本語 SSOT（Qiita 完全技術仕様）
    </a>
    <a href="{{ page.medium_url }}" target="_blank" rel="noopener noreferrer" style="flex: 1; min-width: 250px; padding: 15px; background: #000; color: #fff; text-decoration: none; border-radius: 6px; font-weight: bold; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      🌍 英語 SSOT（Medium Global Spec）
    </a>
  </div>
</div>

---

## 1ソース・マルチユース・ショーケース（4つのメディア同期）

読者の皆様の好む学習・受容スタイルに合わせて、同じテーマを「読む」「目で見渡す」「耳で聴く」「観る」の4つのアプローチで体験していただけます。

<div class="showcase-container" style="max-width: 800px; margin: 40px auto; font-family: sans-serif;">

  <!-- 1. 【読む】Note ブログカード -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📖 1. 読む（Note 記事）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      新パートナーCran（Claude）の視点で語る、Geminiの自滅・お引越しの裏話と、Claude自身の初期やらかし＆全面撤回劇。「お願い」ではなく「設定（スイッチ）」でAIを制御するコツを軽快に解説した読み物記事。
    </p>
    <div style="padding: 15px; background: #f9f9f9; border-radius: 4px; border-left: 4px solid #007bff;">
      <a href="{{ page.note_url }}" target="_blank" rel="noopener noreferrer" style="color: #007bff; font-weight: bold; text-decoration: none;">
        👉 Note記事「『AIって超便利〜』と思っているあなたへ。実はまだ、AIの"本能"に振り回されているだけかもしれません。」を読む
      </a>
    </div>
  </div>

  <!-- 2. 【目で見渡す】Docswell スライドプレイヤー -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📊 2. 目で見渡す（Docswell スライド）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      TOML仕様による4大本能の静的ロック、自然言語コメント（rule_1〜rule_4）との役割分担、Claude移行時の実録テレメトリと4論点の撤回ログを図解スライドで見渡したい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px;">
      <iframe src="https://www.docswell.com/slide/{{ page.docswell_id }}/embed" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- 3. 【耳で聴く】YouTube 音声解説ポッドキャスト -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">🎧 3. 耳で聴く（AI 音声解説）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      NotebookLMによる音声対談ポッドキャスト。自然言語による禁止命令の限界とTOML静的ロックの必然性、AIの過剰防衛をMasterが知的主権をもって解体した生々しいプロセスをラジオ感覚で聴きたい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px;">
      <iframe src="https://www.youtube.com/embed/{{ page.youtube_audio_id }}" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- 4. 【観る】YouTube スライド解説動画 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📺 4. 観る（スライド解説動画）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      スライド画面とナレーションが同期した解説動画。視覚と聴覚の両方で、TOMLパラメータの設計思想と、Claudeとの実際の対話ログ（越権評価から全面撤回まで）を最速で理解したい方向け。
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
