# Fine-Tuning DeepSeek-R1
Overview

This repository contains a fine-tuning script for DeepSeek-R1-Distill-Llama-8B, utilizing Unsloth for efficient training. By leveraging LoRA (Low-Rank Adaptation) and 4-bit quantization, we significantly reduce memory usage while maintaining high performance.

Features

Optimized Fine-Tuning: Uses Unsloth for efficient memory utilization.

LoRA Adaptation: Fine-tunes key transformer layers to save computational resources.

Hugging Face Integration: Seamlessly loads and uploads models.

Weights & Biases (wandb) Support: Tracks training progress.

Installation

Ensure you have the required dependencies installed:

pip install unsloth wandb transformers huggingface_hub trl

Usage

Clone the repository:

git clone https://github.com/SrihariR2004/fine_tune_deep_seek.git

cd fine-tune-deepseek

Update authentication tokens in train.py.

Run the training script:

python deep_seep train.py

After fine-tuning, the model will be saved locally and pushed to Hugging Face Hub.

Model Deployment

Once fine-tuned, you can load and use the model for inference:

from transformers import pipeline

model_name = "your_hf_username/DeepSeek-R1"

pipe = pipeline("text-generation", model=model_name)

print(pipe("What are the symptoms of diabetes?"))

Contributing

Feel free to submit pull requests or open issues to enhance the repository!

