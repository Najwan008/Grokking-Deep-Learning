# Chapter 9 — Modeling Probabilities and Nonlinearities: Activation Functions

Activations, softmax, cross-entropy and vanishing gradients.

## What's covered

| Section | Concepts |
|---|---|
| Activations | ReLU, sigmoid, tanh and their derivatives (numerically checked); what makes a good activation |
| Softmax | scores → probabilities; shift invariance and the max-subtraction stability trick |
| Cross-entropy | $L=-\log\hat p_c$ and the gradient $\hat p-y$ (numerically checked) |
| MSE vs softmax+CE | both reach ≈ 97% test accuracy; softmax+CE learns faster (0.935 vs 0.902 after 5 epochs) |
| Vanishing gradients | 5 hidden layers: sigmoid fails (≈ 0.09 test accuracy); tanh (0.988) and ReLU (0.968) train well |

## Key takeaway

Hidden layers need non-saturating activations; a classification output wants softmax with cross-entropy, whose gradient is simply *prediction − target*.

## Files

- `chapter09_activation_functions.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter09_activation_functions.ipynb
```
