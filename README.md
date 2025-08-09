# Sherlock Holmes Next-Word Prediction

LSTM + Multi-head Attention model trained on Sherlock Holmes stories for next-word prediction.

## Quick Start

### Option 1: Google Colab (Runs in 1 min with T4 GPU)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asR9/sherlock-nextwordgen/blob/main/sherlock_nextwordgen.ipynb)

Simply click the badge above to run the notebook directly in Google Colab. Select T4 GPU and click run

### Option 2: Local Setup
```bash
# Install uv
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone repo
git clone https://github.com/asR9/sherlock-nextwordgen.git
cd sherlock-nextwordgen

# Create venv in .venv folder
uv venv

# Install dependencies from pyproject.toml
uv pip install -e .

# Run Jupyter notebook (from venv)
uv run jupyter notebook sherlock_nextwordgen.ipynb
```

## Model Architecture
```
GPT-2 Embeddings (768d) → Linear (128d) → 2-Layer LSTM → 4-Head Attention → Output
```

## Performance
- **Parameters**: ~45.5M
- **Training Time**: ~2 min on GPU (T4)
- **Perplexity**: ~107-120

## Files
- `sherlock_nextwordgen.ipynb` - Main training notebook
- `pyproject.toml` - Dependencies (for uv)
- `README.md` - This file

## Usage
The model generates text in the style of Arthur Conan Doyle's Sherlock Holmes stories. Simply run the notebook cells to train the model and generate your own Holmes-style text!
