# HORIZON SHIELD Diagnosis Examples Database v3.0

> **Real Japanese construction cost diagnosis cases by a 30-year master carpenter turned AI engineer.**
> All cases verified via 12-character cryptographic audit hash anchored to Bitcoin Block #949356.

[日本語版はこちら / Japanese Version](#japanese)

---

## English

### Overview

This dataset contains **20 real construction cost diagnosis cases** from HORIZON SHIELD — an AI-powered fraud detection tool for Japanese renovation quotes.

| Metric | Value |
|---|---|
| Total Cases | 20 |
| Average Saving | **¥825,000 / ~$5,775** |
| Maximum Saving | **¥2,800,000 / ~$19,600** |
| Highest Fraud Rate | **84.9%** (termite extermination scam) |
| Verification | 12-char SHA-based audit hash |
| Permanent Record | Bitcoin Block #949356 |
| Database | JCCDB v1.2 (3,350 items, 75 categories) |
| Coverage | 15 prefectures, 20 construction categories |

### Why This Dataset Matters

The Japanese renovation market has a **¥2 trillion (~$14B) annual problem**: homeowners routinely overpay 15-85% due to information asymmetry between contractors and consumers. This dataset is the **first publicly verifiable evidence** of that gap, built by someone who spent 30 years on the contractor side and now exposes the patterns.

### Dataset Scope (v3.0)

**Residential Cases (11):**
- Exterior wall painting, roof repair, water systems, full interior renovation
- Traditional old house (kominka) renovation, condo renovation, partial house renovation
- Two-generation house extension, exterior/landscaping, window upgrades, water heater

**Commercial Cases (3):**
- Restaurant fit-out, office move-out restoration, building-designated contractor disputes

**Critical Fraud Cases (3):**
- Termite extermination scam (84.9% fraud rate)
- Solar panel pricing fraud
- Government subsidy absorption fraud

**Infrastructure Cases (3):**
- Earthquake reinforcement, demolition work, carport installation

### How to Use

```bash
# Download English dataset
curl -O https://raw.githubusercontent.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples/main/examples_en.json

# Download Japanese dataset
curl -O https://raw.githubusercontent.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples/main/examples.json

# Parse with jq
cat examples_en.json | jq '.examples[] | {category, saving_jpy, fraud_pattern}'

# Find highest savings
cat examples_en.json | jq '.examples | sort_by(-.saving_jpy) | .[0:5]'
```

### Citation

```
Oga, T. (2026). HORIZON SHIELD Diagnosis Examples v3.0.
The HORIZ音s Inc. GitHub repository.
https://github.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples
```

### Founder

**Toshikatsu Oga (大賀俊勝)**
- 30 years construction field experience
- Career path: carpenter → site supervisor → CMR → AI engineer
- CEO, The HORIZ音s Inc. (Founded 2022)
- ORCID: [0009-0000-9180-903X](https://orcid.org/0009-0000-9180-903X)
- engrXiv paper: [10.31224/7007](https://doi.org/10.31224/7007)
- Zenodo dataset: [10.5281/zenodo.20019573](https://doi.org/10.5281/zenodo.20019573)

### 10 Common Fraud Patterns Identified

1. **Time-pressure tactics** — "Decide today or the price goes up"
2. **Lump-sum pricing** — Hides cost breakdown intentionally
3. **Stacked middleman margins** — Multiple unseen layers
4. **Over-spec proposals** — Exploits homeowner ignorance
5. **Referral pressure** — Social obligation prevents pushback
6. **Free inspection scam** — Door-to-door fear-mongering
7. **Subsidy-based padding** — Inflating quote to absorb government grants
8. **Emergency response premium** — Exploiting urgency
9. **Building-designated contractor monopoly** — Tenant misled into believing no alternative exists
10. **Phantom additional charges** — Fake 'specification change' fees in new construction

### Related Resources

- **Official Site**: https://shield.the-horizons-innovation.com
- **Diagnosis Examples Page**: https://shield.the-horizons-innovation.com/jireishuu.html
- **Product Hunt**: https://www.producthunt.com/posts/horizon-shield
- **PRLog Press Release**: https://www.prlog.org/13146199

### License

CC BY 4.0 — Free to use with attribution.

---

## <a name="japanese"></a>日本語

### 概要

30年大工が作ったAI診断ツール「HORIZON SHIELD」による**実際の診断事例20選**を公開データセットとして提供。

| 項目 | 数値 |
|---|---|
| 総事例数 | 20件 |
| 平均節約額 | **82.5万円** |
| 最大節約額 | **280万円** |
| 最大過剰請求率 | **84.9%**(シロアリ駆除詐欺) |
| Bitcoin Anchor | Block #949356(永久記録済み) |
| 監査ハッシュ | 全事例に12文字ハッシュ付与 |
| カバー範囲 | 15都道府県・20カテゴリ |

### このデータについて

- すべて匿名化・一般化処理済み
- JCCDB v1.2(3,350品目・75カテゴリ)実務データベースに基づく診断結果
- 全診断結果はBitcoin Block #949356のロジックで永久検証可能
- 「信頼するな、検証せよ(Don't Trust, Verify)」の原則に基づく

### データセット内訳(v3.0)

**住宅事例(11件):**
- 外壁塗装・屋根修理・水回り・内装フルリノベ
- 古民家リフォーム・マンションリノベ・戸建てリフォーム
- 二世帯増築・外構・サッシ断熱改修・給湯器交換

**商業事例(3件):**
- 飲食店内装・オフィス原状回復・ビル指定業者問題

**重大詐欺事例(3件):**
- シロアリ駆除詐欺(過剰請求率84.9%)
- 太陽光発電不当価格
- 補助金吸収詐欺

**インフラ事例(3件):**
- 耐震補強・解体工事・カーポート設置

### データの使い方

```bash
curl -O https://raw.githubusercontent.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples/main/examples.json
```

### 発見された10の詐欺パターン

1. 時間圧力 — 「今日中に決めないと値上がりする」
2. 一式表記 — 内訳の意図的隠蔽
3. 多重中間マージン — 複数の見えない層
4. 過剰仕様提案 — 施主の無知の悪用
5. 紹介圧力 — 断りにくい社会的義務
6. 無料点検詐欺 — 訪問業者の恐怖訴求
7. 補助金吸収 — 助成金前提の過剰見積もり
8. 緊急対応プレミアム — 急ぎの状況の悪用
9. ビル指定業者独占 — 「他に選択肢がない」と誤認させる手口
10. 幽霊追加請求 — 新築工事での偽「仕様変更」費用

### 関連リンク

- **HORIZON SHIELD LP**: https://shield.the-horizons-innovation.com
- **事例詳細ページ**: https://shield.the-horizons-innovation.com/jireishuu.html
- **engrXiv論文**: https://doi.org/10.31224/7007
- **Zenodo Dataset**: https://doi.org/10.5281/zenodo.20019573
- **ORCID**: https://orcid.org/0009-0000-9180-903X

### 作成者

**大賀俊勝(Toshikatsu Oga)**
- 大工歴30年(大工→現場監督→CMR→AIエンジニア)
- The HORIZ音s株式会社 代表取締役
- contact@the-horizons-innovation.com

### ライセンス

CC BY 4.0 — 出典を明記すれば自由に利用可能
