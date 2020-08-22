# Building a Semantic Parser Overnight
タイトル通り、「学習データがゼロの状態から一晩でSemantic Parserを構築する」フレームワークを提案した論文。
具体的には、

1. 自分が扱いたいドメインの語彙ルールを追加
2. フレームワーク側で予め用意されている文法ルールで形式表現と自然言語文のペアを生成
3. 生成した自然言語文をクラウドソーシングを利用して言い換え、流暢かつ幅広い表現を網羅する

というような流れで学習データを構築する。
幅広いドメインにおいて、高い性能を発揮するSemantic Parserを構築できることを示した。

<p align="center">
<img width="800" src="https://user-images.githubusercontent.com/53220859/90784022-bfe12380-e33b-11ea-8a24-bb21b46ed9c5.png">
</p>

## 文献情報
- 著者: Yushi Wang, Jonathan Berant, Percy Liang
- リンク: [https://www.aclweb.org/anthology/P15-1129/](https://www.aclweb.org/anthology/P15-1129/)
- 学会: IJCNLP2015
