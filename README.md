# Resume Matcher AI 🚀

A lightweight, notebook-driven NLP pipeline that **scores** how well a candidate’s résumé matches a job description and then **explains** the match in plain English.  
Built with Hugging Face Transformers (BERT & FLAN-T5), PyTorch, and scikit-learn.

---

## ✨ Features
| Stage | Model | What it does |
|-------|-------|--------------|
| **1. Classification** | `bert-base-uncased` fine-tuned | Predicts a *Match* label (`0 = No match`, `1 = Partial`, `2 = Good`) |
| **2. Explanation** | `google/flan-t5-small` fine-tuned | Generates a natural-language rationale (“Why this résumé fits / fails”) |

Additional goodies 📈  
* End-to-end notebook (`resumeMatcher.ipynb`) with training ➜ evaluation ➜ inference.  
* Notebook cells show dataset exploration, train/val split, metrics, and sample predictions.  
* Easily extensible to larger models or custom data.

---

### Dataset format  
`jobmatch_dataset.json` is a list of objects:

[
  {
    "job_description": "Hiring data scientist with NLP, Python, Transformers…",
    "resume": "Developed NLP models using spaCy and Hugging Face…",
    "label": 2
  },
  ...
]```


### Requirements
torch>=2.0
transformers>=4.40
pandas
scikit-learn
matplotlib
jupyter
