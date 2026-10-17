# Chapter 7 — How to Picture Neural Networks: In Your Head and on Paper

Layer diagrams, and looking *inside* trained networks (scikit-learn 8x8 digits).

## What's covered

| Section | Concepts |
|---|---|
| Diagrams | layer diagrams and weight counts for a network (64-24-10 has 1776 weights; 64-128-128-10 has 25,856) |
| Weights as pictures | a one-layer net's weights for "is a 3" compared with the pixel–target correlation map (r ≈ 0.54) |
| One layer | 10 weight templates, one per digit (train ≈ 0.95, test ≈ 0.94) |
| Hidden layer | 64-24-10 network (train ≈ 0.96, test ≈ 0.95), hidden-unit pictures, activation heatmap |
| Spurious correlation | a planted "sticker" feature: train ≈ 1.00 but test ≈ 0.47, versus ≈ 0.90 without it |

## Key takeaway

A network is just correlation-finding machinery: weights can be drawn as pictures and read. That is powerful, but it also means the network will happily use a spurious feature that disappears at test time.

## Files

- `chapter07_picturing_neural_networks.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter07_picturing_neural_networks.ipynb
```
