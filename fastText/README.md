# fastText

The fastText models for NPVec1 can be found at: https://drive.google.com/drive/folders/1UYnw6Kzhll_9kB02it1RJpaWd8FdyM7L?usp=sharing

To load the models, you'll need [Gensim](https://radimrehurek.com/gensim/). You can install Gensim via pip using `pip install gensim`

Sample code to load fastText models from Gensim.
```python
from gensim.models import FastText

# We have eight models available for FastText (Kindly refer to the paper)
# (B) -> processed.fast_text
# (BN) -> processed_normalized.fast_text
# (BT) -> processed_tokenized.fast_text
# (BS) -> processed_stemmed.fast_text
# (BNT) -> processed_normalized_tokenized.fast_text
# (BNS) -> processed_normalized_stemmed.fast_text
# (BTS) -> processed_tokenized_stemmed.fast_text
# (BNTS) -> processed_normalized_tokenized_stemmed.fast_text

model = "processed.fast_text"
wv = FastText.load(model)

# continue with the word vector...
```
