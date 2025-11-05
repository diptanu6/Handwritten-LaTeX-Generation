# Handwritten-LaTeX-Generation


**Handwritten-LaTeX-Generation** is a deep learning–based project that converts *handwritten mathematical expressions* into structured **LaTeX code**.
It combines **vision-language transformer models** with fine-tuning on the **Im2LaTeX-230K dataset** to achieve accurate symbol recognition and expression formatting.

---

## 🚀 Project Overview

Mathematical expression recognition requires understanding both **visual structure** and **symbolic semantics**.
This project integrates:

* 🧩 **Microsoft TrOCR** for handwritten text recognition
* 🧠 **Vision-Language Models (Qwen2-VL / LLaMA-3.2)** for multimodal sequence learning
* 📜 **Transformer-based LaTeX generator** trained on **Im2LaTeX-230K**

The system, **Handwritten-LaTeX-Generation**, can interpret handwritten equations and generate their equivalent LaTeX markup.

---

## 🧰 Tech Stack

* **Language:** Python
* **Frameworks:** PyTorch, Hugging Face Transformers
* **Libraries:** OpenCV, NumPy, Matplotlib, scikit-learn
* **Environment:** Google Colab
* **Base Models:** TrOCR, Qwen2-VL, LLaMA-3.2, ViT Encoder

---

## 📊 Dataset: Im2LaTeX-230K

The **Im2LaTeX-230K** dataset is a large-scale collection of rendered mathematical expressions with their LaTeX source.

### 📁 Dataset Structure

| Component   | Description                                 |
| ----------- | ------------------------------------------- |
| **Images**  | Rendered mathematical formulas (PNG format) |
| **Labels**  | Corresponding LaTeX strings                 |
| **Samples** | 230,000+ image–LaTeX pairs                  |
| **Split**   | Train / Validation / Test                   |
| **Format**  | `<image_path> \t <LaTeX_code>`              |

### 🔍 Example

```
img_0000123.png    \frac{a+b}{c+d}
img_0000456.png    \int_{0}^{\infty} e^{-x^2} dx
```

### 🧪 Why Im2LaTeX-230K?

* Covers diverse mathematical notations (integrals, fractions, matrices, limits, etc.)
* Provides clean LaTeX annotations suitable for sequence-to-sequence training
* Compatible with Transformer-based models for multimodal learning

---

## 🧩 Model Architecture

1. **Encoder:** Vision Transformer (ViT) extracts spatial features from handwritten input images.
2. **Decoder:** Transformer-based LaTeX generator produces tokenized LaTeX sequences.
3. **Loss Function:** Cross-Entropy with teacher forcing.
4. **Metrics:**

   * Exact Match Accuracy
   * Expression Recognition Rate (ERR)
   * BLEU Score
   * Edit Distance

---

## 🧠 Training Workflow

1. Preprocess images and tokenize LaTeX expressions
2. Load pretrained encoder (TrOCR / Qwen2-VL)
3. Fine-tune model on Im2LaTeX-230K dataset
4. Validate and evaluate with BLEU, ERR, and Exact Match
5. Generate LaTeX predictions and visualize output

---

## ⚙️ Usage

```bash
# Clone the repository
git clone https://github.com/yourusername/Handwritten-LaTeX-Generation.git
cd Handwritten-LaTeX-Generation

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook hwrite2latex.ipynb
```

---

## 📈 Results & Discussion

* The model achieves high recognition accuracy on structured handwritten equations.
* Fine-tuning with **TrOCR + Qwen2-VL** improves semantic consistency and spacing in generated LaTeX.
* Evaluation shows balanced performance across both clean and noisy inputs.

---

## 📚 References

* *Deng et al., “Im2LaTeX: Translating Images to Markup,” arXiv:1609.04938 (2016)*
* *Microsoft TrOCR: Transformer-based OCR*
* *Qwen2-VL and LLaMA-3.2 Vision-Language models (2024–2025)*
* *CROHME: Competition on Recognition of Online Handwritten Mathematical Expressions*

---

## 🧑‍💻 Author

**Diptanu Biswas**
Final-Year BTMT (Computational Mathematics), NIT Agartala
📧 [diptanubiswas@email.com](mailto:diptanubiswas@email.com)
💼 [LinkedIn](https://linkedin.com/in/diptanubiswas) 🐙 [GitHub](https://github.com/yourusername)

---

## 🏁 Future Work

* Fine-tuning with CROHME dataset for handwritten variations
* Integration of live **LaTeX rendering** interface
* Deployment via **FastAPI + Streamlit** for real-time usage

---

**⭐ If this project helps your research or work, please star the repo and share feedback!**
