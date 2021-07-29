# Word2Vec

The Word2Vec models for NPVec1 can be found at: https://drive.google.com/drive/folders/1Lq_laJUn1lNkOw8pcv4PJsGi1U3DC_uM?usp=sharing

To load the models, you'll need [Gensim](https://radimrehurek.com/gensim/). You can install Gensim via pip using `pip install gensim`

Sample code to load Word2Vec models from Gensim.
```python
from gensim.models import Word2Vec

# We have eight models available for Word2Vec (Kindly refer to the paper)
# (B) -> processed.word2vec
# (BN) -> processed_normalized.word2vec
# (BT) -> processed_tokenized.word2vec
# (BS) -> processed_stemmed.word2vec
# (BNT) -> processed_normalized_tokenized.word2vec
# (BNS) -> processed_normalized_stemmed.word2vec
# (BTS) -> processed_tokenized_stemmed.word2vec
# (BNTS) -> processed_normalized_tokenized_stemmed.word2vec

model = "processed.word2vec"
wv = Word2Vec.load(model)

# continue with the word vector...
```
