# MFE RP1 — Constructing Hedge Portfolios with Neural Networks
**Group:** Micaela, Kaiden, Siphelele, Glasson
**Affiliation:** African Institute of Financial Markets and Risk Management

---

## Deadlines
| Deliverable | Due |
|---|---|
| Broad Literature Review | Mon 13 April 2026, 22:00 |
| Research Paper + Code (.zip) | Fri 26 June 2026, 12:00 |
| Presentation + Oral Exam | Tentatively 31 July / 3 August 2026 |

## Marking
`0.1 × Lit Review + 0.45 × Presentation + 0.45 × Research Paper`

---

## Folder Structure

```
MFE RP 1/
│
├── STRUCTURE.md                   ← this file
│
├── paper/                         ← research paper (6 000–8 000 words)
│   ├── main.tex                   ← MASTER FILE — compile this
│   ├── references.bib             ← shared BibTeX database
│   ├── figures/                   ← all figures (.pdf or .png)
│   │
│   ├── abstract/
│   │   └── abstract.tex
│   ├── introduction/
│   │   └── introduction.tex
│   ├── literature_review/
│   │   └── literature_review.tex
│   ├── methods/
│   │   └── methods.tex
│   ├── results/
│   │   └── results.tex
│   ├── conclusion/
│   │   └── conclusion.tex
│   └── appendices/
│       ├── appendix_code.tex
│       └── appendix_ai.tex
│
├── lit_review/                    ← broad literature review (3 000–4 000 words)
│   └── lit_review.tex             ← compile this; references ../paper/references.bib
│
├── code/                          ← Python source files / Jupyter notebooks
│   ├── simulate.py
│   ├── model.py
│   ├── train.py
│   ├── evaluate.py
│   └── utils.py
│
└── data/                          ← saved model weights, generated datasets
```

---

## Compiling LaTeX

### Research paper (compile from inside `paper/`)
```bash
cd paper
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### Literature review (compile from inside `lit_review/`)
```bash
cd lit_review
pdflatex lit_review.tex
bibtex lit_review
pdflatex lit_review.tex
pdflatex lit_review.tex
```

---

## Saving figures from Python
Save figures as **PDF** (vector graphics) for crisp rendering in LaTeX:

```python
fig.savefig('../paper/figures/learning_curve.pdf', bbox_inches='tight')
```
