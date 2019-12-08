# Cross-lingual Pre-training Based Transfer for Zero-shot Neural Machine Translation 

masked language model, translation language modelを応用した事前学習により、zero-shot machine translation (source-pivot, pivot-targetの教師データのみで、source-targetの翻訳を行う)を行なった研究。具体的には、下図の2つの方法によって、事前学習を行う。

<p align="center">
  <img src=https://user-images.githubusercontent.com/53220859/70385276-1be36200-19d0-11ea-8c31-0e4e3ef79cfe.png width=450pt>
</p>

学習としては、事前学習と転移学習の2つのステップに分けられる。事前学習時では、source, pivotの単言語コーパス及び、source-pivotの対訳コーパスを利用する。転移学習時は、pivot-targetの対訳コーパスを利用して学習を行う。




## 文献情報
- 著者: Baijun Ji, Zhirui Zhang, Xiangyu Duan, Min Zhang, Boxing Chen and Weihua Luo 
- リンク: [https://arxiv.org/abs/1912.01214](https://arxiv.org/abs/1912.01214)
- 学会: AAAI2020