# Simple Unsupervised Keyphrase Extraction using Sentence Embedding

教師なしのキーフレーズ抽出手法を提案。文書ベクトルとフレーズベクトルを同じベクトル空間上にマップし、以下の2つの方法でキーフレーズ候補をランキングする。
- 文書ベクトルとフレーズベクトルのコサイン類似度 (EmbedRank)
- EmbedRank + 抽出されたキーフレーズ中の多様性を考慮 (EmbedRank++)

多様性を考慮することにより、ユーザによる評価において、高いスコアを獲得。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63406315-7a3a0400-c424-11e9-9a5b-60df4595421c.png width=800pt>
</p>

## 文献情報
- 著者: Kamil Bennani-Smires, Claudiu Musat, Andreaa Hossmann, Michael Baeriswyl, and Martin Jaggi
- リンク: [https://arxiv.org/abs/1801.04470](https://arxiv.org/abs/1801.04470)
- 学会: CoNLL2018
