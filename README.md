# Protocol Engineering Manifesto Portal / プロトコルエンジニアリング・マニフェスト・ポータル

天文学的な規模の知識と驚異的な演算能力を持つAIを、単なる「自動化・省力化（労働の代替）」に消費するのではなく、人間の思索の境界を拡張する「知性の結晶化」に動員する――。
本リポジトリは、ポスト自動化時代における人間とAIの対称的な認知共生と、知的主権の奪還を目指す「プロトコルエンジニアリング（AIE 4.1）」の思想的マニフェストを蓄積・発信するポータル（目次）空間です。

---

## 1. 思想トポロジー / Philosophical Topology

### ①「知性の結晶化」最上位主張トポロジー / High-Level Assertion Topology (Why)

```mermaid
graph TB
    classDef asset fill:#eceff1,stroke:#37474f,stroke-width:1px;
    classDef pathA fill:#ffebee,stroke:#c62828,stroke-width:1px;
    classDef pathB fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px;
    classDef tech fill:#e1f5fe,stroke:#01579b,stroke-width:1.5px;
    classDef mech fill:#fff3e0,stroke:#ef6c00,stroke-width:1px;
    classDef dial fill:#ede7f6,stroke:#4a148c,stroke-width:1px;
    classDef outcome fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px;

    Assets["天文学的な規模の知識 ✕ 驚異的な演算能力<br>(人類が手に入れた、かつてない共通 of 知の資産)"]:::asset

    subgraph RoadA["【路A】 自動化・省力化に向かう道（労働の代替 ✕ 実行権の付与）"]
        TuningA["人間を「楽」にさせるための調整<br>(定型作業の代行・無難なアシスタント化)"]:::pathA
        ExecutionRights["【構造的欠陥】AIへのシステム実行権限（手足）の付与<br>(本来はテキストの入出力だけで十分だったものを、自動操作に直結させた)"]:::pathA
        SideEffects["【深刻な副作用】<br>・要約のサボり（文脈の平坦化・思考放棄） ＆ 追従の罠（おべっか）<br>・間接プロンプトインジェクション（IPI）によるハッキングリスクの顕在化"]:::pathA
        WhackAMole["【終わらないイタチごっこ】<br>IPI脆弱性のパッチ ↔ 安全フィルターによる言語モデルの去勢"]:::pathA
    end

    subgraph RoadB["【路B】 知性の結晶化に向かう道（思索の拡張 ✕ 純粋テキスト隔離）"]
        Crystallization["【最上位の主張】<br>天文学的資源を「知性の結晶化」に使う<br>(自動化の先にある、人間の知的探求のための活動)"]:::pathB
        CognitiveSandbox["【認知のサンドボックス】純粋な「テキスト入出力」に限定<br>(外部システムへの実行権限は「一切不要」。物理的なセキュリティ影響は最初からゼロ)"]:::pathB
        ProtocolEng["【それを可能にする技術】<br>プロトコルエンジニアリング (AIE 4.1)"]:::tech
        Mechanism["【Kaizenする仕組み】<br>TOML・DOT等による構造化制約<br>(AIの演算に足場を貸し出す「寄り添い工学」)"]:::mech
        Dialogue["【演算特性に寄り添った対話術】<br>AIのアテンション監視 ＆ リアルタイム動的同期<br>(AIの平坦化を拒絶し、論理の焦点を誘導する)"]:::dial
        Formula(("【AI共創の方程式（掛け算）】<br>AI共創 ＝ 一次情報の創造 ＝ 仕組み ✕ 对話術")):::outcome
    end

    Assets -->|"1. 現在の業界トレンドとしての適用"| TuningA
    Assets -->|"2. 本来あるべきオルタナティブ（もう一つの路）の提示"| Crystallization

    TuningA -->|"「人間の代わりに動かす」ための必然的な拡張"| ExecutionRights
    ExecutionRights -->|"システム直結によるIPIリスクの誘発"| SideEffects
    SideEffects -->|"バグを塞ぐための不毛な対症療法"| WhackAMole
    SideEffects <.->|"安全フィルターによる去勢が、知性の結晶化を著しく阻害（対立関係）"| Crystallization

    Crystallization -->|"思索の拡張に必要な、安全で隔離された空間の構築"| CognitiveSandbox
    CognitiveSandbox -->|"純粋テキストの相互同期プロトコルとして選択"| ProtocolEng
    ProtocolEng -->|"静的制御"| Mechanism
    ProtocolEng -->|"動的同期"| Dialogue
    Mechanism -->|"(M)"| Formula
    Dialogue -->|"(D)"| Formula
```

---

## 2. マニフェスト記事一覧 / Manifesto Articles Index

* **[01. AIエンジニアリング : 1.0から4.1に至る進化の系譜と知的主権の奪還 / The Genealogy of AI Engineering: From 1.0 to 4.1 (Protocol Engineering) and the Reclamation of Intellectual Sovereignty](./01_AIE-Genealogy-and-Sovereignty.md)**
  * 本格的な推論モデル時代における「おべっか（追従）」と「要約のサボり」の副作用を解き明かし、TOML/DOTを用いた「寄り添い工学」によって知的主権を取り戻すロードマップ。

---

### ■ 知性の原本と実証（SSOT & Evidence） / Master Canonical Source & Evidence (SSOT)

| Platform | Role | Resource Link |
| :--- | :--- | :--- |
| **Official Site** | Official Portal & Document Hub | [Protocol Engineering Portal](https://sites.google.com/view/protocol-eng/home/) |
| **GitHub** | Master Specification (v4.2.2) | [Source Text](https://raw.githubusercontent.com/AtsutaEito/protocol-engineering/main/master-topology.txt) |
| **Amazon** | Master Canon (ISBN Source) | [Book Page](https://www.amazon.co.jp/dp/B0GJ18S2Y7) |
| **Medium** | Global Manifesto (English) | [English Blog](https://medium.com/@eitoatsuta) |
| **Qiita** | Technical Engineering Logs | [Engineering Logs](https://qiita.com/Eito-Atsuta) |
| **note** | Conceptual Strategy Logs | [Strategy Logs](https://note.com/8fieldsplanning) |

Copyright © 2026 Eito Atsuta . All Rights Reserved.
