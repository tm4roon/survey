# TABERT: Pretraining for Joint Understanding of Textual and Tabular Data
テーブルデータに基づいた質問応答のタスクにBERTを適用させた研究。モデルは下図に示すように、3つの要素によって構成される。

<p align="center">
  <img width=600 src="https://user-images.githubusercontent.com/53220859/88265034-b6967400-cd07-11ea-925d-15e24485fa83.png">
</p>

(A) 入力された質問文に関連度の高い行の抽出: 質問文と行に含まれる各要素のn-gramの一致度により関連度を計算し、上位n件を学習に利用する。
(B) 質問文と(A)で得られた行の要素を結合してエンコード: 行の要素は、列名・列のタイプ・セルの値の3つを結合する形でエンコードする。

<p align="center">
  <img width=300 src="https://user-images.githubusercontent.com/53220859/88265123-e180c800-cd07-11ea-9c1c-7db8285ca34d.png">
</p>

(C) Vertical self-atttentionで各行の情報を集約。

事前学習はテーブルにマスクをかけて、列名や列のタイプ、セルの値を予測させるマスク単語予測により行う。



## 文献情報

- 著者: Pengcheng Yin, Graham Neubig, Wen-tau Yih, Sebastian Riedel
- リンク: [https://arxiv.org/abs/2005.08314](https://arxiv.org/abs/2005.08314)
- 学会: ACL2020