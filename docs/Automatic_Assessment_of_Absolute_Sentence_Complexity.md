# Automatic Assessment of Absolute Sentence Complexity
文の難易度推定を行うためのデータセット(文難易度:5段階評価)と、教師なしの難易度推定器を構築した。教師なしの難易度推定器では、(unigram, bigram, trigram)が出現する(各レベルのおける相対度数, 最も高い難易度, 最も低い難易度)の組み合わせにおいて、以下の8種類の特徴量を利用。また、文長も特徴量として加え、合計で73種類の特徴量を用いて、Random Forestにより難易度の推定を行う。結果として、教師ありの難易度推定手法を上回る結果を達成。また、人手評価と相関のある57種類のみで、73種類使用した場合と同等程度の性能を達成できることを示した。

<p align='center'>
<img src=https://user-images.githubusercontent.com/53220859/67774665-23dee680-faa1-11e9-8883-509340d3e145.png width=400pt>
</p>

\* PCL: **P**hrase **C**omplexity **L**evel

## 文献情報
- 著者: Sanja Stajner, Simone Paolo Ponzetto, Heiner Stuckenschmidt
- リンク: [https://www.ijcai.org/proceedings/2017/572](https://www.ijcai.org/proceedings/2017/572)
- 学会: IJCAI2017