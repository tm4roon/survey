# Variational Pretraining for Semi-supervised Text Classification

言語資源が限られている場合でも、軽量かつ高性能を実現する事前学習方法(VAMPIRE)を提案。ELMoやBERTでは単語を予測されるタスクによって事前学習を行うが、ここでは、単語の頻度を予測させる事前学習を行う。VAEによって得られたベクトルを単語ベクトルに組み合わせることで後段のタスクの学習を行う。


<p align="center">
<img  src="https://user-images.githubusercontent.com/53220859/74027606-db15c280-49eb-11ea-949a-3a2310bdc47e.png" width=400>
</p>

## Results
データが小規模な場合でも、大きく性能を伸ばしている。また、ELMoに比べて、非常に高速に学習できることがわかる。

<p align="center>
<img src="https://user-images.githubusercontent.com/53220859/74027632-de10b300-49eb-11ea-8e23-ae3c73f30ed5.png" width=500>
<img src="https://user-images.githubusercontent.com/53220859/74027636-df41e000-49eb-11ea-9370-3b468b965c60.png" width=500>
</p>















## 文献情報

- 著者: Suchin Gururangan, Tam Dang, Dallas Card, Noah A. Smith
- リンク: [https://www.aclweb.org/anthology/P19-1590/](https://www.aclweb.org/anthology/P19-1590/)
- 学会: ACL2019