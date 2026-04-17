# 🌍 Yoruba → English Sequence-to-Sequence Translation Model


This project demonstrates a **Sequence-to-Sequence (Seq2Seq) neural network** for translating Yoruba sentences into English using deep learning.

It was built to understand how encoder-decoder architectures work using GRU-based recurrent neural networks.

---

# 🧠 What is this project about?

This project builds a model that learns:

> Yoruba sentence → English sentence

Instead of memorizing translations, the model learns patterns between languages using a neural network.

---

# ⚙️ How it works (High-Level)

The model follows the Seq2Seq architecture:

Input Sentence (Yoruba)
↓
Encoder (GRU)
↓
Context Vector (compressed meaning)
↓
Decoder (GRU)
↓
Output Sentence (English)


---

# 🧩 Key Concepts Used

## 1. Sequence-to-Sequence (Seq2Seq)
A model that converts one sequence into another sequence.

Examples:
- Yoruba → English translation
- Text summarization
- Chatbots

---

## 2. Encoder-Decoder Architecture
- **Encoder**: Reads and understands the input sentence
- **Decoder**: Generates the output sentence step-by-step

---

## 3. GRU (Gated Recurrent Unit)
A type of recurrent neural network that helps the model remember important information in sequences.

Used in both encoder and decoder.

---

## 4. Embedding Layer
Converts words into dense numerical vectors so the model can understand meaning.

---

## 5. Teacher Forcing (Training Concept)
During training, the correct previous word is used to improve learning stability.

---

# 🧪 Dataset

A small custom dataset of Yoruba-English sentence pairs:

Example:

| Yoruba | English |
|--------|--------|
| mo n lo si ile | i am going home |
| inu mi dun | i am happy |
| o n jeun | he is eating |

---

# 🏗️ Model Architecture

```

Encoder:
Embedding → GRU → Context Vector

Decoder:
Embedding → GRU → Dense (Softmax)

```

---

# 📦 Requirements

```bash
tensorflow
numpy
```

---

# 🚀 How to run

```bash
# Clone the repository
git clone https://github.com/your-username/yoruba-english-seq2seq.git

# Navigate into the folder
cd yoruba-english-seq2seq

# Run the script
python model.py
```

---

# 📊 Training

The model is trained using:

```python
model.fit(
    [yoruba_input, english_input],
    english_output,
    epochs=200
)
```

Loss function used:
- Sparse Categorical Crossentropy

Optimizer:
- Adam

---

# 🧠 Key Insight

> The model does not “translate like a human” — it learns statistical patterns between sentence structures in two languages.

---

