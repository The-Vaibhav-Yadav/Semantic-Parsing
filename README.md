### Project Overview:
The notebook involves training or evaluating a natural language processing model (likely for text-to-SQL translation) using the **Spider dataset**. It uses Hugging Face Transformers, PyTorch, and Google Colab (with Google Drive integration for data loading).

---

# Text-to-SQL Generation using Transformers

This project focuses on converting natural language questions into SQL queries using transformer-based sequence-to-sequence models. The **Spider** dataset is used to train and evaluate the model, enabling generalization to unseen databases.

## 📁 Project Structure

- `FINAL_NLP.ipynb`: Main notebook containing preprocessing, model setup, training, and evaluation pipeline.
- Data loaded from Google Drive:
  - `train_spider.json`
  - `tables.json`

## 🚀 Features

- Schema serialization for input formatting
- Dataset class for PyTorch DataLoader
- Hugging Face Transformers for sequence-to-sequence modeling
- Mixed-precision training with `torch.cuda.amp`

## 🛠️ Setup Instructions

1. Clone this repository and upload to Google Colab.
2. Mount Google Drive in the notebook.
3. Ensure your Drive contains the Spider dataset at the following path:
   ```
   /MyDrive/NLP/spider_data/
   ├── train_spider.json
   └── tables.json
   ```

4. Install required packages:
   ```bash
   pip install transformers torch
   ```

Other Requirements are mentioned in the Final_NLP.ipynb file

## 🧠 Model

Uses a Hugging Face `AutoModelForSeq2SeqLM` and `AutoTokenizer`. You can modify this to use models like `T5`, `BART`, etc.

## 📊 Dataset

**Spider** dataset – a complex and cross-domain semantic parsing dataset. More info: [https://yale-lily.github.io/spider](https://yale-lily.github.io/spider)

## 🔍 Example

Each input to the model includes:
- Natural language question
- Serialized schema from the associated database

## 📌 Notes

- Make sure you have GPU enabled in Colab for training.
- Adjust batch size based on available memory.

## 📜 License

MIT License.

---
