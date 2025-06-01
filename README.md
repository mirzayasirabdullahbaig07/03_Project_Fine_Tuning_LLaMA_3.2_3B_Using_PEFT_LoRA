# 🧠 Parameter-Efficient Supervised Fine-Tuning of LLaMA 3.2 (3B) on a Medical Chain-of-Thought Dataset

## 👨‍⚕️ Project Objective

This project fine-tunes the **LLaMA 3.2 (3B)** language model on a **Medical Chain-of-Thought (CoT)** dataset using **parameter-efficient fine-tuning (PEFT)** with **LoRA** via the **Unsloth** library on **Kaggle Notebooks**. The goal is to enhance the model’s capability to reason and generate structured responses in the medical domain.

## 🧪 Key Features

- Utilizes **LoRA (Low-Rank Adaptation)** for efficient fine-tuning.
- Trains on the **FreedomIntelligence/Medical-CoT** dataset from Hugging Face.
- Applies structured formatting using `<think>` and `<response>` tags.
- Tracks training progress and metrics using **Weights & Biases (wandb)**.
- Evaluates model improvements using **ROUGE-L** scores.
- Uploads the fine-tuned adapter and tokenizer to **Hugging Face Hub**.
- Provides clear instructions for **inference** using the adapter.

## 🔧 Workflow Overview

### 1. Environment Setup
- Kaggle Notebook configured with required libraries.
- GPU enabled for faster computation.
- wandb initialized for live training logs.

### 2. Dataset Preparation
- Loads Medical Chain-of-Thought dataset.
- Formats data using `<think>` and `<response>` tags.
- Splits into training and validation subsets.

### 3. Model Loading
- Loads the quantized 4-bit **LLaMA 3.2 3B** base model via Unsloth.
- Applies **LoRA** using PEFT for efficient training.

### 4. Data Preprocessing
- Tokenizes and pads inputs.
- Prepares datasets for supervised fine-tuning.

### 5. Training
- Trains the LoRA adapter using the Trainer API.
- Evaluation done after every epoch.
- Training tracked on **wandb**.

### 6. Saving Artifacts
- Saves the LoRA adapter and tokenizer locally.
- Pushes the model to Hugging Face model hub.

### 7. Inference
- Loads base model and LoRA adapter for inference.
- Generates medical responses from `<think>` prompts.

### 8. ROUGE-L Evaluation
- Compares **ROUGE-L** scores before and after fine-tuning.
- Demonstrates model improvement in structured medical response generation.

## 🚀 Deliverables

- ✅ Kaggle Notebook with training workflow.
- ✅ Uploaded Model: [Hugging Face Repo](https://huggingface.co/ArshiaJ05/lora-medical-llama3-3b)
- ✅ Weights & Biases training logs.
- ✅ ROUGE-L score comparison (before vs after fine-tuning).
- ✅ Inference Instructions for downstream usage.

## 🏁 Conclusion

This project showcases how **parameter-efficient fine-tuning** with **LoRA** and **Unsloth** can significantly enhance a large language model’s ability in domain-specific reasoning—in this case, medical structured thinking—while keeping compute costs manageable.

---

## 📇 About the Author

**Name:** Mirza Yasir Abdullah Baig  
**GitHub:** [github.com/mirzayasirabdullahbaig07](https://github.com/mirzayasirabdullahbaig07)  
**LinkedIn:** [linkedin.com/in/mirza-yasir-abdullah-baig](https://www.linkedin.com/in/mirza-yasir-abdullah-baig/)  
**Email:** yasirabdullah4549@gmail.com  


📌 This project was completed as part of the **Arch Technology Internship Advanced Task**.

