# Chapter 10 — Intro to Convolutional Neural Networks: Reusing Weights in Multiple Places

Convolution from scratch in NumPy, with a CNN vs dense comparison.

## What's covered

| Section | Concepts |
|---|---|
| Convolution | filter sliding over an image; hand-made edge filters; output size $(n-k+1)^2$ |
| Vectorized layer | im2col turns convolution into one matrix product (checked against the loop); 72 conv weights vs 18,432 for an equivalent dense layer |
| Backprop | filter gradient is a sum over all positions (numerical gradient check ≈ 1e-10) |
| CNN vs dense | equal weight budget: CNN test ≈ 0.96, dense ≈ 0.97 (no CNN advantage on tiny digits) |
| Shift test | 1-pixel shift drops both to ≈ 0.42–0.43; without pooling the CNN is not more robust (honest negative result) |

## Key takeaway

Convolution reuses a few weights at every position, saving parameters and detecting local patterns anywhere. Shift invariance needs more (pooling, depth, augmentation).

## Files

- `chapter10_convolutional_neural_networks.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter10_convolutional_neural_networks.ipynb
```
