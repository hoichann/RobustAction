# RobustAction

Padgett & Ansell (1993) "Robust Action and the Rise of the Medici, 1400-1434" の再現と拡張分析。

15世紀フィレンツェにおけるメディチ家の台頭を、婚姻・ビジネスのネットワークデータを用いて分析する。
教科書 *Quantitative Social Science* (Imai 2017) の内容を出発点に、原論文の知見をRで再現・拡張した。

## 分析内容

1. **婚姻ネットワークの中心性分析** -- 次数・近接・媒介中心性の比較
2. **富・政治参加 vs ネットワーク構造** -- 権力の源泉は経済力か、ポジションか
3. **ビジネスネットワークとの比較** -- 婚姻とビジネスで異なる相手と繋がるブローカー戦略
4. **ノード除去シミュレーション** -- メディチ家の構造的重要性の検証
5. **コミュニティ検出** -- ネットワーク構造から歴史的派閥を自動検出

## ファイル構成

| ファイル | 内容 |
| --- | --- |
| `Padgett1993_Medici.Rmd` | Rソースコード |
| `Padgett1993_Medici.md` | レンダリング済み（GitHub上で閲覧可能） |
| `Padgett1993_Medici_files/` | グラフ画像 |

## 使用データ

`ergm` パッケージの組み込みデータセット `florentine`（`flomarriage`, `flobusiness`）を使用。
外部データのダウンロードは不要。

## 実行方法

```r
# 必要なパッケージ
install.packages(c("ergm", "igraph", "ggplot2", "ggrepel", "gridExtra", "rmarkdown"))

# レンダリング
rmarkdown::render("Padgett1993_Medici.Rmd")
```

## 参考文献

- Padgett, J. F., & Ansell, C. K. (1993). Robust Action and the Rise of the Medici, 1400-1434. *American Journal of Sociology*, 98(6), 1259--1319. https://doi.org/10.1086/230190
- Imai, K. (2017). *Quantitative Social Science: An Introduction*. Princeton University Press.
- Kent, D. V. (1978). *The Rise of the Medici: Faction in Florence, 1426-1434*. Oxford University Press.
- Burt, R. S. (1992). *Structural Holes: The Social Structure of Competition*. Harvard University Press.
