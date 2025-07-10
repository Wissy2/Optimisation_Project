
#  Optimizer Comparison for Fine-Tuning BERT and GPT-2

This project compares the performance of various optimization algorithms — **AdamW**, **LAMB**, **Adafactor**, and **SGD with warmup** — on two different tasks:
- **Text Classification with BERT** using the **SST-2** dataset
- **Question Answering with GPT-2** using the **SQuAD v1.1** dataset

##  Objectives

- Evaluate the impact of different optimizers on training accuracy, F1-score, validation loss, and training time  
- Log and visualize training metrics with **Weights & Biases (WandB)**
- Export the results to Excel for easier comparison

##  Technologies Used

- Python 3.x  
- PyTorch  
- HuggingFace Transformers & Datasets  
- scikit-learn  
- pandas + openpyxl  
- Weights & Biases (WandB) for experiment tracking

## 📁 Project Structure

```
├── Bert_optimisation.py     # BERT fine-tuning on SST-2 with optimizer comparison
├── bert-optimisation.ipynb  # Notebook with results of BERT fine-tuning on SST-2 with optimizer comparison               
├── Gpt_optimisation.py      # GPT-2 fine-tuning on SQuAD with optimizer comparison
├── gpt-optimisation.ipynb   # Notebook with results of GPT fine-tuning on SST-2 with optimizer comparison
├── README.md                # This file
```

## 🚀 How to Run

### 📌 Requirements

- Kaggle, Google Colab, or local environment with GPU
- A WandB API key (added via Kaggle Secrets or as an environment variable)

### 🧪 To Run BERT Optimization:

```bash
python Bert_optimisation.py
```

This will:
- Train BERT on SST-2 using all 4 optimizers
- Track metrics on WandB
- Export results to `bert_optimization_results.xlsx`

### 🧠 To Run GPT-2 Optimization:

```bash
python Gpt_optimisation.py
```

This will:
- Fine-tune GPT-2 on SQuAD using all 4 optimizers
- Track metrics on WandB
- Export results to `gpt_qa_optimization_results.xlsx`

## 📈 Evaluation Metrics

### For BERT (Text Classification):
- Accuracy  
- F1-score  
- Precision / Recall

### For GPT-2 (Question Answering):
- Exact Match (EM)  
- F1-score  
- Start/End token accuracy

## 📊 Output

Both scripts export an Excel file with:
- **Summary sheet**: final scores per optimizer  
- **Detailed_Results sheet**: epoch-by-epoch performance  
- **Comparison_Ranking sheet**: sorted results and ranking  

## 🔍 Notes

- The LAMB optimizer is simulated using AdamW with modified hyperparameters  
- Answer extraction in GPT-2 is simplified for efficiency and could be further refined  
- Both models are limited to a subset of the full datasets to ensure quick comparison

## 🙋‍♀️ Authors

- Wissal HANAOUI
- Imane IDBALI
- Hiba TIJANI
