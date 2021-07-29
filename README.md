# NPVec1: Word Embeddings for Nepali - Construction and Evaluation

## Introduction
We present NPVec1, which consists of 25 state-of-art Word Embeddings for Nepali that we have derived from a large corpus using GloVe, Word2Vec, fastText, and BERT. These models are trained using 279 million word tokens and are the largest Embeddings ever trained for Nepali language. 

(Read our paper at: https://aclanthology.org/2021.repl4nlp-1.18.pdf)

(Read our poster at: https://drive.google.com/file/d/14WIAd9tyxt6zofAuKjqt9NerF03qWwi1/view?usp=sharing)

(Video recordings of our presentation: https://drive.google.com/file/d/1zxi8Rf_-4LCumrRiorQJqkrcCg73qmL9/view?usp=sharing)


## Corpus
Our base corpus consists of a deduplicated mixture of news, Wikipedia articles, and OSCAR:

| Corpus | Tokens | Types | Genre | Description |
|--|--|--|--|--|
|Our News Corpus | 216M | 3.3M | News | Online news |
| Lamsal (Lamsal, 2020) | 58.8M | 1.2M | News | Online news |
|OSCAR (Ortiz Suárez et al., 2019) | 71.8M | 2.2M | Mixed | Mixed Genre |
| Wikipedia (Gaurav, 2020) | 5.1M | 0.3M | Mixed | Mixed Genre |

## Preprocessing

We apply following preprocessing schemes: Normalization, Tokenization and Stemming.

### Normalization
There are different written sounds in Nepali which, when spoken, are indistinguishable from each other. For example: the two different words नेपाली (Nepali) and नेपालि are spoken the same way even though their written representations differ. Thus, people often mistakenly use multiple written version of the same words which introduces noise in the data set. Normalization, in the context of this study, is identification of all these nuances and mapping them to a same word.

### Tokenization
Nepali language has multiple post-positional and agglutinative suffixes like ले, मा, बाट, देखि etc. which can be compounded together with nouns and pronouns to produce new words. For example, the word नेपाली (Nepalese) can be compounded as नेपालीले (Nepalese did), नेपालीहरु (Nepalese+plural), नेपालीको (Of Nepalese), so on and so forth. Thus, these different words can be tokenized as नेपाली + ले, नेपाली + हरु, नेपाली + को which serves to drastically reduce the vocabulary size without the loss of any linguistic functionality.

### Stemming
There are also other case markers and bound suffixes that primarily inflect verbs to produce new words. For example, from the same root word खा (eat), words such as खायो (ate), खाँदै(eating), खाएको (had eaten), खाएर (after eating), etc can be constructed. Stemming, in this context, means the reduction of all such inflected words to their base forms

## Preprocessed Corpus
After applying the preprocessing schemes in the specified order, we obtain the following eight datasets. 
|Preprocessing Scheme | Code | #Tokens | #Types |
|--|--|--|--|
|Base |(B) |279M |3.14M|
|Base+Normalized |(BN)| 279M |2.6M|
|Base+Normalized+Tokenized| (BNT)| 360M |1.4M|
|Base+Normalized+Stemmed |(BNS)| 279M |2.04M|
|Base+Normalized+Tokenized+Stemmed |(BNTS)| 359M |1.09M|
|Base+Tokenized |(BT) |357M |1.8M|
|Base+Tokenized+Stemmed |(BTS) |357M |1.4M|
|Base+Stemmed |(BS) |279M| 2.5M|


June 7, 2021: 
We are uploading models at the moment. Once it is completed, we will update this with the links for the 25 Word Embeddings for Nepali.  

January, 2021:
Our paper is currently in review. This repository will contain 25 Word Embeddings for Nepali. We will publish the models soon.
