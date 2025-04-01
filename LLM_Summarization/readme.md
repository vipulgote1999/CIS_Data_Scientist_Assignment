# LLM Summarization Task

## Overview
This repository contains a Jupyter Notebook for fine-tuning and evaluating an LLM-based summarization model using a Hugging Face adapter model. The notebook is designed to streamline the process of summarizing text effectively using state-of-the-art AI models.

## Model Used
- **Hugging Face Model**: [Llama 2 Summarization Adapter Model](https://huggingface.co/Existance/llama2-summarizations-adapter-models-1743521986.1225166)

## Features
- Fine-tunes an LLM model for text summarization.
- Uses Hugging Face’s transformers and adapter-based fine-tuning.
- Supports Weights & Biases (wandb) for experiment tracking.
- Provides inference functionality for generating summaries.

## Installation
To set up the environment, install the required dependencies:

```bash
pip install -r requirements.txt
```
Ensure you are logged into Hugging Face and Weights & Biases before running the notebook:

```python
from huggingface_hub import notebook_login
import wandb

notebook_login()
wandb.login()
```
## Usage
Run the Jupyter Notebook to train and evaluate the summarization model:

```bash

jupyter notebook LLM_Summarization_Task_CIS.ipynb
```

## Dataset
The notebook processes text input for summarization tasks. Ensure the dataset is correctly formatted before running the training pipeline.

## Results & Metrics
  - Training loss, validation loss, and other performance metrics are tracked via Weights & Biases.
  
  - The final model can be used for summarization tasks in various applications.
  
  - Weights & Biases training run details: [WandB Run](https://wandb.ai/existence/huggingface/runs/b8x350xg)

## Acknowledgments
Hugging Face for the model and transformers library.

Weights & Biases for experiment tracking.

## License
This project is licensed under the MIT License. 
