# End-to-end Sequence Labeling via Bi-directional LSTM-CNNs-CRF


系列ラベリングの際に広く利用されるBiLSTM-CNN-CRFを提案している論文。CNNにより生成されたcharacter-embeddingとword embeddingを結合し、BiLSTMに入力。その後、BiLSTMの出力をCRFに入力しラベルを生成する、といったモデルの構成。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/78683759-a8744180-792a-11ea-85e6-96b4124d0eb3.png">
</p>


In-vocabulary(IV), Out-of-training-vocabulary(OOTV), Out-of-embedding-vocabulary(OOEV), Out-of-both-vocabulary(OOBV)それぞれに関して評価を行っている。character-embeddingを導入しているからか、OOTVであっても高い性能を達成することができる。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/78683818-b924b780-792a-11ea-9c9a-673871fe390c.png">
</p>





## 文献情報

- 著者: Xuezhe Ma, Eduard Hovy
- リンク: [https://www.aclweb.org/anthology/P16-1101/](https://www.aclweb.org/anthology/P16-1101/)
- 学会: ACL2016