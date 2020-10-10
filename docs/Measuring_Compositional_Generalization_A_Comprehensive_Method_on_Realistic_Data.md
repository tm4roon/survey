# Measuring Compositional Generalization: A Comprehensive Method on Realistic Data

汎化性能を評価する新たな方法を提案した論文。従来では、訓練データとテストデータを、文の長さやクラスタリングを用いて分割する方法が提案されていた。本研究ではSemantic Parsingを対象とし、文の構造に注目した分割による汎化性能の評価手法を提案している。今回利用するデータは、以下のようにあらかじめ用意したテンプレート(Compounds)を穴埋めする形で生成されたデータである。構成されているCompoundsの類似性で訓練データとテストデータを分割する、というのが提案手法である。



<p align="center">
  <img width="800" src="https://user-images.githubusercontent.com/53220859/95658618-bcf1fa80-0b56-11eb-89f2-f9e49a853919.png">
</p>



Compound divergenceが低い場合にはすべてのモデルで95%以上の精度を達成するが、Compound divergence高い場合は、すべてのモデルで20%以下の精度となり、訓練データとテストデータの間で利用している単語が類似した大規模な訓練セットであっても、モデルの汎化性能向上に十分ではないことを意味している。

<p align="center">
  <img width="500" src="https://user-images.githubusercontent.com/53220859/95658506-dc3c5800-0b55-11eb-95cc-d3ad027325ce.png">
</p>





## 文献情報

- 著者: Daniel Keysers, Nathanael Schärli, Nathan Scales, Hylke Buisman, Daniel Furrer, Sergii Kashubin, Nikola Momchev, Danila Sinopalnikov, Lukasz Stafiniak, Tibor Tihon, Dmitry Tsarkov, Xiao Wang, Marc van Zee & Olivier Bousquet
- リンク: [https://arxiv.org/abs/1912.09713](https://arxiv.org/abs/1912.09713)
- 学会: ICLR2020
- ブログ: https://ai.googleblog.com/2020/03/measuring-compositional-generalization.html