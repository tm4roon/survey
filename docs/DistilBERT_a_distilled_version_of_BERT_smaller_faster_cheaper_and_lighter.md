# DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter 
BERTを知識蒸留することにより、軽量化・高速化を図った研究。モデルの性能を97%保ちつつ、モデルサイズを40%、計算速度を60%落とすことに成功。知識蒸留を行う際には、教師モデルの出力分布を教師データとしたsoft target lossに加えて、BERTの学習時の損失関数であるmasked language modeling loss及び隠状態間の差を損失としたcosine embedding lossを加える。


<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/69475701-9084a100-0e13-11ea-8f3b-a4ef44a6e124.png width=450pt>
</p>


## 文献情報
- 著者: Victor Sanh, Lysandre Debut, Julien Chaumond, Thomas Wolf
- リンク: [https://arxiv.org/abs/1910.01108](https://arxiv.org/abs/1910.01108)
- 学会: NeurIPS 2019