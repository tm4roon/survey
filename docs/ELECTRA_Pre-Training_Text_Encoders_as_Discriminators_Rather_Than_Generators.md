# ELECTRA: Pre-Training Text Encoders as Discriminators Rather Than Generators
効率的な事前学習手法ELECTRA:*E*fficiently *L*earning an *E*ncoder that *C*lassifies *T*oken *R*eplacements *A*ccuratelyを提案した論文。Masked Language Modelでは、マスクした部分しか学習できないので非常に非効率である。そこで、Generative Adversarial Networkのアイデアを応用して、Replaceing Token Detection (置き換えられた単語かどうかの二値分類タスク)による事前学習を導入する。具体的なモデルの構成は以下の図に示す通り。

<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/53220859/76696808-a70c7c00-66d2-11ea-9abf-de82991cf8b9.png">
</p>

結果として、RoBERTaやXLNet等 に比べて学習時間を1/4に短縮。なおかつ、それらのモデルの性能を上回ることができることを示した。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/76696809-a8d63f80-66d2-11ea-9c24-7e33f865b989.png" width="500">
</p>


## 文献紹介

- 著者: Kevin Clark, Minh-Thang Luong, Quoc V. Le, Christopher D. Manning
- リンク: [https://openreview.net/forum?id=r1xMH1BtvB](https://openreview.net/forum?id=r1xMH1BtvB)
- 学会: ICLR2020
- GitHub: [https://github.com/google-research/electra](https://github.com/google-research/electra)



## 解説記事

- [Efficient NLP Model Pre-training with ELECTRA - Google AI Blog](http://ai.googleblog.com/2020/03/more-efficient-nlp-model-pre-training.html)
- [「ELECTRA」新たな自然言語処理モデルが示したMLMの問題点とは？](https://ai-scholar.tech/treatise/electra-ai-382/)