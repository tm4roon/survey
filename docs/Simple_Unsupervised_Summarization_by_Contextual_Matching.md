# Simple Unsupervised Summarization by Contextual Matching
言語モデルのみを利用したシンプルな教師なしの生成型要約手法を提案。ここでは、Contextual Matching ModelとDomain Fluency Modelの2つの言語モデルを利用して要約文を生成している。生成型要約および抽出型要約の2つのタスクで、提案手法の有用性を示した。

## 文献情報
- 著者: Jiawei Zhou, and Alexander M. Rush
- リンク: [https://arxiv.org/abs/1907.13337](https://arxiv.org/abs/1907.13337)
- 学会: ACL2019
- コード: [https://github.com/jzhou316/Unsupervised-Sentence-Summarization](https://github.com/jzhou316/Unsupervised-Sentence-Summarization)


## 手法
要約では、次の2つの特性を満たしている必要がある。
- 正確性: 元テキストの意味を保持している
- 流暢性: 目的のドメインに関して、文法的に正しく理解可能

これらを本手法では、次式のように定式化する。
<a href="https://www.codecogs.com/eqnedit.php?latex=P({\bf&space;y}|{\bf&space;x})&space;\propto&space;p_{cm}({\bf&space;y}|{\bf&space;x})p_{fm}({\bf&space;y}|{\bf&space;x})^{\lambda}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?P({\bf&space;y}|{\bf&space;x})&space;\propto&space;p_{cm}({\bf&space;y}|{\bf&space;x})p_{fm}({\bf&space;y}|{\bf&space;x})^{\lambda}" title="P({\bf y}|{\bf x}) \propto p_{cm}({\bf y}|{\bf x})p_{fm}({\bf y}|{\bf x})^{\lambda}" /></a>

ここで、<a href="https://www.codecogs.com/eqnedit.php?latex=\bf&space;x" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bf&space;x" title="\bf x" /></a>は入力テキスト、<a href="https://www.codecogs.com/eqnedit.php?latex=\bf&space;y" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bf&space;y" title="\bf y" /></a>は要約文を表す。また、<a href="https://www.codecogs.com/eqnedit.php?latex=p_{cm}({\bf&space;y}|{\bf&space;x})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p_{cm}({\bf&space;y}|{\bf&space;x})" title="p_{cm}({\bf y}|{\bf x})" /></a>は正確性の評価であり、<a href="https://www.codecogs.com/eqnedit.php?latex=p_{fm}({\bf&space;y}|{\bf&space;x})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p_{fm}({\bf&space;y}|{\bf&space;x})" title="p_{fm}({\bf y}|{\bf x})" /></a>は、流暢性の評価を表す (<a href="https://www.codecogs.com/eqnedit.php?latex=\lambda" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\lambda" title="\lambda" /></a>はハイパーパラメータ)。以下で、それぞれの詳細を述べる。また、出力語彙***C***は、元テキストに含まれる語及びベクトル空間上でその近傍にある*k*語 (論文中では、*k*=6)のみに制限している。

### Contextual Matching Model
正確性は、元テキストと要約文の文脈類似度によって評価する。文脈の類似度は、言語モデルの最終出力系列のコサイン類似度によって計算する。ここで、文脈の類似度を<a href="https://www.codecogs.com/eqnedit.php?latex=S(x_{1:m},&space;y_{1:n})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?S(x_{1:m},&space;y_{1:n})" title="S(x_{1:m}, y_{1:n})" /></a>と表すこととする。このとき、<a href="https://www.codecogs.com/eqnedit.php?latex=x_{1:m}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{1:m}" title="x_{1:m}" /></a>, <a href="https://www.codecogs.com/eqnedit.php?latex=y_{1:n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y_{1:n}" title="y_{1:n}" /></a>　はそれぞれ系列長mの入力テキスト、系列長nの要約文を表す。

<p align="center">
<a href="https://www.codecogs.com/eqnedit.php?latex=p_{cm}({\bf&space;y}|{\bf&space;x})&space;=&space;\prod^{N}_{n=1}q_{cm}(y_n|{\bf&space;y_{<n}},&space;{\bf&space;x})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p_{cm}({\bf&space;y}|{\bf&space;x})&space;=&space;\prod^{N}_{n=1}q_{cm}(y_n|{\bf&space;y_{<n}},&space;{\bf&space;x})" title="p_{cm}({\bf y}|{\bf x}) = \prod^{N}_{n=1}q_{cm}(y_n|{\bf y_{<n}}, {\bf x})" /></a>
</p>

実際に生成を行う際には、以下の手順に従う。
1. n=1のとき
   - 出力語彙集合と元テキストの語彙集合との類似度<a href="https://www.codecogs.com/eqnedit.php?latex=s_{\omega}&space;=&space;max_{j\geq&space;1}S(x_{1:j},&space;\omega)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?s_{\omega}&space;=&space;max_{j\geq&space;1}S(x_{1:j},&space;\omega)" title="s_{\omega} = max_{j\geq 1}S(x_{1:j}, \omega)" /></a>を計算する。
   - 出力分布<a href="https://www.codecogs.com/eqnedit.php?latex=q_{cm}(y_{1}=\omega|x)&space;=&space;softmax({\bf&space;s})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?q_{cm}(y_{1}=\omega|x)&space;=&space;softmax({\bf&space;s})" title="q_{cm}(y_{1}=\omega|x) = softmax({\bf s})" /></a>を計算する。
   - <a href="https://www.codecogs.com/eqnedit.php?latex=y_{1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y_{1}" title="y_{1}" /></a>に対応付く元テキストの単語位置 <a href="https://www.codecogs.com/eqnedit.php?latex=z_{1}&space;=&space;argmax_{j\geq&space;1}S(x_{1:j},&space;y_{1})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z_{1}&space;=&space;argmax_{j\geq&space;1}S(x_{1:j},&space;y_{1})" title="z_{1} = argmax_{j\geq 1}S(x_{1:j}, y_{1})" /></a>を求める。
2. n > 1のとき
   - step1と同様に類似度<a href="https://www.codecogs.com/eqnedit.php?latex=s_{w}&space;=&space;max_{j>z_{n-1}}S(x_{1:j},&space;[y_{1:n-1},&space;\omega])" target="_blank"><img src="https://latex.codecogs.com/gif.latex?s_{w}&space;=&space;max_{j>z_{n-1}}S(x_{1:j},&space;[y_{1:n-1},&space;\omega])" title="s_{w} = max_{j>z_{n-1}}S(x_{1:j}, [y_{1:n-1}, \omega])" /></a>を計算する。
   - ただし、<a href="https://www.codecogs.com/eqnedit.php?latex=z_{n-1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z_{n-1}" title="z_{n-1}" /></a>以降の単語しか考慮しない。これは、要約タスクにおける単調性(<a href="https://www.codecogs.com/eqnedit.php?latex=z_{n-1}<z_{n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?z_{n-1}<z_{n}" title="z_{n-1}<z_{n}" /></a>)を仮定しているためである。

3. <a href="https://www.codecogs.com/eqnedit.php?latex=y" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y" title="y" /></a>が元テキストの末尾に対応付くまでstep2を繰り返す。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63256291-3aeba600-c2b2-11e9-9693-0b204d42edc7.png width=400pt>
</p>


### Domain Fluency Model
言語モデル確率を利用して、流暢性の評価を行う。しかしながら、事前学習済みの言語モデルの語彙***V***と出力語彙***C***ではサイズが異なり、適切に言語モデルが計算できない。そこで、Voronoi partitionにより語彙***V***を制約を設けた語彙***C***にマップさせる。ここで、<a href="https://www.codecogs.com/eqnedit.php?latex=y_{n}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y_{n}" title="y_{n}" /></a>のvoronoi cell<a href="https://www.codecogs.com/eqnedit.php?latex={\it&space;N(y_{n})}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{\it&space;N(y_{n})}" title="{\it N(y_{n})}" /></a>をとしたとき、言語モデルは次のように計算される。

<a href="https://www.codecogs.com/eqnedit.php?latex=p_{fm}({\bf&space;y}|{\bf&space;x})&space;=&space;\prod^{N}_{n=1}\sum_{\omega'\in{\it&space;N(y_{n})}}lm(\omega'|{\bf&space;y}_{<n})" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p_{fm}({\bf&space;y}|{\bf&space;x})&space;=&space;\prod^{N}_{n=1}\sum_{\omega'\in{\it&space;N(y_{n})}}lm(\omega'|{\bf&space;y}_{<n})" title="p_{fm}({\bf y}|{\bf x}) = \prod^{N}_{n=1}\sum_{\omega'\in{\it N(y_{n})}}lm(\omega'|{\bf y}_{<n})" /></a>


## Results
教師あり学習のモデルに匹敵する性能を達成。

<p align="center">
<img src=https://user-images.githubusercontent.com/53220859/63333014-9893f700-c373-11e9-885f-785ef1194c58.png width=300pt>
</p>

