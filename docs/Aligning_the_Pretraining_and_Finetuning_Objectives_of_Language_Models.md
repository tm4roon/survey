# Aligning the Pretraining and Finetuning Objectives of Language Models

BERTの事前学習で利用されている、masked language model (MLM)とnext sentence prediction(NSP)の代替となる事前学習手法を提案し、concept-of-interest taggingとacronym detectionタスクにおいて、より少ないデータでも効果的にfinetuningできることを示した。ここで提案している事前学習手法は次の2つ。

- Wikipedia hyperlink prediction: concept-of-interest taggingのための事前学習

- Pseudo acronym detection: acronym detectionのための事前学習

  

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/74219609-a4dc8980-4cf0-11ea-8925-78584343e544.png" width=800>
</p>



## 文献情報

- 著者: Nuo Wang Pierse,  Jingwen Lu
- リンク: [https://arxiv.org/abs/2002.02000](https://arxiv.org/abs/2002.02000)
- 学会: arXiv