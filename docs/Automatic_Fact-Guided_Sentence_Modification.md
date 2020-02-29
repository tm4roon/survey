# Automatic Fact-Guided Sentence Modification

Fact-Guided Sentence Modification(ある指示文に従って、文を書き換えるタスク)というタスクを定義し、それを可能にするモデルを提案した研究。ここでは、Wikipediaの編集依頼をもとにWikipediaの古い記事を書き換える。
<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/53220859/75606875-9a195580-5b34-11ea-90c8-7e81960c1540.png">
</p>
<br>

具体的には、次の2つのステップによって行われる。

1. 編集対象となる部分をマスクする。Fact-checkingのデータFEVER(claim-evidenceのペアに対して、"refutes", "not enough information", supports"の3種類のラベルが付与されているデータ) を利用して、分類器を学習させる。その過程でマスク範囲を選択するモデル(Masker)の学習を行う。
<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/75606878-a30a2700-5b34-11ea-9bcf-ce0cfc4ccc6b.png">
</p>

2. 1.によって構築されたMaskerの出力とclaimを入力として、新しい文を生成する。
<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/75606879-a7cedb00-5b34-11ea-94f3-271d53395ba8.png">
</p>


## 文献情報

- 著者: Darsh J Shah, Tal Schuster, Regina Barzilay
- リンク: [https://arxiv.org/abs/1909.13838](https://arxiv.org/abs/1909.13838)
- 学会: AAAI2020