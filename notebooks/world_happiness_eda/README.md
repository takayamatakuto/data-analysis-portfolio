# World Happiness Report 2019 各国幸福度の要因分析（EDA） : Exploratory Data Analysis

## 概要
本分析では、Kaggleに公開されているWorld Happiness Reportのうち、2019年データを対象として探索的データ分析（EDA）を行った。本EDAの目的は、幸福度スコア（Score）と各指標との関係を把握する事、及びEDAの経験を積む事である。

## データセット
- データ名：World Happiness Report 2019
- 観測単位：国
- 主な変数：
  - Happiness Score
  - GDP per capita
  - Social support
  - Healthy life expectancy
  - Freedom to make life choices
  - Generosity
  - Perceptions of corruption

※ 2015〜2019年の時系列データも存在するが、本分析では学習段階を考慮し、単年データ（2019年）のみに絞ってEDAを行った。

## 分析方針
本EDAでは以下の方針で分析を進めた。

- まずは欠損や分布を確認し、データ全体の性質を把握する
- 幸福度スコアと各指標との相関関係を確認する
- 相関の結果から、以降に検証すべき仮説を整理する

## 主な観察結果
- GDP per capitaとHealthy life expectancyは、幸福度スコアと強い正の相関を示した
- Freedom to make life choicesは相関が見られるものの、分布の幅が広かった
- Perceptions of corruptionは、値が高い（汚職が少ないと認識されている）国では幸福度スコアが高い傾向が見られたが、低い値の領域では、ばらつきが大きかった
- Generosityは幸福度スコアとの相関が弱く、本データから明確な影響を読み取るのは困難であった

## 仮説と今後の検討事項
本EDAから、以下のような仮説・論点が考えられる。

- GDPと健康寿命は、ともに「社会的発展度」を反映する共通因子として扱える可能性がある
- 汚職認識と幸福度の関係は、地域や文化圏によって異なる可能性がある
- Generosityの影響は、本データからは読み取れなかったが、他の要因に影響を与えている可能性は否定できない
## リポジトリ構成
```
world_happiness_eda/
├─README.md           
└─world_happiness_eda.ipynb
```
## 今回行わなかったこと
- 時系列分析（2015–2019）
- 地域別比較分析
- 回帰分析や機械学習モデルによる検証

これらについては、着実な学習を重視し、本EDAでは扱わなかった。