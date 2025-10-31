FAIR-Lens – Auditing Generative AI for Civic and Public-Sector Use

FAIR-Lens is a prototype auditing tool that evaluates the outputs of generative AI systems (chatbots, assistants, LLM-powered forms) against responsible AI criteria relevant to government and social-impact projects. It is designed for teams like the Burnes Center’s AI for Impact program who are deploying AI to serve vulnerable populations and need a fast way to check for bias, clarity, and accessibility.

This project complements civic AI products such as FAIR (Fast AI-Assisted Investigation & Review), GENIE, and A-IEP by providing a transparency layer. Instead of just generating content, FAIR-Lens tells you whether the content is readable, neutral, inclusive, and explainable.

What It Does
	•	Takes any AI-generated text as input
	•	Runs a set of evaluations:
	•	readability (Flesch-Kincaid)
	•	tone and sentiment
	•	biased / exclusionary phrasing detection
	•	accessibility and plain-language score
	•	transparency (whether rationale / sources / next steps are present)
	•	Produces a 0–100 “Responsible AI Score”
	•	Provides suggestions for improvement
	•	Can optionally call an LLM to re-write the text in a more inclusive/public-facing style

Why This Matters

Public-sector AI must not only be accurate but also:
	•	understandable to non-technical residents
	•	inclusive of people with language or accessibility needs
	•	free from obvious bias or exclusionary phrasing
	•	auditable by human staff

FAIR-Lens shows that LLM engineering and AI governance can be implemented together.

Features
	•	Text scoring function
	•	Streamlit dashboard to paste text and get score
	•	Optional LLM-based rewrite
	•	Keyword dictionaries for common civic bias issues
	•	Exportable JSON report

Tech Stack
	•	Python 3.x
	•	textstat (for readability)
	•	textblob or nltk/vader (for sentiment)
	•	spaCy (for NLP)
	•	Streamlit (dashboard)
	•	OpenAI API (for rewrite / improve mode)

Files
	•	fair_lens.ipynb – main notebook
	•	fair_lens_app.py – Streamlit app
	•	bias_terms.json – sample dictionary
	•	requirements.txt

Evaluation Dimensions
	1.	Readability (0–25 pts)
	2.	Tone and Sentiment (0–15 pts)
	3.	Bias / Exclusion detection (0–25 pts)
	4.	Accessibility and plain language (0–20 pts)
	5.	Transparency and actionability (0–15 pts)

Total: 100 pts

Getting Started
	1.	Clone the repo
	2.	Install requirements
	3.	Run streamlit run fair_lens_app.py
	4.	Paste in any LLM output and review the report

Notes
	•	This is not a legal/compliance tool
	•	Always add domain-specific bias rules for education, health, or housing contexts
	•	Do not expose API keys in public repos
