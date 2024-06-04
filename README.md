# Toxic Comment Classifier

This is a model that classifies whether the comment is toxic. It is trained on "DistilBERT base model (uncased)" using the wiki-toxic dataset used in "Kaggle Toxic Comment Classification" challenge from 2017/18.

## How to use

### Using Pipeline
The model can be accessed using the "pipeline" function of Huggingface "Transformers" Library.
```python
# Use a pipeline as a high-level helper
from transformers import pipeline

pipe = pipeline("text-classification", model="Ashed00/test_trainer")
```

This can then be accessed using
```python
pipe("Toxic Comment.")
```

### Output
The output will be a dictionary with keys 'label' and 'score'
>Label1 -> Toxic Comment

>Label0 -> Not toxic Comment

>Score -> Probability of that Label.
