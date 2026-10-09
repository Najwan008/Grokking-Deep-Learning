# Chapter 4 — Introduction to Neural Learning: Gradient Descent

The **Compare** and **Learn** steps for the simplest case: one input, one weight.

## What's covered

| Section | Concepts |
|---|---|
| Measuring error | squared error and why it is used (non-negative, punishes big misses, smooth) |
| Hot and cold learning | try ±step, keep the better one — works but wasteful and jitters around the optimum |
| The gradient | derivative $dE/dw = 2x(xw-y)$ derived with the chain rule and **verified numerically** |
| Gradient descent | $w \leftarrow w - \alpha\,dE/dw$: direction from the sign, step size from the magnitude |
| Learning rate $\alpha$ | exact analysis: error distance shrinks by $c = 1-2\alpha x^2$; converges iff $0<\alpha<1/x^2$; experiments confirm |
| Many examples | average gradient; result matches the closed-form optimum |

## Key takeaway

Gradient descent reads both the direction and the amount of the correction from the slope of the error. The learning rate must
be tuned: too small is slow, too large diverges.

## Files

- `chapter04_gradient_descent.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter04_gradient_descent.ipynb
```
