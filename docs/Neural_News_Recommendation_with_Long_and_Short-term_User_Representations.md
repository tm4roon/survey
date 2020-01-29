# Neural News Recommendation with Long- and Short-term User Representations

ニュース記事推薦の研究。ユーザの長期的な嗜好と短期的な興味の両方を考慮した、ユーザのベクトル化手法を提案。モデルは(1) News encoder (2) User encoderの2つのコンポーネントにより構成される。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/73257739-a6458680-4207-11ea-9861-74aa5b180ce5.png" width=400pt>
</p>

User encoderでは、(1) long-term user representationをshort-term user representationに利用するGRUの初期値として導入する方法 (2) long-term user representationとshort-term user representationを結合する方法のの2つが提案されている。

long-term user representationは、User IDのembedding layerにより獲得。short term user representationは、ユーザのブラウジング履歴を利用し、news encoder + GRUにより獲得。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/73257740-a6458680-4207-11ea-8f95-73d4eeba1c91.png" width=600pt>
</p>


## 文献情報

- 著者: Mingxiao An, Fangzhao Wu, Chuhan Wu, Kun Zhang, Zheng Liu, Xing Xie
- リンク: [https://www.aclweb.org/anthology/P19-1033/](https://www.aclweb.org/anthology/P19-1033/)
- 学会: ACL2019