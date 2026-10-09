# Grokking Deep Learning — Code Reproduction & Theoretical Deep-Dive

Individual assignment (Enrichment for Deep Learning classes): reproduce the code of every chapter of
*grokking Deep Learning* (Manning), summarize each chapter in its own notebook, and explain the underlying theory.

The book builds neural networks from scratch with NumPy before ever touching a framework. This repository follows the same
path: every notebook uses plain NumPy, checks its math numerically where possible, and has been **executed end to end** (all
outputs and charts are saved in the notebooks).

**Reference book:** [grokking Deep Learning (Manning)](https://www.manning.com/books/grokking-deep-learning)

## Repository structure

Each chapter folder contains a Jupyter notebook (theory + code + outputs), a short README summarizing the chapter, and an
`outputs/` folder with the saved charts.

| Chapter | Topic | Status |
|---|---|---|
| 1 | [Introducing Deep Learning: Why You Should Learn It](Chapter01_Introducing_Deep_Learning/) | ✅ Done |
| 2 | [Fundamental Concepts: How Do Machines Learn?](Chapter02_Fundamental_Concepts/) | ✅ Done |
| 3 | [Introduction to Neural Prediction: Forward Propagation](Chapter03_Forward_Propagation/) | ✅ Done |
| 4 | [Introduction to Neural Learning: Gradient Descent](Chapter04_Gradient_Descent/) | ✅ Done |
| 5 | [Learning Multiple Weights at a Time](Chapter05_Learning_Multiple_Weights/) | ✅ Done |
| 6 | [Building Your First Deep Neural Network: Backpropagation](Chapter06_Backpropagation/) | ✅ Done |
| 7–10 | to be added (deadline: 17 Oct 2026) | ⏳ Pending |

## Chapter summaries

**Chapter 1 — Introducing Deep Learning.** Motivates the subject: deep learning is the part of machine learning that uses
many-layered neural networks whose weights are learned from data. Explains why it is worth learning, why the book builds
everything from scratch, and introduces two mental models used throughout: *data + answers → rules* and *learning = moving downhill
on an error landscape*.

**Chapter 2 — Fundamental Concepts.** Defines what it means for a machine to learn and classifies learning methods along two
independent axes: supervised vs unsupervised (are the right answers available?) and parametric vs non-parametric (is the number of
adjustable numbers fixed?). Introduces the **Predict → Compare → Learn** loop that organizes the following chapters.

**Chapter 3 — Forward Propagation.** The *Predict* step. A neuron multiplies inputs by weights and sums them (a dot product); a
layer is a matrix–vector product; a batch is a matrix–matrix product. Shows multiple inputs, multiple outputs, stacked layers, and why
stacking purely linear layers collapses into a single layer.

**Chapter 4 — Gradient Descent.** The *Compare* and *Learn* steps for a single weight. Squared error, the naive hot-and-cold method,
the derivative of the error derived with the chain rule and checked numerically, the update rule $w \leftarrow w - \alpha\,dE/dw$, and
an exact analysis of how the learning rate decides between slow convergence, fast convergence and divergence.

**Chapter 5 — Learning Multiple Weights.** Gradient descent generalized to many inputs, outputs and examples: each weight's update is
the error times its own input; the gradient for a weight matrix is an outer product. Includes freezing a weight, a numerical gradient
check, and a dataset experiment where the network recovers a hidden true weight matrix.

**Chapter 6 — Backpropagation.** Why one layer cannot learn patterns with no direct input–output correlation (XOR-style), how a
non-linearity (ReLU) fixes this, and how the hidden layer is trained by sending the output error *backwards* through the weights.
Includes a gradient check, training results, an experiment on why narrow layers can fail (dead ReLU units), and a general
backpropagation for any depth.

## Setup

```bash
pip install -r requirements.txt
jupyter notebook
```

All notebooks run in a few seconds on a CPU. Each notebook is self-contained and creates its own `outputs/` folder, so it can also be
uploaded to Google Colab on its own.

## Notes on originality and tools

- The book's concepts and chapter order are followed, but the **toy examples and datasets are my own** (e.g. a drink-stall sales
  predictor, a two-switch lamp problem) rather than copies of the book's examples.
- Chapters 1–2 are conceptual in the book; their notebooks are written explanations plus small demos that are clearly marked as additions.
- As allowed by the assignment guidelines, an LLM was used to help draft the theoretical explanations. All code was executed, and the
  gradient formulas are verified against numerical gradients inside the notebooks.
