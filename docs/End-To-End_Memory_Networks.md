# End-To-End Memory Networks

Memory Networkを提案した論文。bAbi taskを対象として実験を行なっている。これは、人が部屋の中で行動した事実が自然文で与えられ、それに対する質問に答えるタスクである。以下に示すのが、このタスクの例である。回答は1単語で与えられる。

<p align="center">
  <img width="600" src="https://user-images.githubusercontent.com/53220859/80935224-a658b200-8e06-11ea-9cb1-92c2f6d6341e.png">
</p>


<br>
提案しているMemory Networkの概略図を以下に示す。知識源と質問文をEmbedding A, Bでベクトルm, uに変換し、それらの内積をとりSoftmaxをかけ、ベクトルpを獲得する (類似ベクトルを検索?)。また、知識源を別なEmbedding Cによりベクトルに変換し、ベクトルpにより重み付けを行いベクトルoを獲得 (回答情報の埋め込み?)。oとuを足し合わせてWをかけ(答えを選択?)回答を予測する。

<p align="center">
<img width="600" src="https://user-images.githubusercontent.com/53220859/80935222-a48eee80-8e06-11ea-8fc9-a8e7eb079b24.png">
</p>



## 文献情報

- 著者: Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston, Rob Fergus
- リンク: [https://arxiv.org/abs/1503.08895](https://arxiv.org/abs/1503.08895)
- 学会: NIPS2015