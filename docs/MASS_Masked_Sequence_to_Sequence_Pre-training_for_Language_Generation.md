# MASS: Masked Sequence to Sequence Pre-training for Language Generation
BERTの事前学習をEncoder-Decoderモデルに拡張した研究。BERTやGPTのような言語モデルの学習はEncoder及びDecoderのみの学習した出来なかった(Figure.2)。ここでは、入力文のある範囲をマスクした状態でエンコードし、その部分に入る語を予測するというタスクを解かせる事前学習を行う(Figure.1)。これにより、翻訳や要約、対話応答生成などの3つのタスク(8つのデータセット)で、性能を改善した。

### Masked language modeling in BERT, Standard language modeling
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66794457-8cc04d80-ef3c-11e9-96b2-ac95b6fa6bd2.png width=800pt>
</p>


### Masked sequence-to-sequence pre-training
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66794458-8cc04d80-ef3c-11e9-8305-04dfd9b4b077.png width=500pt>
</p>


## 文献情報
- 著者: Kaitao Song, Xu Tan, Tao Qin, Jianfeng Lu, Tie-Yan Liu
- リンク: [https://arxiv.org/abs/1905.02450](https://arxiv.org/abs/1905.02450)
- 学会: ICML2019