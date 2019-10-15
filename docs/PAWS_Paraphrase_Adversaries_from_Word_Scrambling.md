# PAWS: Paraphrase Adversaries from Word Scrambling
語順の入れ替えや文構造の理解に焦点を当てた言い換え認識のデータセット。従来の言い換え認識のデータセットでは、高いbag-of-words overlapを有する負例が極端に少ないため、下記のようなパターンを認識するのは、困難であった。

- Flights from **New York** to **Florida**.
- Flights from **Florida** to **New York**.

そこで、折り返し翻訳と語彙制約付きの言語モデルによる語順並び変えを組み合わせて、言い換え認識のデータセット(PAWS)を構築。

従来の言い換え認識のデータで学習したモデルをPAWSで評価したところ、正解率は40%以下。一方で、PAWSで学習したモデルで従来のデータで評価したところ正解率は85%以上を達成し、従来のデータに比べ、高品質な言い換えデータセットであることを示した。


<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66252771-4e879900-e79a-11e9-983e-3f618c3c60f6.png width=500pt>
</p>


## 文献情報
- 著者: Yinfei Yang, Yuan Zhang, Chris Tar and Jason Baldridge
- リンク: [https://arxiv.org/abs/1904.01130](https://arxiv.org/abs/1904.01130)
- 学会: NAACL2019
- データセット: [https://github.com/google-research-datasets/paws](https://github.com/google-research-datasets/paws)

