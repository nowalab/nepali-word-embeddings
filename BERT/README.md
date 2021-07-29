# BERT

The BERT models for NPVec1 can be found at: https://drive.google.com/drive/folders/1TJhur6nsYTpiB348AfsHHIfRhVy1RFaV?usp=sharing

To load the models, you'll need [pyTorch](https://pytorch.org/) and [transformers](https://huggingface.co/transformers/). You can install them both using pip as follows:

```
!pip install --upgrade pytorch
!pip install --upgrade transformers
```

Sample code to load BERT models using pyTorch and Transformers

```python
from transformers import BertModel, BertTokenizer

tokenizer = BertTokenizer.from_pretrained("<specify base directory>/tokenizer")
model = BertModel.from_pretrained("<specify base directory>/bert", output_hidden_states=True)

# continue ...
```
