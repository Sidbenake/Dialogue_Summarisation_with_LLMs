# Dialogue Summarization with Fine-Tuned Large Language Models

This repository contains notebooks that explore various methods for improving dialogue summarization using state-of-the-art large language models (LLMs). The notebooks demonstrate approaches such as instruction fine-tuning, parameter-efficient fine-tuning (PEFT), and Proximal Policy Optimization (PPO) for reducing toxicity in model completions.

## Notebooks

### 1. Introduction to LLMs
This notebook demonstrates the process of instruction fine-tuning Google's FLAN-T5 model using the DialogSum dataset. It serves as a foundational guide to loading the dataset and applying fine-tuning techniques to improve dialogue summarization performance.

### 2. PEFT LoRA ROUGE Score Comparison
This notebook leverages PEFT's LoRA method to fine-tune only 1.41% of the parameters of the FLAN-T5 model, resulting in an absolute ~17% improvement in the ROUGE score compared to the original model. The performance of this parameter-efficient model is on par with that of a fully fine-tuned FLAN-T5 model, making it a highly efficient alternative.

### 3. Reducing Toxicity using PPO and RoBERTa with LoRA
In this notebook, Proximal Policy Optimization (PPO) is applied to reduce the toxicity of model-generated completions. RoBERTa is used to classify each completion as either 'hate' or 'nothate,' and the logit value of the 'nothate' class is used as a reward for the PPO algorithm to fine-tune the model's weights. This approach successfully reduces the mean toxicity of Google's FLAN-T5 model by an absolute 27%, making it a more ethical and safer solution for dialogue summarization tasks.

## Summary
This repository showcases practical implementations of cutting-edge fine-tuning techniques on LLMs to enhance performance and reduce biases. The methods used include instruction fine-tuning, PEFT with LoRA, and reinforcement learning with PPO, offering valuable insights for those interested in dialogue summarization and large language models.
