# HORIZON SHIELD Diagnosis Examples Database

> **Real Japanese construction cost diagnosis cases by a 30-year master carpenter turned AI engineer.**
> All cases verified via 12-character cryptographic audit hash anchored to Bitcoin Block #949356.

[日本語版はこちら / Japanese Version](#japanese)

---

## English

### Overview

This dataset contains **10 real construction cost diagnosis cases** from HORIZON SHIELD — an AI-powered fraud detection tool for Japanese renovation quotes.

| Metric | Value |
|---|---|
| Total Cases | 10 |
| Average Saving | **¥730,000 / ~$5,100** |
| Maximum Saving | **¥1,200,000 / ~$8,400** |
| Verification | 12-char SHA-based audit hash |
| Permanent Record | Bitcoin Block #949356 |
| Database | JCCDB v1.2 (3,350 items, 75 categories) |

### Why This Dataset Matters

The Japanese renovation market has a **¥2 trillion (~$14B) annual problem**: homeowners routinely overpay 15-45% due to information asymmetry between contractors and consumers. This dataset is the **first publicly verifiable evidence** of that gap, built by someone who spent 30 years on the contractor side and now exposes the patterns.

### How to Use

```bash
# Download dataset
curl -O https://raw.githubusercontent.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples/main/examples_en.json

# Parse with jq
cat examples_en.json | jq '.examples[] | {category, saving_jpy, fraud_pattern}'
```

### Citation

```
Oga, T. (2026). HORIZON SHIELD Diagnosis Examples v2.0.
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

### Common Fraud Patterns Identified

1. **Time-pressure tactics** — "Decide today or the price goes up"
2. **Lump-sum pricing** — Hides cost breakdown intentionally
3. **Stacked middleman margins** — Multiple unseen layers
4. **Over-spec proposals** — Exploits homeowner ignorance
5. **Referral pressure** — Social obligation prevents pushback

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

30年大工が作ったAI診断ツール「HORIZON SHIELD」による**実際の診断事例10選**を公開データセットとして提供。

| 項目 | 数値 |
|---|---|
| 総事例数 | 10件 |
| 平均節約額 | **73万円** |
| 最大節約額 | **120万円** |
| Bitcoin Anchor | Block #949356(永久記録済み) |
| 監査ハッシュ | 全事例に12文字ハッシュ付与 |

### このデータについて

- すべて匿名化・一般化処理済み
- JCCDB v1.2(3,350品目・75カテゴリ)実務データベースに基づく診断結果
- 全診断結果はBitcoin Block #949356のロジックで永久検証可能

### データの使い方

```bash
curl -O https://raw.githubusercontent.com/ogasurfproject-jpg/horizon-shield-diagnosis-examples/main/examples.json
```

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
