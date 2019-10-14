# Domain Control for Neural Machine Translation

機械翻訳において、学習データと異なるドメインのテストデータに用いた場合には、性能が低い傾向にある。ここでは、学習データのドメインを文末にタグとして挿入する手法と、ドメイン埋め込みを導入し、token-levelでモデルに入力する手法の2つを用いて翻訳性能の改善を試みている。各ドメインのコーパス単体で学習させたモデルよりも、あらゆるドメインを同時に学習させたモデルの方が、全てのドメインで高い性能を達成した。また、ドメインタグを挿入するよりも、ドメイン埋め込みを用いた方が性能を改善できることを示した。

### ドメインタグ
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66733011-0acb1880-ee99-11e9-8b53-caaf88cc4c40.png width=450pt>
</p>

### ドメイン埋め込み
<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66733010-0acb1880-ee99-11e9-92e0-c7c5b6a5983b.png width=450pt>
</p>

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66733070-52ea3b00-ee99-11e9-8b05-65a92b4e3724.png width=300pt>
</p>

## 文献情報

- 著者: Catherine Kobus, Josep Crego,  Jean Senellart
- リンク: [https://arxiv.org/abs/1612.06140](https://arxiv.org/abs/1612.06140)
- 学会: RANLP2017