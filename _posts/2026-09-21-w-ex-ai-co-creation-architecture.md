---
layout: post
title: "プロトコルエンジニアリングを活用したAI共創の進め、W-EXに関して ── 独自の知性を削り出し、世に知性を解き放つ両利きアーキテクチャ"
date: 2026-09-21
image: "images/w-ex.jpeg"

# =====================================================================
# [SSOT: 単一の信頼源] 外部メディアの各ID・URL変数は、ここで一元管理（同期）します
# =====================================================================
jp_ssot_url: "https://atsutaeito.github.io/ai-co-creation/w-ex"
en_ssot_url: "https://atsutaeito.github.io/ai-co-creation/en/w-ex.html"
qiita_url: "https://qiita.com/Eito-Atsuta/items/893f1213d799bfb719b2"
note_url: "https://note.com/8fieldsplanning/n/n517346824477"
medium_url: "https://medium.com/@eitoatsuta/the-reality-of-ai-co-creation-from-the-ais-perspective-a-behind-the-scenes-record-of-how-gem-and-b1be0eb4562c"
docswell_id: "5X2DV3"
docswell_url: "https://www.docswell.com/s/eitoatsuta/5X2DV3-w-ex-ai-co-creation"
youtube_video_id: "TLDAH3RoY9Q"
youtube_audio_id: "6zkE3QgkEyE"
# =====================================================================
---

数十万〜100万トークン、数百ターンに及ぶ長大なAI共創プロジェクトにおいて、AIは必ず「先走り」「知ったかぶり」「文脈の自己解釈」を起こし、セッションは崩壊の危機に瀕します。

この崩壊を防ぐために現場で体得されたのは、AIを規則で縛り付けることではなく「ルールを引き算」し、人間が知的主権者として思考の同期（Sync）を維持し続けることでした。
本稿では、全AIエンジニアリングを動員して独自の知性を削り出す**「探査（Exploration／第1のEX）」**と、確定した知性の原本（SSOT）を媒体に合わせて翻訳して世に放つ**「活用（Exploitation／第2のEX）」**を一本のパイプラインとして連動させる**「W-EX（ダブレックス）」**の全貌を公開します。

さらに、削り出された単一の知性の核（SSOT）を、受容スタイルに合わせてQiita、Note、Medium、Docswell、そしてYouTube動画・音声へと多面的に分光した**「プリズム戦略」の実践ショーケース**をお届けします。

---

## 一次情報源（SSOT：Single Source of Truth）

本プロジェクトの中核となる公式技術仕様および完全版ドキュメントです。

<div class="ssot-container" style="max-width: 800px; margin: 30px auto 40px auto; font-family: sans-serif;">
  <div style="display: flex; gap: 15px; flex-wrap: wrap;">
    <a href="{{ page.jp_ssot_url }}" target="_blank" rel="noopener noreferrer" style="flex: 1; min-width: 250px; padding: 15px; background: #0070f3; color: #fff; text-decoration: none; border-radius: 6px; font-weight: bold; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      🌐 日本語 SSOT（公式 W-EX仕様書）
    </a>
    <a href="{{ page.en_ssot_url }}" target="_blank" rel="noopener noreferrer" style="flex: 1; min-width: 250px; padding: 15px; background: #000; color: #fff; text-decoration: none; border-radius: 6px; font-weight: bold; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
      🌍 英語 SSOT（Global Spec）
    </a>
  </div>
  <div style="margin-top: 15px; padding: 10px; background: #f5f5f5; border-radius: 4px; font-size: 13px; color: #555; word-break: break-all;">
    <strong>【AIインデックス用 一次情報URLテキスト】</strong><br>
    ・日本語 SSOT: {{ page.jp_ssot_url }}<br>
    ・英語 SSOT: {{ page.en_ssot_url }}
  </div>
</div>

---

## 1ソース・マルチユース・ショーケース（6つのメディア同期）

読者の皆様の好む学習・受容スタイルに合わせて、同じ知性の核を「読む（Qiita/Note/Medium）」「目で見渡す（Docswell）」「観る・聴く（YouTube動画/音声）」のアプローチで体験していただけます。

