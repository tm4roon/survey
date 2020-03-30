# Large Scale Question Paraphrase Retrieval with Smoothed Deep Metric Learning
Question Paraphrase Retrieval(QPR) taskにおいて、従来の損失関数Triplet loss(TR)ではノイズデータの影響を受けやすい傾向にあった。ここでは、ノイズデータの影響を小さくするため、Smoothed Deep Metric Learning(SMDL)を提案している。

モデルの概略図は以下の通りで、CNNベースのEncoderでクエリ文を低次元のベクトル空間に変換したのち、kNNを用いてクエリ文に類似した候補を抽出する。

<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/77888151-c1d01a80-72a6-11ea-93d8-2f0bee5edcf2.png">
</p>


従来の損失関数TRでは、anchor question (q^a)とpositive example(q^p)の距離を最小化しつつ、anchor question (q^a)とnegative example(q^p)の距離を最大化するように学習を行っていた。

<p align="center">
<img width="300" src="https://user-images.githubusercontent.com/53220859/77888170-c85e9200-72a6-11ea-8e71-73e0eef4b4b4.png">
</p>

しかし、この損失関数ではノイズデータ(e.g. false-negativeのデータ)影響を受けやすい。そこで、以下のような新しい損失関数SMDLを定義する。この損失関数により、TRによる学習に比べ性能を改善できることを示した。

<p align="center">
<img width="250" src="https://user-images.githubusercontent.com/53220859/77888180-cb598280-72a6-11ea-9692-55029a484bd1.png">
</p>





## 文献情報
- 著者: Daniele Bonadiman, Anjishnu Kumar, Arpit Mittal
- リンク: [https://www.aclweb.org/anthology/D19-5509/](https://www.aclweb.org/anthology/D19-5509/)
- 学会: Proceedings of the 5th Workshop on Noisy User-generated Text (W-NUT 2019)