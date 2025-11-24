# Fine-tuning of LLMs

Practical seminar for 2nd year students at FNSPE CTU in Prague. Fine-tuning of LLM for phishing email classification.

Prepared by Lukáš Bátrla, AI Researcher at Cisco Systems.

--------------------

## The structure of the lecture

1. Problem introduction - Phishing email classification
2. Data preparation and splitting
3. In-context learning
4. Full fine-tuning
5. Parameter efficient fine-tuning

--------------------

## Getting Started

**Setup Instructions:** See [STUDENT_LOCAL_SETUP.md](STUDENT_LOCAL_SETUP.md) for detailed installation and configuration steps.

## Notebooks

- **`LLM_Finetuning_for_Phishing.ipynb`** - Main notebook for GPU/MPS training
- **`LLM_Finetuning_for_Phishing_for_CPU.ipynb`** - CPU-optimized version with reduced dataset (20%)

## Requirements

- Python 3.9+
- 4-8GB RAM (CPU training) or 8-16GB RAM (GPU training)
- 10+ GB free disk space
- GPU optional but recommended (10-100x faster training)
