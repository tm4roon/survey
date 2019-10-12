# GLOSS: Generative Latent Optimization of Sentence Representations
[Generative Latent Optimization (GLO)](https://arxiv.org/abs/1707.05776)をベースとした教師なし学習の文埋め込みを獲得する手法を提案。モデルは下図のように、Sentence IDによってLatent Vector *z*を獲得し、そこから埋め込みたい文のBack-of-Wordを予測するような構造となっている。推論時には、Latent Vector *z*をランダムに初期化し、reconstruction lossが最小となる*z*を探索する。Semantic Textual Similarityのタスクで、[uSIF](https://pdfs.semanticscholar.org/3fc9/7768dc0b36449ec377d6a4cad8827908d5b4.pdf)を上回る性能を達成。また、Supervised Task(MR, CR, SUBJ, MPQA, TREC)においても、従来の手法に匹敵する性能を達成。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63207375-cb35b980-c0ff-11e9-8e23-24ee92e1ad54.png width=400pt>
</p>

## 文献情報
- 著者: Sidak Pal Singh, Angela Fan, and Michael Auli
- リンク: [https://arxiv.org/abs/1907.06385](https://arxiv.org/abs/1907.06385)
- 学会: arXiv2019
