# Cafe del Mar — ランディングページ

![Cafe del Mar](img/kakurega-cafe.png)

---

## 概要（コンセプト）

> 「潮騒と、珈琲と、私だけの時間。」

熊本県天草市の海辺に佇む、築60年の古民家を再生した隠れ家カフェ **Cafe del Mar** の架空ランディングページです。

「余白」と「静けさ」をテーマに、訪れた人が時間を忘れてゆったりと過ごせる場所をイメージしてデザインしました。海・砂浜・古民家の質感を、色・フォント・写真の選択で表現しています。

---

## 制作の目的・ターゲット

**目的**
- HTML / CSS / JavaScript を使ったLP制作のポートフォリオ作品として制作
- デザインの参考サイト（[SANKOU!](https://sankoudesign.com/)）を参考に、国内カフェサイトのトレンドを取り入れた実践的なデザインを習得する

**ターゲット**
- 30〜50代の女性を中心とした、日常に「余白」を求めているユーザー
- 旅行・観光で天草を訪れる個人客
- SNSでカフェ情報を探しているユーザー

---

## こだわったポイント

### デザイン

- **カラーパレット**  
  乾いた砂浜（`#f7f3f0`）・穏やかな海（`#7a8d91`）・墨色の茶（`#4a4542`）の3色を軸に、落ち着いた和の雰囲気を演出

- **タイポグラフィ**  
  本文に明朝体（Shippori Mincho）、英語アクセントに手書き風フォント（Dancing Script）を組み合わせ、上品さと温かみを両立

- **縦書き見出し**  
  ヒーローの `writing-mode: vertical-rl` による縦書きキャッチコピーで、日本らしい視覚的インパクトを演出

- **セクション見出しの装飾**  
  見出し下に細い横ラインを引き（`::after` 疑似要素）、シンプルながらも丁寧なデザインに仕上げた

### 機能・インタラクション

- **スクロールアニメーション**  
  `IntersectionObserver` を使い、各セクションが画面に入ったタイミングで下から浮き上がるエフェクトを実装。メニューやギャラリーはアイテムごとに時間差（stagger）をつけた

- **パララックス効果**  
  ヒーローの背景画像に `background-attachment: fixed` を適用し、スクロールの奥行き感を演出（モバイルでは `scroll` に自動切り替え）

- **ホバーエフェクト**  
  メニュー・ギャラリーの画像にカーソルを乗せると、ゆっくり拡大しながら彩度が自然な色味に戻るトランジション

- **ニュースティッカー**  
  JavaScript 不使用・CSS アニメーションのみで、お知らせが自動スクロールする帯を実装

---

## ページ構成

| セクション | 内容 |
|---|---|
| Hero | 海の全画面写真 + 縦書きキャッチコピー |
| Concept | お店のコンセプトと世界観を紹介 |
| News | 最新情報のニュースティッカー |
| Menu | 代表メニューを写真・説明・価格つきで紹介 |
| Gallery | 店内・風景写真のグリッドギャラリー |
| Access | 住所・営業時間・マップ |
| Contact | お問い合わせフォーム |

---

## 使用言語・ツール

| 種別 | 内容 |
|---|---|
| 言語 | HTML / CSS / JavaScript（Vanilla） |
| フォント | [Shippori Mincho](https://fonts.google.com/specimen/Shippori+Mincho)（明朝体）/ [Dancing Script](https://fonts.google.com/specimen/Dancing+Script)（手書き体） |
| リセットCSS | [sanitize.css](https://csstools.github.io/sanitize.css/) |
| 画像素材 | [Unsplash](https://unsplash.com/)（フリー素材） |
| デザイン参考 | [SANKOU!](https://sankoudesign.com/) |
| エディタ | Visual Studio Code |

---

## ファイル構成

```
kakurega-cafe/
├── index.html              # マークアップ（構造）
├── style.css               # スタイリング（デザイン・アニメーション）
├── sanitize.css            # リセットCSS
└── img/
    ├── kakurega-cafe.png       # サムネイル
    ├── hero.jpg                # ヒーロー背景（海）
    ├── menu-coffee.jpg         # メニュー：コーヒー
    ├── menu-tart.jpg           # メニュー：フルーツタルト
    ├── gallery-sea.jpg         # ギャラリー：海の風景
    ├── gallery-interior.jpg    # ギャラリー：店内
    └── gallery-cafe.jpg        # ギャラリー：カフェ外観
```

---

## 動作確認

`index.html` をブラウザで直接開くだけで動作します。サーバーや追加パッケージは不要です。

```bash
# VS Code の場合は Live Server 拡張機能でも起動可能
open index.html
```

---

## 備考

- お問い合わせフォームはUIのみの実装です。実際の送信処理はありません
- 地図エリアは Google Maps のプレースホルダーです
- 掲載している店舗情報（住所・営業時間など）はすべて架空のものです
