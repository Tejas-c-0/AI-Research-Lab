# Book Blueprint — Machine Learning Research: From Question to Evidence

> **Working title:** *Machine Learning Research: From Question to Evidence*  
> **Subtitle:** *A beginner-friendly field guide to reading papers, designing experiments, evaluating models, and writing reproducible research*  
> **Target length:** approximately 100 designed pages  
> **Audience:** undergraduate computer-science students and beginning ML researchers  
> **Status:** planning and source verification

## 1. What this book is — and is not

This is a practical handbook for **doing research that uses machine learning**. It is not a complete machine-learning textbook, a catalogue of every algorithm, or a Python programming course.

It will teach the machine-learning concepts that a researcher must understand to make sound research decisions:

- How to define a prediction or analysis task.
- How to understand datasets, features, targets, and labels.
- How to choose a reasonable baseline and justify a model family.
- How to split data and avoid leakage.
- How to select metrics that match the research question.
- How to analyse generalisation, uncertainty, and errors.
- How to compare methods fairly and make evidence-supported claims.
- How to read, write, reproduce, and communicate ML research.

Algorithms will be explained to the depth needed to understand research papers and design experiments. Detailed implementation tutorials belong in separate notebooks or companion lessons.

## 2. Learning outcomes

By the end, a reader should be able to:

1. Turn a broad interest into a focused, researchable question.
2. Search for and critically read relevant research papers.
3. Explain the dataset, task, features, target, and assumptions in an ML study.
4. Select a baseline, model family, and evaluation protocol with a reason.
5. Design experiments that reduce bias, leakage, and unfair comparisons.
6. Interpret metrics and results without overstating their meaning.
7. Document code, data, parameters, and limitations for reproducibility.
8. Draft a structured research report or paper.
9. Prepare a research presentation and respond to critical questions.

## 3. Proposed 100-page structure

The page counts below are a design budget. Final pagination will depend on trim size, typography, diagrams, and layout.

| Part | Content | Pages |
|---|---|---:|
| Front matter | Title, copyright, preface, how to use this book | 6 |
| I | Thinking like a researcher | 14 |
| II | Machine-learning foundations for research | 16 |
| III | Designing a sound ML study | 16 |
| IV | Running and analysing experiments | 18 |
| V | Writing, reviewing, and publishing research | 16 |
| VI | Guided end-to-end case study | 8 |
| Appendices | Checklists, templates, glossary, references | 6 |
| **Total** |  | **100** |

### Front matter — 6 pages

- Title and subtitle — 1
- Copyright and publication information — 1
- Preface: why ML research needs more than model building — 2
- How to use the book and its diagrams/checklists — 2

### Part I — Thinking Like a Researcher — 14 pages

**Chapter 1. What Research Actually Does — 3 pages**
- Research versus ordinary development
- Evidence, claims, and uncertainty
- Basic research ethics and intellectual honesty

**Chapter 2. From an Interest to a Research Question — 4 pages**
- Topic, problem, objective, question, and hypothesis
- Scope and feasibility
- Turning vague questions into answerable questions

**Chapter 3. Finding and Reading Prior Work — 4 pages**
- Search terms, scholarly search engines, and citation chaining
- Screening for relevance and credibility
- Three-pass paper reading
- Building a literature matrix

**Chapter 4. Research Gaps and Contributions — 3 pages**
- Limitations versus genuine research gaps
- Novelty and contribution types
- How to avoid claiming “first” without evidence

### Part II — Machine-Learning Foundations for Research — 16 pages

**Chapter 5. Understand the Learning Task — 2 pages**
- Regression, classification, clustering, and other task families
- Inputs, outputs, assumptions, and intended use

**Chapter 6. Understand the Dataset — 4 pages**
- Observations, features, targets, labels, and metadata
- Numerical and categorical variables
- Sampling, missingness, duplicates, outliers, and data quality
- Representativeness and dataset documentation

**Chapter 7. Models as Research Methods — 4 pages**
- Baselines and why they matter
- Linear models, tree-based methods, support vector machines, and neural networks at a conceptual level
- Model capacity, assumptions, interpretability, and cost
- Choosing a model for a question, not for popularity

**Chapter 8. Generalisation and Data Splitting — 3 pages**
- Training, validation, and test roles
- Overfitting and underfitting
- Data leakage and common traps

