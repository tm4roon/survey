# DEFINE: Deep Factorized Input Token Embeddings for Neural Sequence Modeling

ニューラル翻訳モデル・言語モデルにおけるembedding layerのパラメータを圧縮しようという試み。  従来のembedding layerでは、512次元や768次元などのパラメータが選択されていたが、提案しているDEFINEでは、1層目で64次元などの少ない次元を選択し、その後それよりも高い次元へと拡張していく。結果として、モデルの性能を損なうことなく、モデルのパラメータを削減することに成功。


<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/74087040-1982ae80-4acc-11ea-8d9b-1b811d60dbf4.png" width=500>
<img  src="https://user-images.githubusercontent.com/53220859/74087042-1d163580-4acc-11ea-9a90-6bf040f43746.png" width=500>
</p>



## 文献情報

- 著者: Sachin Mehta, Rik Koncel-Kedziorski, Mohammad Rastegari, and Hannaneh Hajishirzi
- リンク: [https://arxiv.org/abs/1911.12385](https://arxiv.org/abs/1911.12385)
- 学会: ICLR2020