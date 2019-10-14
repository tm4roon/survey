# Cross-lingual Transfer Learning for Japanese Named Entity Recognition
固有表現抽出タスクにおいて英語→日本語に転移学習させる手法を提案。モデルの構造は、下図に示すBiLSTM (char+word) + CRFであるが、characterを入力する際は、ローマ字に変換したのちに入力する。転移学習及びローマ字化させることにより、有意な改善ができることを示した。また、モデルのどの部分(Character weights, Word weights, Dence weights)を転移学習すべきかを調査している。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63220947-7dd34e00-c1cc-11e9-81d5-992c4dcc61a1.png width=450pt>
</p>


## 文献情報
- 著者: Andrew Johnson, Penny Karanasou, Judith Gaspers, and Dietrich Klakow
- リンク: [https://www.aclweb.org/anthology/N19-2023](https://www.aclweb.org/anthology/N19-2023/)
- 学会: NAACL2019
