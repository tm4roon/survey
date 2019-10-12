# Improving Language Understanding by Generative Pre-Training
事前学習済みのTransformer言語モデルを、Text ClassificationやTextual Entailment, Semantic Textual Similarity, Question Answeringなど様々なタスクに適応させる方法を提案。fine-tuningの際は、目的のタスクの損失に加え、言語モデルの損失も計算する。 9つのタスクでstate-of-the-artを達成。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/62632603-b756be80-b96d-11e9-80a3-86fd7f7f784b.png width=600pt>
</p>


## 文献情報
- 著者: Alec Radford, Karthik Narasimhan, Tim Salimans and Ilya Sutskever
- リンク: [https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)
