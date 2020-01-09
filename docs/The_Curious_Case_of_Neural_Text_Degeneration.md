# The Curious Case of Neural Text Degeneration

テキスト生成タスクにおいて、機械による生成と人間による生成の違いについて調査し、より人間に近い生成方法について提案している論文。  生成時に広く用いられているBeam searchにおいて単語の繰り返しが発生してしまう原因や、full distributionからのサンプリングによって好ましくない生成が行われてしまう原因について言及している。本論文で提案している、累積確率に基づいて生成する単語をサンプリングするNucleus samplingにより、人間に近い生成を行うことが可能である。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/72047271-848a6b00-32fd-11ea-8259-72ef0559c049.png width=600pt>
</p>

## 文献情報

- 著者: Ari Holtzman, Jan Buys, Maxwell Forbes, Yejin Choi
- リンク: [https://arxiv.org/abs/1904.09751](https://arxiv.org/abs/1904.09751)
- 学会: arXiv