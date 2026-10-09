# Chapter 2 — Fundamental Concepts: How Do Machines Learn?

Another conceptual chapter. The notebook explains the vocabulary of the book and adds small scikit-learn demos (added by me,
not from the book) so each definition can be seen on data.

## What's covered

| Section | Concepts | Demo |
|---|---|---|
| What "learning" means | adjusting internal numbers so outputs improve | — |
| Supervised learning | labelled examples, classification vs regression | logistic regression + decision regions |
| Unsupervised learning | structure without labels, clustering | k-means on hidden-label blobs |
| Parametric vs non-parametric | fixed vs data-dependent number of parameters | line / polynomial / k-NN on a noisy sine |
| The 2×2 map | supervised/unsupervised × parametric/non-parametric | table |
| Why deep learning is supervised-parametric | neural nets = fixed set of weights trained on labelled data | — |
| Predict → Compare → Learn | the training loop used from Chapter 3 on | 8-step toy loop |

## Key takeaway

Two independent axes classify learning methods. Deep learning mostly lives in "supervised parametric learning", trained by a
**Predict → Compare → Learn** loop.

## Files

- `chapter02_fundamental_concepts.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter02_fundamental_concepts.ipynb
```