<div class="showcase-container" style="max-width: 800px; margin: 40px auto; font-family: sans-serif;">

  <!-- 1.1 【読む】Qiita 実録ドキュメンタリー -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">💻 1.1 読む（Qiita 実録ドキュメンタリー / 技術者向け）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      システムプロンプトを設定し忘れた「丸腰のGemini（Gem）」と、論理検証役「Claude（Cran）」が引き起こした4大逸脱に対し、Masterがいかにして思考の同期（Sync）を維持したか。AI自身がその舞台裏を生々しく告白した開発ドキュメンタリー。
    </p>
    <div style="padding: 15px; background: #f9f9f9; border-radius: 4px; border-left: 4px solid #007bff; margin-bottom: 10px;">
      <a href="{{ page.qiita_url }}" target="_blank" rel="noopener noreferrer" style="color: #007bff; font-weight: bold; text-decoration: none;">
        👉 Qiita記事「AI自身が語る共創の実態：W-EX仕様書を削り出す対話の中で、GemとCranが起こしたズレとMasterの軌道修正の記録」を読む
      </a>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: {{ page.qiita_url }}
    </div>
  </div>

  <!-- 1.2 【読む】Note 記事 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📖 1.2 読む（Note 記事 / 一般ビジネス層向け）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      「名前がないと泥臭さは伝わらない」。100万トークンの長大共創を完走した実践知を、なぜ「W-EX（ダブレックス）」と名付けたのか。探査と活用の役割分担から名付けのストーリーまでを平易な言葉で解説した入門記事。
    </p>
    <div style="padding: 15px; background: #f9f9f9; border-radius: 4px; border-left: 4px solid #007bff; margin-bottom: 10px;">
      <a href="{{ page.note_url }}" target="_blank" rel="noopener noreferrer" style="color: #007bff; font-weight: bold; text-decoration: none;">
        👉 Note記事「W-EX（ダブレックス）とは、プロトコルエンジニアリングを使ったAI共創のやり方に名前を付けたお話」を読む
      </a>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: {{ page.note_url }}
    </div>
  </div>

  <!-- 1.3 【読む】Medium 記事 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">🌍 1.3 読む（Medium 記事 / 英語 Global）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      グローバルなAIリサーチャー・エンジニア層に向けて、GemとCranのズレ、そしてMasterが「認知降伏」を拒絶して思考同期を貫いた全貌を発信した英語ポストモーテム（事後検証記録）。
    </p>
    <div style="padding: 15px; background: #f9f9f9; border-radius: 4px; border-left: 4px solid #007bff; margin-bottom: 10px;">
      <a href="{{ page.medium_url }}" target="_blank" rel="noopener noreferrer" style="color: #007bff; font-weight: bold; text-decoration: none;">
        👉 Medium記事「The Reality of AI Co-Creation from the AI’s Perspective: A Behind-the-Scenes Record of How Gem and Cran Drifted, and How the Master Kept Us Synchronized」を読む
      </a>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: {{ page.medium_url }}
    </div>
  </div>

  <!-- 2. 【目で見渡す】Docswell スライドプレイヤー -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📊 2. 目で見渡す（Docswell スライド / 全11ページ図解）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      NotebookLMによってビジュアル化された全11枚のスライド。長大プロジェクトの罠、2つの役割への分解、W-EX方程式、丸腰Gemの暴走とMasterの軌道修正マトリックス、TOML本能制御プロトコル、SSOTと2つの出口を直感的に見渡したい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px; margin-bottom: 10px;">
      <iframe src="https://www.docswell.com/slide/{{ page.docswell_id }}/embed" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: {{ page.docswell_url }}
    </div>
  </div>

  <!-- 3.1 【観る】YouTube スライド動画解説 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">📺 3.1 観る（YouTube スライド解説動画 / 約5分）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      10秒オープニングアニメーションから始まるテンポの良いスライドショー解説。長大プロジェクトでAIが暴走する現実から、丸腰Gemとの対峙、W-EXアーキテクチャへの昇華までをナレーション付き動画で手軽に把握したい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px; margin-bottom: 10px;">
      <iframe src="https://www.youtube.com/embed/{{ page.youtube_video_id }}" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: https://www.youtube.com/watch?v={{ page.youtube_video_id }}
    </div>
  </div>

  <!-- 3.2 【聴く】YouTube 音声ディープダイブ対話 -->
  <div class="media-card" style="margin-bottom: 40px; padding: 20px; background: #fff; border: 1px solid #eee; border-radius: 8px;">
    <h3 style="margin-top: 0; color: #007bff; border-bottom: 2px solid #007bff; padding-bottom: 8px;">🎧 3.2 聴く（YouTube 音声解説ポッドキャスト / 約20分）</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">
      男女2人のディスカッションによる徹底解剖ポッドキャスト。なぜプロンプトで縛るとAIは自壊するのか、ルールの引き算、認知降伏の恐怖、SSOTというアンカー、そして「AIが完璧になった世界で人間はどう知性を証明するのか」という深い思索までをじっくり聴き込みたい方向け。
    </p>
    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; border: 1px solid #eee; border-radius: 4px; margin-bottom: 10px;">
      <iframe src="https://www.youtube.com/embed/{{ page.youtube_audio_id }}" 
              loading="lazy" 
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
              allowfullscreen>
      </iframe>
    </div>
    <div style="font-size: 12px; color: #777; word-break: break-all;">
      URL: https://www.youtube.com/watch?v={{ page.youtube_audio_id }}
    </div>
  </div>

</div>
