# Llama 3.2 3B Instruct Code Fine-tuning

This repository contains code for fine-tuning the Llama 3.2 3B Instruct model on a Python code dataset using the Unsloth library. The project aims to enhance the model's ability to generate and understand Python code.

## Features

- Utilizes the Unsloth library for efficient fine-tuning of large language models
- Implements 4-bit quantization for reduced memory usage
- Uses LoRA (Low-Rank Adaptation) for parameter-efficient fine-tuning
- Integrates with Hugging Face's Transformers and TRL libraries
- Supports gradient checkpointing for handling long contexts
- Includes options for mixed precision training (FP16 or BF16)

## Setup

1. Install the required dependencies:
   ```
   pip install "unsloth[colab-new] @ git+https://github.com/unslothai/unsloth.git"
   pip install "git+https://github.com/huggingface/transformers.git"
   pip install -U trl
   pip install --no-deps trl peft accelerate bitsandbytes
   pip install torch torchvision torchaudio triton
   pip install xformers
   ```

2. Load the dataset and prepare the model:
   - The code uses the "nikhiljatiwal/Llama-3.2-Python-Alpaca-143k" dataset
   - The base model is "unsloth/Llama-3.2-3B-Instruct-bnb-4bit"

3. Configure the training arguments and start the fine-tuning process

4. Save the model locally and push to Hugging Face Hub

## Usage

Adjust the training parameters as needed, such as batch size, learning rate, and number of epochs. You can also modify the LoRA configuration to suit your requirements.

## Contributing

Feel free to open issues or submit pull requests to improve this project.

## License

[apache-2.0]
