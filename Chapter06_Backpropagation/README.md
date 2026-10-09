# Chapter 6 — Building Your First Deep Neural Network: Introduction to Backpropagation

A network with a hidden layer, and how its weights learn from error signals sent backwards.

## What's covered

| Section | Concepts |
|---|---|
| A pattern with no correlation | XOR-style lamp problem: each switch alone has correlation 0 with the target |
| One layer fails | single layer (and two stacked linear layers) stall at predicting 0.5; least-squares confirms it is the best linear fit |
| ReLU | non-linearity $\max(0,z)$ and its slope; a hand-built network proves the problem is solvable |
| Forward pass | $\mathbf l_1=\operatorname{relu}(\mathbf l_0W_{01}),\ \hat{\mathbf y}=\mathbf l_1W_{12}$ |
| Backpropagation | $\boldsymbol\delta_2=\hat y-y$; $\boldsymbol\delta_1=(\boldsymbol\delta_2W_{12}^\top)\odot\operatorname{relu}'(z_1)$; $\nabla W=\mathbf l^\top\boldsymbol\delta$ |
| Gradient check | analytic vs numerical gradients agree (max difference ~1e-10) |
| Training | error → ~0; learned decision surface and hidden-unit activations |
| Width and dead units | success rate by hidden size over 30 seeds; failed runs contain dead ReLU units |
| Any depth | general backward recursion; a two-hidden-layer network also learns the pattern |

## Key takeaway

The hidden layer has no known target, so its blame is computed from the output error by the chain rule and passed **backwards**
through the weights. The same recursion trains networks of any depth.

## Files

- `chapter06_backpropagation.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter06_backpropagation.ipynb
```
