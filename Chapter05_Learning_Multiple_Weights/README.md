# Chapter 5 — Learning Multiple Weights at a Time: Generalizing Gradient Descent

Gradient descent with many inputs, many outputs and many examples.

## What's covered

| Section | Concepts |
|---|---|
| Several inputs | gradient $\partial E/\partial w_i = 2\delta x_i$; each weight's update is proportional to its own input |
| Convergence | signed error shrinks by $1-2\alpha\lVert x\rVert^2$ each step (checked); zero input → zero update (checked) |
| Where learning ends | a single example has infinitely many solutions; GD finds the one closest to the start (formula verified) |
| Freezing a weight | the error still reaches ~0 because the other weights compensate — weights are coupled |
| Several outputs | gradient is an outer product $2\,\boldsymbol\delta\,\mathbf x^\top$; analytic vs numerical gradient check |
| A whole dataset | batch gradient $\tfrac2N(\hat Y-Y)^\top X$; the network recovers a hidden "true" weight matrix |

## Key takeaway

Same recipe as Chapter 4, applied to every weight: **error × input** tells each weight how much to change. One example cannot
pin down the weights; a dataset can. Always verify a derived gradient numerically.

## Files

- `chapter05_learning_multiple_weights.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter05_learning_multiple_weights.ipynb
```
