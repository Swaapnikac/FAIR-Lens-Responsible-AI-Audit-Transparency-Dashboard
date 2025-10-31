# FAIR-Lens – Auditing Generative AI for Civic and Public-Sector Use

FAIR-Lens is a prototype auditing tool that evaluates the outputs of generative AI systems (chatbots, assistants, LLM-powered forms) against responsible AI criteria relevant to government and social-impact projects.  
It is designed for teams like the Burnes Center’s **AI for Impact Program**, who are deploying AI to serve vulnerable populations and need a fast way to check for bias, clarity, and accessibility.

This project complements civic AI products such as **FAIR (Fast AI-Assisted Investigation & Review)**, **GENIE**, and **A-IEP** by providing a transparency layer.  
Instead of just generating content, FAIR-Lens tells you whether the content is readable, neutral, inclusive, and explainable.

---

## What It Does
- Takes any AI-generated text as input  
- Runs a set of evaluations:  
  - Readability (Flesch-Kincaid)  
  - Tone and sentiment  
  - Biased or exclusionary phrasing detection  
  - Accessibility and plain-language score  
  - Transparency (whether rationale, sources, or next steps are present)  
- Produces a 0–100 **Responsible AI Score**  
- Provides suggestions for improvement  
- Can optionally call an LLM to re-write the text in a more inclusive and public-facing style  

---

## Why This Matters
Public-sector AI must not only be accurate but also:  
- Understandable to non-technical residents  
- Inclusive of people with language or accessibility needs  
- Free from obvious bias or exclusionary phrasing  
- Auditable by human staff  

FAIR-Lens demonstrates that **LLM engineering and AI governance** can be implemented together.  

---

## Features
- Text scoring and analysis function  
- Streamlit dashboard to paste text and view the Responsible AI Score  
- Optional LLM-based rewrite for inclusivity and plain language  
- Keyword dictionaries for detecting common civic bias issues  
- Exportable JSON report for auditing and documentation  

---

## Tech Stack
- Python 3.x  
- textstat (for readability scoring)  
- textblob or nltk/vader (for sentiment analysis)  
- spaCy (for natural language processing)  
- Streamlit (interactive dashboard)  
- OpenAI API (for rewrite and improvement mode)  

---

## Files
- `fair_lens.ipynb` – main Jupyter or Colab notebook  
- `fair_lens_app.py` – Streamlit dashboard application  
- `bias_terms.json` – sample dictionary of exclusionary terms  
- `requirements.txt` – dependency file  

---

## Evaluation Dimensions
| Dimension | Max Points | Description |
|------------|-------------|--------------|
| Readability | 25 | How easy the text is to read and understand |
| Tone and Sentiment | 15 | Measures tone neutrality and accessibility |
| Bias / Exclusion Detection | 25 | Flags exclusionary or outdated phrasing |
| Accessibility and Plain Language | 20 | Evaluates sentence complexity and clarity |
| Transparency and Actionability | 15 | Checks for presence of rationale, sources, or next steps |

**Total:** 100 points  

---