**Chapter 9. Evaluation Metrics — 3 pages**
- Regression and classification metrics
- Class imbalance and threshold choices
- Metric alignment with the research objective

### Part III — Designing a Sound ML Study — 16 pages

**Chapter 10. From Question to Experimental Protocol — 4 pages**
- Hypotheses and measurable outcomes
- Independent, dependent, and control variables
- Defining inclusion/exclusion criteria and evaluation protocol

**Chapter 11. Data Preparation Without Leakage — 3 pages**
- Preprocessing pipelines
- Missing-value handling and encoding
- Fit transformations on training data only

**Chapter 12. Baselines, Comparisons, and Ablations — 3 pages**
- Choosing meaningful baselines
- Fair comparison conditions
- Ablation studies and component analysis

**Chapter 13. Statistics and Uncertainty — 3 pages**
- Variability across splits and random seeds
- Confidence intervals and statistical tests at an introductory level
- Practical significance versus statistical significance

**Chapter 14. Ethics, Privacy, and Responsible ML — 3 pages**
- Data consent, licences, and privacy
- Bias, fairness, and subgroup performance
- Security, misuse, and limitations

### Part IV — Running and Analysing Experiments — 18 pages

**Chapter 15. Reproducible Experiment Setup — 4 pages**
- Versioning data, code, and configurations
- Random seeds and environment records
- Experiment logs and reproducibility checklists

**Chapter 16. Reading Results Correctly — 4 pages**
- Tables, plots, and metric interpretation
- Error analysis and failure cases
- Avoiding cherry-picking and overclaiming

**Chapter 17. Robustness and Validity Checks — 3 pages**
- Sensitivity analysis
- Distribution shift and external validity
- Sanity checks and negative results

**Chapter 18. Literature Synthesis During the Study — 4 pages**
- Compare methods, datasets, and protocols
- Evidence matrices and thematic synthesis
- Locate disagreements and unresolved limitations

**Chapter 19. Research Artefacts — 3 pages**
- Code, notebooks, datasets, model cards, and data statements
- What to share and what not to share
- Documentation for another researcher

### Part V — Writing, Reviewing, and Publishing Research — 16 pages

**Chapter 20. Anatomy of an ML Research Paper — 3 pages**
- Title, abstract, introduction, related work
- Methodology, experiments, results, discussion, conclusion

**Chapter 21. Writing Methods and Experiments — 3 pages**
- Enough detail to reproduce the study
- Dataset and split descriptions
- Hyperparameters, baselines, and implementation details

**Chapter 22. Results, Discussion, and Limitations — 3 pages**
- Separate observed results from interpretation
- Explain negative or mixed results
- State limitations and threats to validity

**Chapter 23. Citations and Research Integrity — 2 pages**
- Attribution, paraphrasing, and quotation
- Reference managers and citation checking
- Plagiarism, fabricated references, and responsible AI assistance

**Chapter 24. Peer Review and Publication — 3 pages**
- Conference and journal scope
- Submission checklists and peer review
- Preprints, copyright, licences, and publication ethics
- Responding to reviewers professionally

**Chapter 25. Research Presentations — 2 pages**
- A clear research story
- Figures and posters
- Answering questions about evidence and limitations

### Part VI — Guided End-to-End Case Study — 8 pages

A clearly labelled teaching case (not a fabricated published result):

1. Choose a feasible house-price prediction question.
2. Review related work and define the gap carefully.
3. Inspect and document a dataset.
4. Establish a simple baseline.
5. Choose a valid split and evaluation metrics.
6. Compare methods under one protocol.
7. Analyse errors and limitations.
8. Turn the work into a short research report.

Any numerical results used in this case study must be explicitly marked as synthetic demonstration data unless generated by a documented, reproducible experiment.

### Appendices — 6 pages

- Research question checklist — 1
- Paper-reading and literature matrix template — 1
- Experiment protocol and log template — 1
- Reproducibility and submission checklist — 1
- Glossary — 1
- Selected references and further reading — 1

## 4. The book's teaching format

Each chapter should include:

