#  Dhaka Bus Sentiment Analysis using LLM + LoRA

##  Overview
This project presents a **survey-based sentiment analysis of Dhaka local bus services** using **lightweight Large Language Models (LLMs)** fine-tuned with **LoRA (Low-Rank Adaptation)** via the **Unsloth framework**.

The goal is to analyze commuter feedback and classify:
- **Sentiment** (Positive, Neutral, Negative)
- **Service Issues** (Delay, Safety, Cost, Comfort, etc.)

---

##  Objectives
- To fine-tune a 4-bit instruction model using LoRA with the Unsloth framework Dhaka local bus sentiment dataset.
- To compare the performance of the base model and the fine-tuned model using accuracy, precision, recall, and weighted F1-score.

---

##  Methodology

### 1. Data Collection
- Synthetic survey-based dataset
- Includes:
  - commuter comments
  - demographics (age, profession)
  - travel context (time, crowding, waiting time)

### 2. Data Processing
- CSV → JSONL conversion
- Instruction-based formatting for LLM training

### 3. Model Training
- Model: Lightweight LLM (Qwen / LLaMA via Unsloth)
- Technique: **LoRA (Parameter-Efficient Fine-Tuning)**
- Framework: **Unsloth + Hugging Face TRL**

### 4. Tasks
- Sentiment Classification
- Issue Category Classification

---

##  Technologies Used

- Python
- Google Colab
- Unsloth
- Hugging Face Transformers
- TRL (SFTTrainer)
- PEFT (LoRA)
- Scikit-learn

---

##  Results

| Task | Accuracy | Precision | Recall | F1 Score |
|------|---------|----------|--------|----------|
| Sentiment Classification | 1.00 | 1.00 | 1.00 | 1.00 |
| Issue Category Classification | 0.14 | 0.020 | 0.14 | 0.034 |

> Note: Initial results may show low accuracy due to output formatting issues, which were later improved using robust extraction methods.



##  Dataset

- Synthetic dataset based on real-world transport scenarios
- Contains:
  - `comment_text`
  - `sentiment_label`
  - `primary_category`
  - contextual features
