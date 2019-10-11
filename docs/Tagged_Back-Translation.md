# Tagged Back-Translation

文頭に逆翻訳によって生成されたことを明示する＜BT＞というタグを挿入し、学習データに追加するTagged Back-Translationを提案。従来の[Noised Back-Translation](https://arxiv.org/abs/1808.09381) (逆翻訳後に単語の並び替えや削除・マスクを行う手法)に比べて、提案手法によりWMT English-Romanian, English-GermanにおいてSoTAを達成。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66637035-440f4880-ec4d-11e9-9704-c7e700624d46.png width=400pt>
</p>

## 文献情報
- 著者: Isaac Caswell, Ciprian Chelba, David Grangier
- リンク: [https://arxiv.org/abs/1906.06442](https://arxiv.org/abs/1906.06442)
- 学会: WMT2019