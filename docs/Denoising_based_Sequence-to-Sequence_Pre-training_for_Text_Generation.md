# Denoising based Sequence-to-Sequence Pre-training for Text Generation

ノイズ除去タスクを事前学習させることによって、モデルに変更を加えることなく、要約や文法誤りタスクの性能を改善。従来は、BERTやGPTのように、Seq2SeqのEncoder側及びDecoder側のみに対応する事前学習を行なっていた。ここでは、EncoderとDecoderを同時に学習させるために、ノイズ(単語の削除・置換・並び替え)を加えた文を入力として、元の文を復元するタスクを事前学習に用いる。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66696840-703ccf00-ed0a-11e9-9a88-cbad70b5ed00.png width=600pt>
</p>



## 文献情報

- 著者: Liang Wang, Wei Zhao, Ruoyu Jia, Sujian Li and Jingming Liu
- リンク: [https://arxiv.org/abs/1908.08206](https://arxiv.org/abs/1908.08206)
- 学会: EMNLP-IJCNLP2019