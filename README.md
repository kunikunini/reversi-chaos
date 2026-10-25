# リバーシ・カオス（REVERSI//CHAOS）

AI時代の予測不能なオセロ。4色の石が「ペアの裏表」で裏返る、4人対戦リバーシです。

## ルール概要

- 石は2種類だけ：白黒石（表＝黒／裏＝白）と赤青石（表＝赤／裏＝青）
- 挟んだ石は自分の色になるのではなく、**その石のペアの反対色に裏返る**（例：黒が赤を挟むと赤は青になり、青プレイヤーが得をする）
- 対戦形式：4人フリー／シンプル2人／デュオ（2対2）／ペアバトル（モノクロ vs カラー、エース色対決）
- オプション：角プリセット／連鎖モード（波状に連鎖反転）／ガチャ石（手札3枚制）
- CHAOS SCORE：裏返した石で得点（自分の色10点・事故15点）、連鎖倍率と BIG WAVE / MEGA CHAOS / JACKPOT ボーナス
- 観戦モードでは勝者予想ができ、BGMは盤面が埋まるほどテンポと音量が上がります

## 構成

ビルド不要の静的サイトです。

- `index.html` — ゲーム本体（HTML/CSS/JS、音声は Web Audio API のシンセ生成で外部ファイルなし）
- `manifest.webmanifest` / `icons/` / `favicon.png` — PWA（ホーム画面追加）用

## ローカルで開く

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Vercel へデプロイ

1. このリポジトリを GitHub に作成して push
2. Vercel で「Add New → Project」からリポジトリを Import（Framework Preset は Other、ビルド設定は空でOK）
3. Deploy を押せば `***.vercel.app` のURLで公開されます
4. 独自ドメイン（例：reversi.kobakuni.com）は Vercel の Settings → Domains から追加し、DNS に向けてください

以降は GitHub へ push するたびに自動で再デプロイされます。

## 開発について

2026-10-25 未明、AIアシスタント「ポテチ」とのチャットで約1時間で誕生しました。開発の全行程は開発ログページと note 記事で公開しています。

- 開発：小林くにひろ（ https://kobakuni.com/ ）
