# CTRL: A Conditional Transformer Language Model for Controllable Generation

出力制御可能な言語モデルを提案。ドメインを表すラベル(Wikipedia, Book, Legal, ...)を先頭に付与することによって、出力制御可能な言語モデルの学習を行う。生成時には、ラベルとプロンプト(文書の書き出しの数単語)を入力し、次の単語を順次生成する。 このとき、温度付きソフトマックスによりサンプリングを行う。また、単語の繰り返し生成を抑制するため、coverage mechanismを取り入れている。


<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/72045262-088e2400-32f9-11ea-9049-8ca08608d7a8.png width=500pt>
</p>

<br>

ドメインを表すラベル以外にも、次のようにラベルとプロンプトを入力することにより、質問応答や翻訳タスクを行うことも可能である。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/72045316-23609880-32f9-11ea-9540-bcb77a4dae92.png width=500pt>
</p>


## 文献情報

- 著者: Nitish Shirish Keskar, Bryan McCann, Lav R. Varshney, Caiming Xiong, Richard Socher
- リンク: https://arxiv.org/abs/1909.05858
- 学会: arXiv