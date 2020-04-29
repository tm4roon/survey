# TransferTransfo: A Transfer Learning Approach for Neural Network Based Conversational Agents

GPTを対話応答タスクに適応させる手法を提案。ここでは、Persona chat (対話応答のペアと同時に、話者の人格を表す情報が付与されている)データセットを用いて検証している。GPTを対話応答タスクに適応させる際には、対話文脈に加えて、話者のPersona情報も連結する形で入力している。また、BERTのNext Sentence Predicitonのように、最後の発話が文脈に沿ったものかどうかの二値分類を学習に追加している。結果として、SOTAを達成。


<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/80562825-daf1f580-8a23-11ea-9e9e-6901ca098e62.png">
</p>

<br>

## 文献情報

- 著者: Thomas Wolf, Victor Sanh, Julien Chaumond & Clement Delangue
- リンク: [https://arxiv.org/abs/1901.08149](https://arxiv.org/abs/1901.08149)
- 学会: NeurIPS2018 Workshop