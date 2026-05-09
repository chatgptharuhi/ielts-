# 英語学習アプリ 外部脳

セッション間の学習進捗・改善記録・単語追加履歴を管理します。

---

## 📚 Wiki 構造

```
wiki/
├─ index.md          ← マスターインデックス
├─ hot.md            ← 直近セッション記憶（最新3セッション）
├─ words/            ← 単語追加ログ
│  └─ session_YYYYMMDD.md
├─ features/         ← 機能実装ログ
│  └─ YYYY-MM-DD_機能名.md
└─ analysis/         ← 学習分析
   └─ insights.md
```

---

## 🔄 更新タイミング

- **セッション終了時** — `/save` で会話を Wiki ページ化
- **単語追加 50語ごと** — `words/session_YYYYMMDD.md` に記録
- **機能改善時** — `features/` に実装ログ記録
- **定期分析** — `analysis/insights.md` を月1回更新

---

## 📖 使用例

### 【Session 4: 2026-05-09】
`hot.md` に記録：
- Issue①修正：同一セッション内の単語重複を排除（wordSessionHistory Set）
- Issue②修正：選択肢の品詞を統一（generateChoices 改修）
- セッション = 20単語固定（WORDS_PER_SESSION）
- 問い目数表示追加（問X/20）
- **追加単語数:** 60語（total: 216語）

### 【Words Log】
`wiki/words/session_20260509.md`:
```
# 2026-05-09: +60 Words

## 追加単語リスト
- committee (noun) - 委員会
- tackle (verb) - 取り組む
- union (noun) - 労働組合
...

## レベル内訳
- Level 1: 60語
- Total: 216語
```

---

## 🎯 今後の方針

- [ ] Level 1 残り 90語をインポート（2026年5月末）
- [ ] Level 2 開始（2026年6月初旬）
- [ ] 文章問題の単語セット別補充ログ
- [ ] 月ごとの学習進捗分析

---

**Last Updated:** 2026-05-09
**Sessions Tracked:** 1
**Total Words:** 216
