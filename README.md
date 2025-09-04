Here’s a **clean, professional version of your README.md** (no emojis, no unnecessary fluff):

---

# Healthcare AI Assistant (LLaMA)

This repository contains an AI-powered healthcare assistant built using LLaMA for **medical Q\&A**, **triage-style guidance**, and **structured responses**.
The project includes a Jupyter notebook (`app.ipynb`), setup instructions, and references for downloading model weights (not included in this repository).

> **Disclaimer:** This project is for **educational and research purposes only**. It is **not intended to provide medical advice, diagnosis, or treatment**.

---

## Features

* LLaMA-based medical Q\&A with customizable prompts
* Optional FastAPI backend for asynchronous inference and REST endpoints
* Streamlit interface for interactive demonstrations
* Schema validation using Pydantic
* Configuration-driven setup with `.env` support
* Fully reproducible environment via `requirements.txt`

---

## Architecture

```
Streamlit (Frontend) → FastAPI (Backend) → LLaMA runtime (llama.cpp / llama-cpp-python)
                                         ↘ Pydantic schemas
```

---

## Repository Structure

```
.
├─ app.ipynb                # Main notebook
├─ requirements.txt         # Python dependencies
├─ models/                  # Placeholder for model weights (not included)
│  └─ README.md             # Instructions for downloading q4/q8 weights
├─ data/                    # Sample/test datasets (if any)
├─ .gitignore               # Ignore cache, models, large files
└─ README.md                # This file
```

---

## Prerequisites

* Python 3.9–3.11
* Git (and optionally Git LFS for handling large files)
* One of the following runtimes:

  * `llama-cpp-python` (Python-based)
  * `llama.cpp` (CLI-based)

> Model weights are not included. Refer to `models/README.md` for download instructions.



## Setup

```bash
# 1) Clone the repository
git clone https://github.com/<your-username>/healthcare-llama-assistant.git
cd healthcare-llama-assistant

# 2) Create and activate a virtual environment
python -m venv .venv
# Windows:
.\.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

# 3) Install dependencies
pip install -r requirements.txt

# 4) Download model weights (q4/q8) and place them in ./models

# 5) Run the application (Streamlit example)
streamlit run app.ipynb

# Or, if using FastAPI:
# uvicorn app:app --host 0.0.0.0 --port 8000 --reload
```



## Testing

If tests are included, place them in a `tests/` folder and run:

```bash
pytest -q
```


## Model Weights

Model weights are not provided in this repository. Follow the instructions in `models/README.md` to download and configure **q4** (optimized for speed) or **q8** (optimized for quality) weights.


## Dataset
Dataset have been uploaded as Criticial and Non Critical. These are images relating to various skin marks like bruises cuts etc.

## License

This project is recommended to be licensed under the **MIT License** or another open-source license of your choice.


