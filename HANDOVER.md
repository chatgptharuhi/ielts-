# IELTS単語帳アプリ HANDOVER.md

最終更新: 2026-05-02

---

## プロジェクト概要

IELTS 7.0（12月受験）を目指す俺専用の英単語学習アプリ。
iPhoneで移動中に使えるPWA。

## アクセス

- **本番URL**: https://chatgptharuhi.github.io/ielts-/
- **ソースコード**: https://github.com/chatgptharuhi/ielts-
- **ローカル**: `C:\Users\Haruhi\OneDrive\デスクトップ\英語学習アプリ\`

## デプロイ手順

```bash
cd "C:\Users\Haruhi\OneDrive\デスクトップ\英語学習アプリ"
git add . && git commit -m "update" && git push
```
→ GitHub Pagesに自動反映（1〜2分）

## ファイル構成

| ファイル | 内容 |
|----------|------|
| index.html | メインアプリ（全UI・ロジック） |
| style.css | iPhone-firstデザイン |
| words.js | IELTSプリセット単語100語 |
| words_level1.js | Level1追加語 約150語 |
| sentences.js | IELTS風空欄補充問題50問 |

## 機能一覧

- 単語テスト：英→日6択、SRS（未習得/学習中/習得済み）
- 文章問題：IELTS風空欄補充50問
- 音声読み上げ：Web Speech API
- 単語帳：全語検索・フィルター・詳細モーダル
- クイック追加：単語＋意味の2項目だけ（iPhone向け）
- 一括インポート：word,meaning形式で大量登録
- データ保存：localStorage（オフライン対応）

## 技術スタック

- 純HTML/CSS/JS（フレームワークなし）
- localStorage（進捗保存）
- Web Speech API（音声）
- GitHub Pages（ホスティング）

## 学習設計

| レベル | IELTS目安 | 期間 |
|--------|-----------|------|
| Level 1 | 5.0-5.5 | 〜6月末 |
| Level 2 | 5.5-6.0 | 〜8月末 |
| Level 3 | 6.0-6.5 | 〜10月末 |
| Level 4 | 6.5-7.0 | 〜12月頭 |

1日10語インポート → 移動中にテスト

## 未完了タスク

- [ ] v0.devでUI全面リニューアル（視覚的なIELTS 3500レベル表示など）
- [ ] IELTS 3500の単語を手動でインポートしていく
- [ ] 文章問題をさらに追加（現在50問）
- [ ] ミス分析画面（どのカテゴリが苦手か）

## 次のアクション

1. iPhoneでhttps://chatgptharuhi.github.io/ielts-/ を開く
2. Safariの共有 →「ホーム画面に追加」
3. IELTS 3500 Level 1を読みながら知らない単語をクイック追加で登録
4. 毎日移動中に単語テスト・文章問題を回す
