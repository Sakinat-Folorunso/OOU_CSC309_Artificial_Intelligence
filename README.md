# CSC 309 Artificial Intelligence: Practical Notebooks

Lab work for **CSC 309 Artificial Intelligence** (2 units; LH 15, PH 45), Department of Computer Sciences, Olabisi Onabanjo University, Ago-Iwoye. Lecturer: Dr Sakinat Folorunso.

The twelve notebooks are the practical half of the course. Each one matches a chapter of the class note in `docs/` (same weeks, same notation, same worked numbers) and the CCMAS learning outcomes (LO 1 to LO 8).

## Weekly plan

| Week | Topic | CCMAS LO | Open in Colab |
|:-:|:--------------------------|:--:|:--|
| 1 | Turing test, Chinese Room, rational choice | 1, 3 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week01_Turing_Test_Practical_Student_Centred.ipynb) |
| 2 | Agents, PEAS, environments, belief update | 2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week02_Intelligent_Agents_Student_Centred.ipynb) |
| 3 | Uninformed search, combinatorial explosion | 5 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week03_Search_BFS_DFS_Student_Centred.ipynb) |
| 4 | A*, heuristics, trade-offs (CA 1) | 4, 5 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week04_Astar_CA1_Student_Centred.ipynb) |
| 5 | Predicate logic, clause form, resolution | 6, 7 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week05_KRR_Logic_Student_Centred.ipynb) |
| 6 | Semantic networks and frames | 6 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week06_Semantic_Networks_Frames_Student_Centred.ipynb) |
| 7 | TF-IDF retrieval, Naive Bayes spam (CA 2) | 7 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week07_NLP1_QA_Spam_CA2_Student_Centred.ipynb) |
| 8 | Sentiment, spelling, MT, speech | 7 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week08_NLP2_Sentiment_Spelling_MT_Student_Centred.ipynb) |
| 9 | Expert systems, certainty factors | 8 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week09_Expert_Systems_Student_Centred.ipynb) |
| 10 | Vision, face verification, robots | 8 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week10_AI_Languages_Vision_Robots_Student_Centred.ipynb) |
| 11 | Boids, ants, message passing (CA 3) | 2, 5 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week11_Agent_Simulations_Student_Centred.ipynb) |
| 12 | Campus assistant and responsible AI | 1–8 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sakinat-Folorunso/OOU_CSC309_Artificial_Intelligence/blob/main/notebooks/CSC309_Week12_Integration_Mock_Practical_Student_Centred.ipynb) |

Continuous assessment: **CA 1** (Week 4), **CA 2** (Week 7), **CA 3** (Week 11), 10 marks each. The practical rubric is Table 0.3 of the class note.

## How to use a notebook

1. Click **Open in Colab** (a free Google account is enough).
2. Run the **Setup** cell. It fixes `SEED = 42`, so your numbers should match your classmates' and the class note.
3. Work from top to bottom and edit only cells marked `# TODO(Student)`.
4. Each task ends with an **auto-check** (✅ or ❌). Keep going until it is ✅. *Run all* is safe: unfinished tasks report ❌ instead of crashing.
5. Finish with the **Reflection**, and the **Extensions** if you have time.

To work offline, install Python 3.10 or later and run `pip install -r requirements.txt`, then open the notebooks with Jupyter.

## Repository layout

```
notebooks/   twelve student notebooks (TODO stubs, no solutions)
docs/        the class note (Word, native equations)
requirements.txt
.github/workflows/check-notebooks.yml   runs every notebook headless on each push
```

Instructor solutions are **not** in this repository. Keep them in a private repository or a local folder.

## Reproducibility notes

- Every random draw uses seed 42.
- Some notebooks try to download public data (Olivetti faces in Week 10, NLTK corpora and a translation model in Week 8) and fall back to a bundled stand-in if the download fails. The numbers printed in the class note for these experiments come from the stand-in data (for example, scikit-learn digits in Week 10), so a run on Colab with the real data may give different values. Compare patterns, not exact digits.
- Weeks 1 to 7 and 9 to 12 need only NumPy, SciPy, Matplotlib and scikit-learn.

## Licence

Released under the **MIT License** (see `LICENSE`). Copyright (c) 2026 Sakinat Folorunso.

## Citation

See `CITATION.cff`.

## How each notebook is written
- **Student-centred:** learning objectives with Bloom levels, a *Lab tasks at a glance* table, short explanations before each block of code, and a *code walkthrough* for the harder cells.
- **Every line of code has a plain-English comment above it.** Read the comment, predict the result, then run the cell.
- **Lab tasks** (`TODO(Student)` cells with ✅/❌ auto-checks), then an **Assignment** (marks and submission rule), a **Reflection**, and optional **Extensions** in every week. Weeks 4, 7 and 11 carry the three CA deliverables.
