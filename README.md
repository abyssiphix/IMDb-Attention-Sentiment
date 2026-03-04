# IMDb Sentiment Classification with BiLSTM + Attention

This project explores the use of attention mechanisms for sentiment classification on the IMDb movie review dataset.

The goal is to investigate whether adding an attention mechanism to a BiLSTM model can improve classification performance and provide better interpretability.

---

## Dataset

- Dataset: IMDb Movie Review Dataset
- Task: Binary sentiment classification (positive / negative)
- Input: Movie review text
- Output: Sentiment label

---

## Model Architecture

### Baseline Model

BiLSTM with mean pooling.

Text
↓
Embedding
↓
BiLSTM
↓
Mean Pooling
↓
Linear
↓
Prediction

### Attention Model

BiLSTM with additive attention.

Text
↓
Embedding
↓
BiLSTM
↓
Attention
↓
Weighted Sum
↓
Classifier


Attention weights allow the model to focus on important tokens.

---

## Experimental Setup

To ensure fair comparison:

- Fixed train/test subset
- Multiple random seeds
- Same training configuration

---

## Results

| Model | Accuracy |
|------|------|
| BiLSTM | 0.8561 |
| BiLSTM + Attention | 0.8595 |

Attention provides a small but consistent improvement (~0.34%).

---

## Attention Visualization

The attention mechanism highlights important sentiment words.

Positive example:

- acting
- story
- touching

Negative example:

- terrible
- boring
- plot

This shows that the model focuses on sentiment-related tokens.

---

## Technologies

- Python
- PyTorch
- HuggingFace Tokenizer
- Google Colab

---

## Future Work

Possible improvements:

- Transformer models
- Pretrained models (BERT)
- Larger datasets

---

## Author

Xu Zetao
