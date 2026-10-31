<div align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,6,20&height=280&section=header&text=AI%20Research%20Lab&fontSize=64&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Learn%20deeply%20%E2%80%A2%20Experiment%20carefully%20%E2%80%A2%20Build%20evidence&descSize=20&descAlignY=58" alt="AI Research Lab" width="100%"> <br> <picture> <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=1000&color=A78BFA&center=true&vCenter=true&width=700&height=40&lines=From+fundamentals+to+reproducible+experiments;Data+%E2%86%92+Models+%E2%86%92+Evidence;A+disciplined+path+into+AI+research"> <img alt="Typing animation" src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=1000&color=6D28D9&center=true&vCenter=true&width=700&height=40&lines=From+fundamentals+to+reproducible+experiments;Data+%E2%86%92+Models+%E2%86%92+Evidence;A+disciplined+path+into+AI+research"> </picture>
<br><br>
<a href="./LEARNING_PATH.md"><img src="https://img.shields.io/badge/START%20HERE-LEARNING%20PATH-19b8d5?style=for-the-badge&labelColor=101a2d" alt="Learning path"></a>   <a href="./book/BOOK_BLUEPRINT.md"><img src="https://img.shields.io/badge/RESEARCH%20BOOK-BLUEPRINT-9876f5?style=for-the-badge&labelColor=101a2d" alt="Research book"></a>   <a href="https://tejas-c-0.github.io/AI-Research-Lab/3d-explorer/"><img src="https://img.shields.io/badge/INTERACTIVE-3D%20EXPLORER-20b68b?style=for-the-badge&labelColor=101a2d" alt="3D explorer"></a>
<br><br>
</div>
[!IMPORTANT] Core principle: Understand the problem before the model. Understand the data before training. Evaluate evidence before making claims.
<br>
This is a structured workspace for learning, experimenting with, and documenting AI. It is not just a pile of notes. It is a path that takes you from fundamentals to experiments to evidence.
<br><br>
🧬 3D Explorer
<a href="https://tejas-c-0.github.io/AI-Research-Lab/3d-explorer/"> <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=6,11,20&height=150&section=header&text=%E2%96%B6%20%20Launch%20the%203D%20Explorer&fontSize=36&fontColor=ffffff&animation=twinkling" alt="Launch the 3D explorer" width="100%"> </a> <br>
Three live Three.js scenes you can play with:
- 🧠 Neural network: inspect the input, hidden, and output nodes
- 🔬 Research pipeline: walk through data, preparation, model, evaluation, and prediction
- 🗂️ Dataset: look at rows, columns, feature values, and target values
Drag to rotate, scroll or pinch to zoom, and click any object to read what it means.
<br><br>
📖 Learning Notes
Read them in this order. Each note builds on the one before it.
<br>
#NoteWhat you will learn01AI Research FoundationsResearch problems, gaps, hypotheses, and experiments02Structure of a Research PaperWhat each section of a paper is for03Reading and Analysing a Research PaperHow to judge the method, the evidence, and the limits04Understanding Data and Model EvaluationDatasets, training and testing, metrics05Types of Data, Features and TargetsNumerical and categorical data, features, targets06Understanding Data CleaningMissing, duplicate, invalid, and inconsistent data
<br>
[!TIP] Coming next: Machine Learning Research: From Question to Evidence, a planned beginner-friendly handbook of about 100 pages on research questions, experiment design, evaluation, and reproducibility.
<br><br>
🧭 Roadmap
Click any stage to open it.
<br> <details> <summary><b>🧱 &nbsp;Stage 1 · Foundations</b></summary> <br>
- 🐍 Python: syntax, functions, modules, error handling, virtual environments
- 📊 Data science tools: NumPy, Pandas, Matplotlib, Seaborn, Jupyter
- 🗃️ Understanding data: features and targets, cleaning, exploratory analysis
- 📐 Maths and statistics: vectors, matrices, probability, correlation, gradients
<br> </details> <details> <summary><b>🤖 &nbsp;Stage 2 · Machine Learning</b></summary> <br>
- 🎓 Basics: supervised and unsupervised learning, generalisation
- 🌲 Methods: linear and logistic regression, decision trees, random forests, SVM, clustering
- 🎯 Evaluation: metrics, overfitting, cross-validation, data leakage, error analysis
<br> </details> <details> <summary><b>🚀 &nbsp;Stage 3 · Deep Learning and Research</b></summary> <br>
- 🧠 Deep learning: neural networks, backpropagation, CNNs, sequence models, Transformers
- 🔬 Research practice: research questions, baselines, reproducibility, paper analysis
- 🛠️ Applied projects: build, document, evaluate, and explain
<br> </details> <br><br>
🔬 Research Workflow
Every experiment follows the same path, so every result can be traced.
<br>






next experiment
Problem
Question
Dataset
Method
Experiment
Evaluation
Limitations
<br>
[!NOTE] Experiment rules
1. Start with a simple baseline.
2. Keep train, validation, and test data separate. Never tune on the test set.
3. Record datasets, preprocessing, parameters, and random seeds.
4. Compare methods under the same protocol.
5. Report failures too, and claim only what the evidence supports.
<br> <details> <summary><b>📚 &nbsp;How to read a research paper</b></summary> <br>
Look forAsk yourselfProblem and objectiveWhat is being solved, and why?Related work and gapWhat was tried before, and what is missing?Method and datasetWhat is proposed, and on which data?Evaluation and resultsWhich metrics and baselines back the claims?LimitationsWhat can we not conclude?
Rule: separate what the authors demonstrate from what you infer.
<br> </details> <br><br>
🌌 From Data to Prediction
The five stages behind almost every machine learning system.
<br>



🟦 Data<sub> raw observations</sub>
🟩 Preparation<sub> clean and transform</sub>
🟪 Model<sub> learn patterns</sub>
🟨 Evaluation<sub> measure evidence</sub>
🟥 Prediction<sub> use the output</sub>
<br><br>
🧠 How a Neural Network Learns
Output layer
Hidden layer
Input layer















x₁
x₂
x₃
h₁
h₂
h₃
h₄
ŷ
<br>
The input layer receives the features. The hidden layers learn useful patterns. The output layer makes the prediction. During training, the weights are adjusted a little at a time to reduce the error:
$$\theta \leftarrow \theta - \eta \, \nabla_{\theta}\, \mathcal{L}(\theta)$$<sub>Illustrative diagram only. It is not a trained model or a measured result.</sub>
<br><br>
⚙️ Toolkit
<div align="center"> <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img alt="NumPy" src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white"> <img alt="Pandas" src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"> <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"> <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"> <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
<sub>These are the planned tools. Not all of them are set up in the repository yet.</sub>
</div> <br><br>
🚀 Getting Started

bash
git clone https://github.com/Tejas-c-0/AI-Research-Lab.gitcd AI-Research-Lab
<br>
👤 Maintainer
Tejas C. · @Tejas-c-0
<br> <div align="center">
Learn the fundamentals. Question assumptions. Test ideas. Share reproducible work.
<sub>Curiosity → Understanding → Experimentation → Evidence</sub>
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,6,20&height=140&section=footer" alt="" width="100%"> </div>
