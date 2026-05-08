# Mini LLM From Scratch

A beginner-friendly **Mini Language Model (LLM)** built completely from scratch using **PyTorch** and trained on the **WikiText-2 dataset**.  
This project demonstrates the core working principles behind modern Large Language Models such as tokenization, embeddings, transformers, attention mechanisms, and text generation.

---

## Features

- Character-level tokenization
- Transformer-based GPT-lite architecture
- Text generation using neural networks
- Training on real-world dataset (WikiText-2)
- Flask web application interface
- Real-time training progress updates
- Save and load model weights
- Beginner-friendly and fully commented code

---

## Tech Stack

- Python
- PyTorch
- Flask
- HuggingFace Datasets
- HTML/CSS/JavaScript

---

## Project Structure

```bash
Mini-LLM-From-Scratch/
│── app.py
│── mini_llm_from_scratch.py
│── mini_llm_weights.pt
│── requirements.txt
│── templates/
│    └── index.html
│── static/
│    ├── style.css
│    └── script.js
│── README.md
```

---

# How It Works

The project follows the complete language model pipeline:

```text
Dataset → Tokenization → Encoding → Training → Prediction → Text Generation
```

---

## 1. Dataset Loading

The WikiText-2 dataset is loaded using the HuggingFace `datasets` library.

```python
dataset = load_dataset("wikitext", "wikitext-2-raw-v1")
```

---

## 2. Character-Level Tokenization

Each unique character is converted into a vocabulary index.

Example:

| Character | Token |
|---|---|
| a | 0 |
| b | 1 |
| c | 2 |

---

## 3. Encoding

Text is converted into numerical tensors so PyTorch can process it.

Example:

```text
hello
```

↓

```python
[7, 4, 11, 11, 14]
```

---

## 4. Training

The model learns by predicting the next character in a sequence.

Example:

| Input | Target |
|---|---|
| h | e |
| e | l |
| l | l |
| l | o |

The loss function measures prediction errors, and backpropagation updates model weights.

---

## 5. Text Generation

After training, the model generates text one character at a time.

Example:

```text
Input:
Artificial intelligence

Output:
Artificial intelligence is becoming one of the...
```

---

# Model Architecture

This project includes:

## Bigram Language Model
A simple next-character prediction model.

## GPT-lite Transformer Model
Implemented using:
- Self Attention
- Multi Head Attention
- Feed Forward Networks
- Layer Normalization
- Positional Embeddings

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Rupesh5151/Character-Level-Transformer-Language-Model.git
cd Mini-LLM-From-Scratch
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Run the Project

## Run Training Script

```bash
python mini_llm_from_scratch.py
```

---

## Run Flask Web App

```bash
python app.py
```

Then open:

```text
http://127.0.0.1:5000
```

---

# API Endpoints

| Endpoint | Description |
|---|---|
| `/api/train` | Start model training |
| `/api/status` | Get training progress |
| `/api/generate` | Generate text |
| `/api/save` | Save model weights |

---

# Example Output

```text
Input:
The future of AI

Generated Output:
The future of AI is becoming more powerful and useful...
```

---

# Hyperparameters

| Parameter | Value |
|---|---|
| Batch Size | 32 |
| Block Size | 64 |
| Learning Rate | 3e-4 |
| Max Iterations | 5000 |
| Embedding Dimension | 128 |

---

# Future Improvements

- Implement full GPT architecture
- Add word-level tokenization
- Train on larger datasets
- Add beam search generation
- Deploy on cloud
- Create chatbot interface
- Add model fine-tuning support

---

# Learning Outcomes

This project helps in understanding:

- Tokenization
- Embeddings
- Neural Networks
- Transformers
- Attention Mechanism
- Backpropagation
- Language Modeling
- Text Generation
- PyTorch Fundamentals

---

# Screenshots
check repo file 

---

# Author

## Rupesh Kumar Sah

B.Tech CSE (AI) Student  
AI/ML & Web Development Enthusiast

GitHub:
https://github.com/Rupesh5151

---

# License

This project is open-source and available under the MIT License.
