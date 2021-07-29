# GloVe

The GloVe models for NPVec1 can be found at: https://drive.google.com/drive/folders/1KV5kTHL9N38tQ1p85EqPm5P2NDFfw39W?usp=sharing

To load the models, you'll need [Gensim](https://radimrehurek.com/gensim/). You can install Gensim via pip using `pip install gensim`

Sample code to load GloVe models from Gensim.
```python
from gensim.models.keyedvectors import KeyedVectors

# We have eight models available for GloVe (Kindly refer to the paper)
# (B) -> processed.glove
# (BN) -> processed_normalized.glove
# (BT) -> processed_tokenized.glove
# (BS) -> processed_stemmed.glove
# (BNT) -> processed_normalized_tokenized.glove
# (BNS) -> processed_normalized_stemmed.glove
# (BTS) -> processed_tokenized_stemmed.glove
# (BNTS) -> processed_normalized_tokenized_stemmed.glove

model = "processed.glove"
wv = KeyedVectors.load_word2vec_format(model)

# continue with the word vector...
```
