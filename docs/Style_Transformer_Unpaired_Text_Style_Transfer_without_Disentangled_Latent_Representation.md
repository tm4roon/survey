# Style Transformer: Unpaired Text Style Transfer without Disentangled Latent Representation
教師データとなる(入力文, 変換先スタイル, 変換後の文)のペアを必要としないスタイル制御モデルを提案。ある文のスタイルを判定するdisciminatorとスタイル変換を担うstyle transformerを用いて敵対的学習を行う。結果として、スタイルを適切に変換しつつ、内容や流暢性においても高い評価を獲得している。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304837-3d503f00-240f-11ea-9e9f-e3a481f99380.png width=300pt>
</p>


## 文献情報
- 著者: Ning Dai, Jianze Liang, Xipeng Qiu∗, Xuanjing Huang
- リンク: [https://www.aclweb.org/anthology/P19-1601/](https://www.aclweb.org/anthology/P19-1601/)
- 学会: ACL2019

## 手法 (Methods)
### Discreminator Learning
スタイルが2種類しか存在しない場合は、入力文xとそのスタイルsが一致しているかどうかを予測。スタイルが複数ある場合は、入力文xがどのスタイルに対応するのかを予測する。アルゴリズムの流れは以下の通り。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304898-f6af1480-240f-11ea-8658-667bbcf94309.png width=350pt>
</p>

損失関数は以下。
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304907-11818900-2410-11ea-9c6b-cff3114f01cf.png width=350pt>
</p>


### Style Transformer Learning
(入力文, その文のスタイル)のペアを用いて、入力文を復元する損失関数(self reconstruction loss), 入力文を別なスタイルに変換したのち、それを元のスタイルに戻すことによる損失関数(cycle reconstruction loss)及び、スタイル制御ができているかどうかに関する損失関数(style controlling loss)を用いて、学習を行う。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304986-f3685880-2410-11ea-9e32-f99310d9e469.png width=350pt>
</p>

- self construction loss
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304905-0595c700-2410-11ea-8da4-2cc10bc919a7.png width=350pt>
</p>

- cycle reconstruction loss
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304904-04fd3080-2410-11ea-89a0-695e5d16a490.png width=350pt>
</p>

- style controlling loss
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304903-04fd3080-2410-11ea-9992-f5a138412346.png width=350pt>
<img src=https://user-images.githubusercontent.com/53220859/71304902-04fd3080-2410-11ea-9de1-96e4ec6733fb.png width=350pt>
</p>

### Training algorithm
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304985-f3685880-2410-11ea-8dc2-6d5e079b57ec.png width=350pt>
</p>


## 結果
### 人手評価
- style: どの文が元の文と反対の意味になっているか
- content: どの文が元の文の内容を保持しているか
- fluency: 流暢な文はどれか

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304967-b0a68080-2410-11ea-80d6-7fade6e2f8ce.png>
</p>

### Ablation study

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/71304966-b0a68080-2410-11ea-9af2-f1aa066d81dd.png width=350pt>
</p>



## コメント (Comments):