1. **Core idea** — plain-language explanation.
2. **Why researchers need it** — the research decision it supports.
3. **Visual explanation** — diagram, workflow, or comparison.
4. **Worked example** — a small, carefully labelled example.
5. **Common mistakes** — what beginners frequently misunderstand.
6. **Research checklist** — questions to ask in practice.
7. **Short exercise** — check understanding.
8. **References** — reliable primary sources or textbooks.

Use the same visual language throughout:

- 🟦 Blue/cyan — data and evidence inputs
- 🟩 Green — preparation and validation
- 🟪 Purple — models and methods
- 🟨 Amber — evaluation and analysis
- 🟥 Coral — predictions, decisions, and outputs

Use labels as well as colours for accessibility.

## 5. Source books and references to study alongside this book

These are supporting references, not text to copy. The handbook must be written in original language and cite all ideas, figures, and quotations appropriately.

### Start here

- **An Introduction to Statistical Learning with Applications in Python** — Gareth James, Daniela Witten, Trevor Hastie, Robert Tibshirani, and Jonathan Taylor. Best starting reference for statistical learning concepts and practical Python labs. The official author website provides the Python edition and related resources: https://www.statlearning.com/

### Research process and writing

- **The Craft of Research, 5th edition** — Wayne C. Booth, Gregory G. Colomb, Joseph M. Williams, Joseph Bizup, and William T. FitzGerald. Useful for shaping questions, evaluating sources, building arguments, and research ethics. Publisher: https://press.uchicago.edu/ucp/books/book/chicago/C/bo215874008
- **Writing for Computer Science, 3rd edition** — Justin Zobel. Useful for computer-science research methods, experiments, figures, papers, and ethics. Publisher: https://link.springer.com/book/10.1007/978-1-4471-6639-9
- **How to Read a Paper** — S. Keshav. A short paper introducing the three-pass reading method: https://svr-sk818-web.cl.cam.ac.uk/keshav/publications/htrap.html

### Deeper machine-learning theory — later reference

- **Deep Learning** — Ian Goodfellow, Yoshua Bengio, and Aaron Courville. Use selected chapters when deep-learning theory is needed. The authors' online version is available at https://www.deeplearningbook.org/
- **Probabilistic Machine Learning: An Introduction** — Kevin P. Murphy. A more mathematical reference for probability, statistics, linear models, neural networks, and learning theory. Publisher: https://mitpress.mit.edu/9780262046824/probabilistic-machine-learning/

### Reading order for these references

1. Begin with *An Introduction to Statistical Learning with Applications in Python* alongside the ML foundations chapters.
2. Read *How to Read a Paper* before building a large literature review.
3. Use *The Craft of Research* when developing research questions and arguments.
4. Use *Writing for Computer Science* while drafting methods, experiments, and the manuscript.
5. Refer to Goodfellow or Murphy only when the project requires deeper theory.

Do not try to read every reference cover-to-cover before beginning research. Read selectively to answer a concrete question, and record what you learned.

## 6. How we will author the book

1. **Freeze the scope and table of contents.** Do not expand it into a general ML encyclopaedia.
2. **Draft one chapter at a time.** Each chapter must pass a beginner-comprehension check.
3. **Verify technical claims.** Use primary papers, official documentation, and reputable textbooks.
4. **Create original diagrams.** Keep source files and captions; do not copy copyrighted figures.
5. **Add practical templates.** A reader should be able to use the checklists and logs in a real study.
6. **Cross-review chapters.** Check consistency, terminology, examples, and references.
7. **Edit the whole manuscript.** Check structure, clarity, citations, plagiarism risk, and page budget.
8. **Prepare publication files.** Create a clean PDF and editable source, then proofread the rendered pages.
9. **Publish only after a rights and quality check.** Confirm image licences, quotations, author credit, publisher/platform requirements, and any required metadata.

## 7. Quality rules

- Never invent papers, citations, datasets, experimental results, or performance numbers.
- Mark hypothetical examples as hypothetical.
- Do not imply that correlation proves causation.
- Do not treat one test score as proof of general superiority.
- Explain the assumptions behind metrics and methods.
- Distinguish an author's claim from independently supported evidence.
- Keep citations close to the statements they support.
- Use original diagrams or assets with documented rights.
- Keep a version history and acknowledge substantial contributions.

**Definition of done:** A reader with introductory programming and basic data familiarity can use the book to plan, conduct, document, evaluate, and communicate a small, responsible ML research study.
