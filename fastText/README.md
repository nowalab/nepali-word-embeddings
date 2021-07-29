# fastText

The fastText models for NPVec1 can be found at: https://drive.google.com/drive/folders/1UYnw6Kzhll_9kB02it1RJpaWd8FdyM7L?usp=sharing

To load the models, you'll need [Gensim](https://radimrehurek.com/gensim/). You can install Gensim via pip using `pip install gensim`

Sample code to load fastText models from Gensim.
```python
from gensim.models import FastText

# We have eight models available for FastText (Kindly refer to the paper)
# (B) -> processed
# (BN) -> processed_normalized
# (BT) -> processed_tokenized
# (BS) -> processed_stemmed
# (BNT) -> processed_normalized_tokenized
# (BNS) -> processed_normalized_stemmed
# (BTS) -> processed_tokenized_stemmed
# (BNTS) -> processed_normalized_tokenized_stemmed

model = "processed"
wv = FastText.load(model)

# continue with the word vector...
```
