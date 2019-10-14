# Google’s Multilingual Neural Machine Translation System: Enabling Zero-Shot Translation

入力文頭に、「どの言語に翻訳するか」を表すラベルを挿入することで多言語翻訳を実現しようという試み。入力データに変更を加えるだけで、モデル自体は変更していない。WMT2014, 2015のFrench-English, German-EnglishでSoTAを達成。また、様々な言語対を同時に学習させたことにより、少資源の言語対での性能改善やZero-shot translation(e.g. Portugese-Spanishのデータが存在しなくても、Portugese-English, English-Spanishを学習していることにより、Portugese-Spanishの翻訳が可能)を実現。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/66731788-0bad7b80-ee94-11e9-844b-16f5b7339145.png width=450pt>
</p>







## 文献情報

- 著者: Melvin Johnson, Mike Schuster, Quoc V. Le, Maxim Krikun, Yonghui Wu, Zhifeng Chen, Nikhil Thorat
- リンク: [https://arxiv.org/abs/1611.04558](https://arxiv.org/abs/1611.04558)
- 学会: arXiv