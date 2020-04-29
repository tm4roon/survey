# Fully Convolutional Networks for Semantic Segmentation

Semantic Segmentation task(「画像領域を「何が写っているか」によって分割するタスク。ピクセル単位の分類問題。)に対して、CNNのみで構成されたモデルを提案している論文。CNNでは層を重ねるごとに特徴量が抽出されていくが、それに伴い元の位置の情報が薄れてしまう。そこで、本論文ではSkip architecture(前段のCNNの出力を足し合わせる機構)を提案し、位置の情報を補完している。また、学習済みモデルを使うなどして学習の高速化をはかっている。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/79044490-63a91d00-7c40-11ea-9421-de09b48a66ba.png">
</p>

<br>

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/79044494-660b7700-7c40-11ea-9b6a-5dabd0072433.png">
</p>




## 文献情報

- 著者: Jonathan Long, Evan Shelhamer, Trevor Darrell
- リンク: [https://arxiv.org/abs/1411.4038](https://arxiv.org/abs/1411.4038)
- 学会: CVPR2015