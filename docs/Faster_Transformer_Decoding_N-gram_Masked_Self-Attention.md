# Faster Transformer Decoding: N-gram Masked Self-Attention

Transformerのdecode時に、self-attentionの範囲をn-gramに制限することで計算コストを抑えてdecodeする手法を提案。モデルの性能を損なうことなく、出力時の計算コストを抑えることができる。

<p align="center">
<img src="https://user-images.githubusercontent.com/53220859/72680158-05b1e100-3afa-11ea-8096-0069aff370b0.png" width=500pt>
</p>



## 文献情報

- 著者: Ciprian Chelba, Mia Chen, Ankur Bapna, Noam Shazeer
- リンク: [https://arxiv.org/abs/2001.04589](https://arxiv.org/abs/2001.04589)
- 学会: arXiv