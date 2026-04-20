# RobustAction

Padgett & Ansell (1993) "Robust Action and the Rise of the Medici, 1400-1434" の読書ノートと分析コード。

15世紀フィレンツェにおけるメディチ家の台頭を、婚姻・ビジネスのネットワークデータを用いて分析する。
教科書 *Quantitative Social Science* (Imai 2017) の内容を出発点に、原論文の知見をRで拡張した。

## ファイル構成

| ファイル | 内容 |
| --- | --- |
| [`paper_notes.md`](paper_notes.md) | 論文の背景・理論・知見のまとめ |
| [`reading_notes.md`](reading_notes.md) | Rによる分析（コード＋実行結果＋グラフ） |
| `reading_notes.Rmd` | 上記のRソースコード |

- **論文の内容を知りたい** → [`paper_notes.md`](paper_notes.md)
- **分析コードと結果を見たい** → [`reading_notes.md`](reading_notes.md)

## 分析内容

1. **婚姻ネットワークの中心性分析** -- 次数・近接・媒介中心性の比較
2. **富・政治参加 vs ネットワーク構造** -- 権力の源泉は経済力か、ポジションか
3. **ビジネスネットワークとの比較** -- 婚姻とビジネスで異なる相手と繋がるブローカー戦略
4. **ノード除去シミュレーション** -- メディチ家の構造的重要性の検証
5. **コミュニティ検出** -- ネットワーク構造から歴史的派閥を自動検出

## 使用データ

`ergm` パッケージの組み込みデータセット `florentine`（`flomarriage`, `flobusiness`）を使用。
外部データのダウンロードは不要。

## 実行方法

```r
# 必要なパッケージ
install.packages(c("ergm", "igraph", "ggplot2", "ggrepel", "gridExtra", "rmarkdown", "ragg"))

# レンダリング
rmarkdown::render("reading_notes.Rmd")
```

## 参考文献

- Padgett, J. F., & Ansell, C. K. (1993). Robust Action and the Rise of the Medici, 1400-1434. *American Journal of Sociology*, 98(6), 1259--1319. https://doi.org/10.1086/230190
- Imai, K. (2017). *Quantitative Social Science: An Introduction*. Princeton University Press.
- Kent, D. V. (1978). *The Rise of the Medici: Faction in Florence, 1426-1434*. Oxford University Press.
- Burt, R. S. (1992). *Structural Holes: The Social Structure of Competition*. Harvard University Press.
