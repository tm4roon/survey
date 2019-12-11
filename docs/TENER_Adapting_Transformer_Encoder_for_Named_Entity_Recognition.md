# TENER: Adapting Transformer Encoder for Named Entity Recognition
Transformerのencoderを固有表現抽出に適用させたモデルを提案。  単語レベルの特徴量(word embedding layer)の他に文字レベルの特徴量(CNN layer)を取り入れる。また、従来の方法と同様に、Transformer layerの上にCRFを導入している。  

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/70592169-327df900-1c1c-11ea-8fcc-1ecac8bac11a.png width=300pt>
<img src=https://user-images.githubusercontent.com/53220859/70592173-3578e980-1c1c-11ea-9326-4d0936245ed3.png width=500pt>
</p>

## 文献情報
- 著者: Hang Yan, Bocao Deng, Xiaonan Li, Xipeng Qiu
- リンク: [https://arxiv.org/abs/1911.04474](https://arxiv.org/abs/1911.04474)
- 学会: arXiv