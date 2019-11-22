# Controlling Neural Machine Translation Formality with Synthetic Supervision

機械翻訳 における出力スタイル(formal, informal)を制御することを目的とした研究。翻訳のためのデータはたくさん存在するが、形式を表すラベル(formal, informal)が付与されている翻訳データは非常に限られている。ここでは、翻訳とスタイル制御のmulti-task learning及びSynthetic Supervisionにより、既存の手法を上回る性能を達成。

Synthetic Supervisionでは、事前学習したスタイル制御翻訳(FNMT)モデルを用いて、1つの入力に対しformal, informalな文を生成し、それらにおけるcross-entropy differenceを元に、閾値を用いて、<2formal>, <2informal>, <2unknown>の擬似的なラベルを与える。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/69333140-7758e480-0c9b-11ea-8ff3-65c346a2b8c9.png width=450pt>
</p>



## 文献情報 (Authors and URL of the paper)

- 著者: Xing Niu, Marine Carpua
- リンク: https://arxiv.org/abs/1911.08706
- 学会: AAAI2020