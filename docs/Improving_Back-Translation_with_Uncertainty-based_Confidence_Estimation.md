# Improving Back-Translation with Uncertainty-based Confidence Estimation

逆翻訳において順方向モデルの学習時に、逆方向モデルの確信度(モデルがどれくらいの自信を持ってその文を出力したのか)で重み付けすることにより、品質の良い擬似データを効果的に学習しようという試み。確信度の計算において、word-levelとsentence-levelの2つを採用している。

Word-levelでは、逆方向モデルで得られた単語単位の確信度を順方向モデルのattention weightに重み付けを行う (自信のない単語は、あまり見ないようにする)。

sentence-levelでは、Monte Carlo Dropoutでサンプリングした擬似生成文の出力分布の統計量(ここでは、4種類の統計量をを利用する)を用いて計算し、順方向モデルの損失時に利用する。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/69705333-aefedb00-1138-11ea-8695-d76057a4bb36.png width=500pt>
</p>


## 文献情報

- 著者: Shuo Wang, Yang Liu, Chao Wang, Huanbo Luan, and Maosong Sun
- リンク: [https://www.aclweb.org/anthology/D19-1073/](https://www.aclweb.org/anthology/D19-1073/)
- 学会: EMNLP2019