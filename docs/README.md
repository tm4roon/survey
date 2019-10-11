# Dynamic Data Augmentation for Sentence Rewritings

This code is an implementation of **dynamic data augmentation** for sentence rewriting tasks, such as summarization, grammatical error correction, paraphrase generation, text simplification, and style transfer. The sentence rewriting task needs pairs of an original sentence and a rewritten sentence. The dynamic data augmentation is an expanding training data method, which dynamically generates pseudo-sentences from supervised sentence pairs in the training step. The following data augmentation strategies operate tokens sampled in a sentence. 

- **dropout**: drop tokens (Iyyer et al., 2015; Lample et al., 2017);

- **blank**: replace tokens with a placeholder token (Xie et al., 2017);
- **smooth**: replace tokens with a sample from the unigram frequency distribution over the vocabulary (Xie et al., 2017); 
- **wordnet**:  
- **ppdb**:
- **word2vec**:
- **bert**:



## Installation

This code is depend on the following.

- python==3.6.5
- pytorch1.1.0
- Pytorch-transformers1.2.0

```sh
git clone /path/to/this/repository
cd repository
pip install -r requirements.txt
```



## Models

You can choose either transformer ([Vaswani et al. 2017](https://arxiv.org/abs/1706.03762)) or a translation language model (Khandelwal et al. 2019, Hoang et al. 2019) for sentence rewritings. 

 

![]()

![]()



## Data Augmentation

You can choose a data augmentation strategy, using a combination of a sampling strategy `--sampling-strategy` and a generation strategy `--augmentation-strategy`. If you need to training without data augmentation, please use `--augmentation-strategy base`.

 



### Sampling storategies (`--sampling-storategy`)

This option decides how to sample token's positions in original sentence pairs.

| storategy | description                                                  |
| --------- | ------------------------------------------------------------ |
| random    | randomly sample tokens.                                      |
| uif       | sample tokens from **u**nigram **i**nverse **f**requency distribution. |



### Generation storategies



| storategy | description                                                  |
| --------- | ------------------------------------------------------------ |
| dropout   | drop tokens (Iyyer et al., 2015; Lample et al., 2017);       |
| blank     | replace tokens with a placeholder token (Xie et al., 2017);  |
| smooth    | replace tokens with a sample from the unigram frequency distribution over the vocabulary (Xie et al., 2017); |
| wordnet   |                                                              |
| ppdb      |                                                              |
| word2vec  |                                                              |
| bert      |                                                              |

### 

## Replacing probability scheduling





## Usage





## Options





## References

