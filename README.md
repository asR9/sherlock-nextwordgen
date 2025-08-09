# Sherlock Holmes Next-Word Prediction

LSTM + Multi-head Attention model trained on Sherlock Holmes stories for next-word prediction.

## Quick Setup

```bash
# Install uv
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone repo
git clone https://github.com/yourusername/sherlock-nextwordgen.git
cd sherlock-nextwordgen

# Install dependencies
uv pip install -e .

# Run Jupyter notebook
uv run jupyter notebook sherlock_nextwordgen.ipynb
```

## Model Architecture

```
GPT-2 Embeddings (768d) → Linear (128d) → 2-Layer LSTM → 4-Head Attention → Output
```

- **Parameters**: ~45.5M
- **Training Time**: ~2 min on GPU (T4)
- **Perplexity**: ~107-120

## Files

- `sherlock_nextwordgen.ipynb` - Main training notebook
- `pyproject.toml` - Dependencies (for uv)
- `README.md` - This file