# Clustering of Deep Contextualized Representations for Summarization of Biomedical Texts

医療テキストの抽出型要約。入力テキストを文単位に分割して、BERTに入力。トークンの平均ベクトルを文ベクトルとみなして、文をクラスタリングする。下記のwithin-cluster scoreが上位の文を抽出して、要約文を生成する。

![biotextsum](https://user-images.githubusercontent.com/53220859/64122706-54760d00-cddd-11e9-8807-ef55b7b843d2.png)



- within-cluster score

![within-cluster score](https://user-images.githubusercontent.com/53220859/64122796-8b4c2300-cddd-11e9-93ce-2e6175365167.png)



## 文献情報

- 著者: Milad Moradi, Matthias Samwald
- リンク: [https://arxiv.org/abs/1908.02286](https://arxiv.org/abs/1908.02286)