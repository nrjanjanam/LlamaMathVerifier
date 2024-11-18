# LlamaMathVerifier

A fine-tuned Llama3-8B model for mathematical answer verification using Supervised Fine-Tuning (SFT). This project implements a binary classification system to determine the correctness of mathematical solutions across various topics.

## Project Overview

This implementation uses Parameter-Efficient Fine-Tuning (PEFT) with LoRA to adapt Llama3-8B for mathematical reasoning verification. The model evaluates mathematical solutions and provides binary (True/False) verification of answer correctness.

## Dataset

### Overview
The dataset consists of mathematical problems and their solutions, specifically structured for answer verification:

### Structure
- **Questions**: Mathematical problems across various topics
- **Answers**: Provided solutions to be verified
- **Solutions**: Detailed explanations and reasoning
- **Labels**: Binary classification (True/False) indicating answer correctness

### Specifications
- Training Set Size: 900000
- Validation Set Size: 100000
- Test Set Size: 10000
- Format: CSV
- Label Distribution: [Distribution of True/False labels if known]

### Key Features
- Diverse mathematical topics
- Detailed solution explanations
- Binary verification labels
- No external datasets permitted
- Test partition reserved for evaluation only

### Data Processing
- Text cleaning and normalization
- Prompt formatting
- Token length optimization
- Special character handling for mathematical symbols
- Solution explanation integration

### Usage Restrictions
- Limited to competition-provided dataset
- No external data augmentation
- Test set strictly for evaluation
- Compliance with NYU academic rules

### Key Features
- 🚀 Supervised Fine-Tuning of Llama3-8B
- 🔧 LoRA-based parameter-efficient training
- 📊 Binary classification for answer verification
- 🧮 Specialized mathematical reasoning
- 🔍 Solution explanation integration

### Technical Specifications
- Model: Llama3-8B
- Training Method: SFT with LoRA
- Task: Binary Classification
- Input: Mathematical questions with answers and explanations
- Output: Boolean verification (True/False)

## Implementation Details

- Parameter-Efficient Fine-Tuning using LoRA
- 4-bit quantization for memory efficiency
- Optimized prompt engineering
- Comprehensive evaluation metrics
- Inference pipeline for solution verification

## Performance

- Baseline Accuracy (on running on Colab): 0.56025
- Finetuned Acccuracy: 0.82438
- Target Metric: Binary Classification Accuracy
- Evaluation: Validation Set Accuracy

## Usage

Detailed implementation and usage instructions are provided in the Jupyter notebook. The repository includes:
- Training pipeline
- Inference code
- Evaluation metrics
- Hyperparameter configurations
- Example usage scenarios

## Requirements

- Python 3.8+
- pyTorch
- transformers
- unsloth
- datasets
- random
- gc
- trl
- tqdm

## Citation

If you use this implementation in your work, please cite:

```bibtex
@software{mathverifyllm2024,
  author = {[Abhishek Mahajan, Neeha Rathna Janjanam, Nimit Kanani]},
  title = {MathVerifyLLM: Mathematical Answer Verification using Llama3-8B},
  year = {2024},
  publisher = {GitHub},
  url = {https://github.com/nrjanjanam/MathVerifyLLM}
}
