# Fine-tune BERT for Extractive Summarization

BERTを抽出型要約にfine-tuningする手法を提案。BERTでは、トークンレベルのタスク(マスク単語予測)を解いているので、これを文レベルに拡張するために、下図のように、各文の先頭に[CLS]、末尾に[SEP]を挿入することによって文境界の情報を与えている。[CLS]の位置に対応する出力ベクトルを文のベクトルとみなす。BERTの上に、Summarization Layersをのせることで二値分類を行う。Summarization Layersは、3種類 (Linear layer, Inter-sentence Transformer, RNN)用いて比較を行っている。



![bertsum](https://user-images.githubusercontent.com/53220859/63507683-3ffb6000-c513-11e9-99d8-edfe75387c28.png)

※ 図は元論文から引用。

<br>





## 文献情報

- 著者: Yang Liu
- リンク: [https://arxiv.org/abs/1903.10318](https://arxiv.org/abs/1903.10318)

