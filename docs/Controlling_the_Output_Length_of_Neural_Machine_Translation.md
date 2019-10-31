# Controlling the Output Length of Neural Machine Translation
文長制御可能な機械翻訳モデルを提案。次の2つのアプローチによって制御を行う。
- **Length token method**: コーパスを文長に応じて、<short>, <normal>, <long>の3段階に分割する。それぞれのラベルを入力文頭に追加する。
- **Length encoding method**: 出力をする際に、目的の出力文長*len*と現在の出力文長*pos*の差(absolute:*len-pos*, relative:*len/pos*)をpositional embeddingとして入力する。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/67960034-0777b100-fc3d-11e9-9149-a4ed5803075e.png width=600pt>
</p>



## 文献情報
- 著者: Surafel Melaku Lakew, Mattia Di Gangi, Marcello Federico
- リンク: [https://arxiv.org/abs/1910.10408](https://arxiv.org/abs/1910.10408)
- 学会: IWSLT2019