# Dyslexic NLP Audit

> What Happens to Your Writing When You're Dyslexic and an NLP Pipeline Reads It?

A three-experiment audit of how standard NLP tools treat dyslexic writing as input.
Published on [Towards Data Science](#) ← replace with your article link

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/dyslexic-nlp-audit/blob/main/dyslexic_nlp_audit.ipynb)

---

## Experiments

| # | Experiment | Tool | Dataset |
|---|-----------|------|---------|
| 1 | Sentiment Classifier Audit | cardiffnlp/twitter-roberta-base-sentiment-latest | IMDB (500 reviews) |
| 2 | Readability Score Audit | Flesch-Kincaid · Gunning Fog · SMOG | IMDB matched pairs |
| 3 | Grammar Correction Audit | LanguageTool (en-GB) | IMDB sample (100 reviews) |

---

## Key Findings

- **2.4% label flip rate** on dyslexic-pattern text in a RoBERTa sentiment classifier
- **0.227 confidence swing** from a single phonetic spelling of one contraction
- **48.8% wrong correction rate** from LanguageTool on dyslexic-pattern text
- Most frequent wrong correction: `woz → won` (18 occurrences), intended: `was`

---

## Requirements

```bash
pip install transformers datasets textstat language_tool_python torch
```

---

## Dataset

IMDB Large Movie Review Dataset — Stanford AI Lab  
https://ai.stanford.edu/~amaas/data/sentiment/  
Open licence. No PII. No real customer data.

---

## Author

**Immanuel Obani** — Data Scientist (NLP & Responsible AI)  
[immanuelobani.com](https://immanuelobani.com)
