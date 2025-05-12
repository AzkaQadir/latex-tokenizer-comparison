# latex-tokenizer-comparison
Efficient Tokenization of Mathematical LaTeX Formulas: A Comparative Study of Character, Word, Subword (BPE), and WordPiece Tokenizers

# LaTeX Tokenizer Comparison

This project explores and compares different tokenization strategies—**Character-level**, **Word-level**, **Subword (BPE)**, and **WordPiece**—for mathematical LaTeX formulas using Hugging Face's `tokenizers` library. The dataset used is [`OleehyO/latex-formulas`](https://huggingface.co/datasets/OleehyO/latex-formulas).

## 🧠 Motivation

Mathematical LaTeX expressions contain specialized syntax that challenges traditional tokenization methods. The goal is to evaluate how different tokenizers perform in terms of:

- Vocabulary Size
- Average Tokens per Formula (Efficiency)
- Out-of-Vocabulary (OOV) Rate

## 📦 Dataset

- Source: [OleehyO/latex-formulas](https://huggingface.co/datasets/OleehyO/latex-formulas)
  
## 🔧 Methods

1. **Data Cleaning**  
   - Normalizes whitespace  
   - Removes uncommon/special symbols (except core LaTeX math symbols)

2. **Tokenizers Trained**  
   - **Character-based** (BPE with ByteLevel)
   - **Word-based** (BPE with Whitespace)
   - **Subword-based** (BPE with ByteLevel)
   - **WordPiece** (WordPiece with Whitespace)

3. **Training**  
   - Vocabulary size: 5000  
   - Special tokens: `<PAD>`, `<UNK>`, `<BOS>`, `<EOS>`

4. **Evaluation Metrics**  
   - Vocabulary size  
   - Average tokens per formula  
   - OOV rate (%)

## 📊 Results

Evaluation includes:
- Printing metrics for each tokenizer
- Visualization using bar plots for efficiency
- Token outputs for sample LaTeX formulas

## 📁 Output Files

- `character_tokenizer.json`
- `word_tokenizer.json`
- `subword_tokenizer.json`
- `wordpiece_tokenizer.json`
- `cleaned_latex_formulas.txt`

## 🧪 Sample Test Formulas

```latex
\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}
\int_{0}^{\infty} x^{s-1} e^{-x} dx = \Gamma(s)
\begin{array}{cc} a & b \\ c & d \end{array}

## 📊 Visualization
A bar plot comparing average tokens per formula for each tokenizer is generated using Seaborn.

##📜 License
This project is under the MIT License.

##🔗 Related
Hugging Face Tokenizers Documentation
LaTeX Formula Dataset

##📌 Disclaimer
This project was developed as part of a personal learning journey in reinforcement learning.
As such, it may contain experimental implementations, non-optimized code, or areas for improvement.
Feedback, suggestions, and contributions are always welcome!
