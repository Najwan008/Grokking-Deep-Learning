# Chapter 3 — Introduction to Neural Prediction: Forward Propagation

The **Predict** step of Predict → Compare → Learn, implemented with plain NumPy. Weights are hand-picked here; learning starts in Chapter 4.

## What's covered

| Section | Concepts |
|---|---|
| One input, one weight | $\hat y = xw$; the weight as a knob / slope |
| Several inputs → one output | weighted sum = dot product, per-input contributions, sensitivity |
| One input → several outputs | independent single-weight neurons |
| Several inputs → several outputs | weight matrix $W$ (outputs × inputs), `W @ x` |
| Batches | predicting many examples with one matrix product |
| Stacked networks | hidden layers, and why purely linear stacking collapses to one layer ($W_2W_1$) |
| NumPy refresher | element-wise ops, broadcasting, dot, shape rules |

## Key takeaway

Forward propagation is repeated weighted sums. One neuron is a dot product, a layer is a matrix–vector product, a batch is a
matrix–matrix product. Stacking *linear* layers gains nothing — a non-linearity is needed (Chapter 6).

## Files

- `chapter03_forward_propagation.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter03_forward_propagation.ipynb
```
