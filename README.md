Task-01: Text Generation with GPT-2
Overview
Fine-tune GPT-2 model on Shakespeare dataset to generate text in Shakespearean style.

Objective
Train a model to generate coherent and contextually relevant text based on given prompts, mimicking Shakespearean writing style.

Implementation Details
Model
Architecture: GPT-2 (124M parameters)

Base Model: gpt2 from Hugging Face

Layers: 12

Hidden Size: 768

Attention Heads: 12

Dataset
Source: Shakespeare plays (tinyshakespeare)

Size: 1,115,394 characters

Training Samples: 300 lines

Test Samples: 5 prompts

Training Configuration
Epochs: 2

Batch Size: 4

Learning Rate: 5e-5

Max Length: 64 tokens

Mixed Precision: Enabled (FP16)

Hardware: Google Colab GPU (T4)

Project Structure
text
Task-01-Text-Generation-GPT2/
├── code/
│   └── gpt2_finetuning.ipynb
├── outputs/
│   ├── generated_1.txt
│   ├── generated_2.txt
│   ├── generated_3.txt
│   ├── generated_4.txt
│   ├── generated_5.txt
│   └── gpt2_finetuned/
├── report/
│   └── Task-01-Report.pdf
└── README.md
Setup & Installation
Requirements
bash
pip install transformers datasets accelerate torch
Run in Google Colab
Open Google Colab

Set runtime to GPU: Runtime → Change runtime type → GPU

Copy and paste the provided code

Run all cells

Usage
Training
python
# The code automatically:
# 1. Downloads Shakespeare dataset
# 2. Fine-tunes GPT-2 for 2 epochs
# 3. Generates text from 5 test prompts
# 4. Saves outputs
Text Generation
python
# Generate text from custom prompt
prompt = "Your custom prompt here"
generated_text = generate_text(prompt, max_length=100)
Generated Examples
Prompt: "To be or not to be"
Generated: "To be or not to be, that is the question: Whether 'tis nobler in the mind to suffer..."

Prompt: "Romeo, wherefore art thou"
Generated: "Romeo, wherefore art thou Romeo? Deny thy father and refuse thy name..."

Prompt: "All the world's a stage"
Generated: "All the world's a stage, And all the men and women merely players..."

Results
Successfully fine-tuned GPT-2 on Shakespeare dataset

Generated coherent Shakespeare-style text

Training completed in ~3 minutes

Model captures archaic language patterns effectively

Files Included
generated_1.txt to generated_5.txt - Sample outputs

Fine-tuned model weights

Complete Colab notebook

This README file

Dependencies
Python 3.8+

transformers 4.30+

datasets 2.12+

torch 2.0+

accelerate 0.20+

References
GPT-2 Paper

Hugging Face Transformers

Shakespeare Dataset
