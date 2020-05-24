# Enabling Language Models to Fill in the Blanks
単語穴埋めタスクによる新しい言語モデルの学習手法(ILM: infilling by language model)を提案。
短編小説や論文概要, 歌詞などのドメインにおいて、機械が生成したものか判別が困難なレベルに流暢な文を生成することに成功。
従来の単語穴埋めタスクとは異なり、マスクされた文とマスクされたフレーズを[SEP]トークンで連結した物を言語モデルに入力とし、left-to-rightで1単語ずつ生成していく。

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/82147123-a2a64000-9888-11ea-9a86-afccca44549d.png">
</p>


## 文献情報
- 著者: Chris Donahue, Mina Lee, Percy Liang
- リンク: [https://arxiv.org/abs/2005.05339](https://arxiv.org/abs/2005.05339)
- 学会: ACL2020
