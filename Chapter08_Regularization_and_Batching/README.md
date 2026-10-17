# Chapter 8 — Learning Signal and Ignoring Noise: Regularization and Batching

Overfitting, early stopping, L2, dropout and mini-batches, on 300 training digits with 25% wrong labels.

## What's covered

| Section | Concepts |
|---|---|
| Overfitting | train accuracy → 0.98 while test falls from 0.90 (epoch ≈ 53) to 0.83; the net fits ~92% of the wrong labels |
| Early stopping | validation set picks the epoch: test 0.894 |
| L2 / weight decay | $w\leftarrow(1-\alpha\lambda)w-\alpha\,\partial E/\partial w$; best λ=1e-2 gives test 0.927; λ=3e-2 is too strong |
| Dropout | inverted dropout (mask/keep), same mask in backprop (gradient-checked); keep 0.5 gives test 0.889 |
| Mini-batches | batch 300/100/20/5: more updates per epoch, faster fitting, and faster overfitting |
| Comparison | 5 seeds, mean ± std table and bar chart |

## Key takeaway

The goal is low error on *new* data, not low training error. Early stopping, weight decay and dropout all push the network towards signal rather than noise (results from one small noisy setup).

## Files

- `chapter08_regularization_and_batching.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter08_regularization_and_batching.ipynb
```
