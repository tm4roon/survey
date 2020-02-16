# LayoutLM: Pre-training of Text and Layout for Document Image Understanding
BERTに、文書の画像情報のembedding(image embedding)と2次元のPositinal embeddingを新たに導入することで文書の視覚的情報を考慮した事前学習を行うモデル(LayoutLM)を提案。 事前学習には、Masked visual language modeling task(BERTのマスク単語予測と同じ)とMulti-label document Classificationの2つを利用する。

以下の3つのタスクでLayoutLMの効果を検証。
- Form Understanding
- Receipt Understanding
- Document Image Classification

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/74586169-45e87e80-5028-11ea-9740-6d5b5d148702.png" width=500pt>
</p>


## 文献情報
- 著者: Yiheng Xu, Minghao Li, Lei Cui, Shaohan Huang, Furu Wei, Ming Zhou
- リンク: [https://arxiv.org/abs/1912.13318](https://arxiv.org/abs/1912.13318)
- 学会: arXiv