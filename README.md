# Bert-Summarization

## This code based on [Bert Extractive Summarizer](https://github.com/dmmiller612/bert-extractive-summarizer), but it was important for me to get not the summary itself, but the weight for each sentence. 

The result is presented in the form of a pandas DataFrame, which contains information about the sentence index, its weight (the higher the weight, the more important the sentence), the number of the cluster to which it belongs and the sentence itself.

### Example

```
from summarizer import Summarizer

sample_doc = '''Put here any text'''
model = Summarizer()
result = model(sample_doc, min_length=1,max_length=600,ratio=0.1)
//changing the ratio changes the number of clusters
model.df

```

### Result
![Иллюстрация к проекту](https://github.com/alex-romanovskii/Bert-Summarization/blob/main/output.PNG)
