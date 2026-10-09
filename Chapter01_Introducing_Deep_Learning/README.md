# Chapter 1 — Introducing Deep Learning: Why You Should Learn It

This chapter of the book is conceptual (it motivates the subject and sets the learning approach), so the notebook is a
written deep-dive plus a few small demos that I added to make the ideas concrete.

## What's covered

| Section | Concepts |
|---|---|
| What is deep learning? | many-layered neural networks whose weights are learned from data |
| AI ⊃ ML ⊃ DL | how the three terms nest (diagram) |
| Why learn it | broad usefulness, small core idea, transferable skill, better debugging |
| Why from scratch with NumPy | frameworks hide the mechanism; understanding the "engine" |
| Prerequisites | Python, basic linear algebra, derivative intuition |
| Mental model 1 | data + answers → rules (Celsius → Fahrenheit learned from examples) |
| Mental model 2 | knobs and error: learning = moving downhill on an error curve |
| Roadmap | what Chapters 1–6 will build |

## Key takeaway

Deep learning is *prediction → error → adjust weights*, repeated. The idea is small enough to build by hand, which is exactly what the following chapters do.

## Files

- `chapter01_introducing_deep_learning.ipynb` — executed notebook with saved outputs
- `outputs/` — saved charts

## Running it

```bash
pip install -r ../requirements.txt
jupyter notebook chapter01_introducing_deep_learning.ipynb
```
