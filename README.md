# SupportSage AI

SupportSage AI is a fine-tuned customer support language model built using Meta Llama 3.2 1B Instruct and LoRA-based parameter-efficient fine-tuning.

## Features

- Fine-tunes an instruction-following language model for customer support responses.
- Uses the Bitext customer support dataset.
- Applies 4-bit quantization to reduce model memory requirements.
- Uses LoRA to train a small subset of parameters rather than the entire base model.
- Supports generating responses to customer questions.

## Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- PEFT / LoRA
- TRL
- BitsAndBytes
- Google Colab

## Model

Base model: `meta-llama/Llama-3.2-1B-Instruct`

Fine-tuned weights: LoRA adapter saved separately from the base model.

The base model may require Hugging Face access approval and authentication. Refer to the model's official page for its license and access requirements.

## Dataset

[Bitext Customer Support LLM Chatbot Training Dataset](https://huggingface.co/datasets/bitext/Bitext-customer-support-llm-chatbot-training-dataset)

## Project Structure

```text
SupportSage_AI/
├── SupportSage_AI.ipynb
├── final_adapter/
├── README.md
├── requirements.txt
└── .gitignore
```

## Usage

1. Install the required Python dependencies in a compatible environment.
2. Obtain access to the base model on Hugging Face.
3. Authenticate using a Hugging Face access token stored securely as an environment variable.
4. Load the base model and saved adapter using Transformers and PEFT.
5. Generate responses using the inference code in the notebook.

## Current Status

Fine-tuning and basic inference have been completed. Systematic held-out evaluation and further deployment work are planned.

## Security

Never commit access tokens, `.env` files, or other credentials to the repository.