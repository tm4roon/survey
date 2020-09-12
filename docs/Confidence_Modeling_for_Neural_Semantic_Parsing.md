# Confidence Modeling for Neural Semantic Parsing

本論文ではSemantic Parsingにおける出力の確信度/不確かさを測る方法として、次の3つの観点に着目している.

- Model: テスト時にもDropoutを利用し、出力分布の摂動を測るなど.
- Data: 入力文の一部にマスクをかけて、その際の出力分布の摂動を測るなど.
- Input: 出力分布の分散やエントロピーを利用して測るなど.

また、不確かさが入力文のどの部分から発生しているのかを出力から逆算する、Uncertainty Backpropagationを提案している. 結果として、アテンション機構を利用するよりもうまく不確かさを検出できる.

[![img](https://user-images.githubusercontent.com/53220859/92985841-5cd54d80-f4f1-11ea-8188-9ce4058a0b3b.png)](https://user-images.githubusercontent.com/53220859/92985841-5cd54d80-f4f1-11ea-8188-9ce4058a0b3b.png)

## 文献情報

- 著者: Li Dong, Chris Quirk, Mirella Lapata
- リンク: https://www.aclweb.org/anthology/P18-1069/
- 学会: ACL2018