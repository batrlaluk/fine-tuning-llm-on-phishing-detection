# Student Local Setup Guide
## LLM Fine-tuning for Phishing Detection

---

## System Requirements

- Python 3.9+
- 16 GB RAM recommended (8 GB minimum)
- 20+ GB free disk space
- GPU optional but recommended (training is 10-100x faster with GPU)

---

## Step 1: Verify Python Version

```bash
python --version
```

---

## Step 2: Create Virtual Environment

```bash
# Navigate to your project folder
cd /path/to/your/project

# Create virtual environment
python -m venv venv

# Activate virtual environment
source venv/bin/activate
```

---

## Step 3: Install Required Packages

```bash
# Upgrade pip first
pip install --upgrade pip

# Install all required packages
pip install torch transformers datasets peft scikit-learn numpy pandas accelerate tqdm jupyterlab

# For NVIDIA GPU with CUDA:
pip install torch --index-url https://download.pytorch.org/whl/cu118
```

---

## Step 4: Verify Installation

```bash
python -c "import torch, transformers, datasets, peft, sklearn; print('✓ All packages installed successfully')"
```

---

## Step 5: Pre-download Flan-T5-small model (optional)
To avoid network congestion during class, you can pre-download the required model:

```bash
python -c "from transformers import AutoTokenizer, AutoModelForSeq2SeqLM; AutoTokenizer.from_pretrained('google/flan-t5-small'); AutoModelForSeq2SeqLM.from_pretrained('google/flan-t5-small'); print('✓ Models downloaded successfully')"
```

**Cache location:**
- Linux/Mac: `~/.cache/huggingface/hub/`

---

## Step 5: Start Jupyter Lab

```bash
jupyter lab
```

Navigate to `LLM_Finetuning_for_Phishing.ipynb` and open it.

---

## Troubleshooting

1. **"ModuleNotFoundError"**: Make sure virtual environment is activated
2. **GPU not detected**: Check device configuration in notebook Section 0
3. **Out of memory**: Reduce batch size or use LoRA instead of full fine-tuning
4. **Slow training**: On GPU, increase batch size or gradient aggregation if you have enough RAM - to parallelize learning.

---

## Deactivate Virtual Environment (when done)

```bash
deactivate
```

