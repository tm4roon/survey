# Retrieve, Rerank and Rewrite: Soft Template Based Neural Summarization

生成型要約に関する論文。 入力文とそれに相応しいtemplateの2つを利用して要約文を生成するモデル。 templateを利用することで、より流暢かつ意味のある要約文を生成できるようになった。imformativenessに関して、state-of-the-artの手法よりも優れた結果が得られた。 また、生成される要約文の頑健さと可読性を改善した。 

<br>

提案手法では、次の3ステップで要約文を生成する。 

- Retrieve: 入力文をキーとして、トレーニングコーパスから入力文と類似度の高い上位30文を選択する。 これらの参照文をtemplatesと呼ぶ。
- Rerank: Retrieveで得られたtemplatesをランキングする。 入力文のhidden vectorとtemplateとhidden vectorをBilinear networkに入力して、saliencyを計算する。(教師データは、templateと正解文のROUGEスコア) 

- Rewrite: 入力文とRerankによって得られた最も相応しいtemplateのhidden vectorを利用し、attentionalRNN decoderにより要約文を生成。 

<br>

![re3sum](https://user-images.githubusercontent.com/53220859/63508841-bb5e1100-c515-11e9-8de3-3a4ad95c7dad.png)

※ 図は元論文から引用。

<br>

## 文献情報

- 著者: Ziqiang Cao, Wenjie Li, Furu Wei, and Sujian Li
- リンク: [https://www.aclweb.org/anthology/P18-1015/](https://www.aclweb.org/anthology/P18-1015/)