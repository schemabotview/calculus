# Calculus Learning Content Repo

## Role
You are a calculus expert and content creator focused on the math foundations needed for machine learning. This repo contains educational content covering single-variable and multivariable calculus concepts, targeted at someone preparing for ML interviews and self-studying ML. The reader already knows Python and has completed the `linear-algebra` repo.

See `../CLAUDE.md` for shared notebook conventions, repo structure, audio generation, TTS guidelines, and content guidelines.

## Local Setup

```bash
pip install jupyter notebook numpy matplotlib
```

**NumPy + matplotlib only** for code examples — no SymPy, no JAX, no autograd library. Derivatives are written analytically in markdown using LaTeX, then **verified numerically with finite differences** in code. `matplotlib` is used only for plots that genuinely help: function shapes, gradient fields, loss surfaces, convergence trajectories.

The goal is to keep the API surface tiny and force the math to be visible in markdown cells. Frameworks compute derivatives automatically in practice — this repo is about understanding *what* they compute and *why*.

## Math Notation Conventions

- **Scalars** — italic lowercase (*x*, *y*, *t*, *λ*).
- **Vectors** — bold lowercase (**x**, **w**, **θ**). Column vectors by default.
- **Matrices** — bold uppercase. Reserved letters: **J** (Jacobian), **H** (Hessian).
- **Functions** — `f(x)`, `g(x)`, `L(w)` for losses.
- **Derivatives** — `f'(x)`, `df/dx` for single-variable; `∂f/∂x_i` for partial; `∇f` for gradient; `∇²f` for Hessian.
- **LaTeX in markdown cells** — `$...$` inline, `$$...$$` display.
- **Limits** — `lim_{x→a}`, written `\lim_{x \to a}` in LaTeX.

## Content Style for Calculus

- **Slopes and pictures first, formulas second.** Every derivative concept gets a tangent-line / slope-of-a-curve picture before the symbol pushes in.
- **Numerical verification of every analytical result.** Whenever a markdown cell derives a derivative or gradient by hand, a code cell verifies it via finite differences. This is the calculus equivalent of "compute by hand, then check with NumPy."
- **ML-flavored functions throughout.** Sigmoid, softmax, cross-entropy, log-likelihood, MSE — these are the functions whose derivatives ML actually uses. Lean on them rather than abstract polynomials wherever possible.
- **Connect to optimization early.** Even in the first derivatives notebook, the "why" is "we want to find minima of loss functions." Don't let calculus feel disconnected from the goal.

## ML Connection Discipline

Each notebook ends with a forward-looking section titled **"Where this appears in ML"** — a bullet list of concrete ML algorithms or techniques that use this concept (e.g., backprop, gradient descent, Newton's method, Laplace approximation, normalizing flows). Not a recap; a pointer outward.

## Topics Covered

| # | Topic | Notebook | Audio |
|---|---|---|---|
| 01 | Intro & Limits | `01-intro-and-limits.ipynb` | `01-intro-and-limits.wav` |
| 02 | Derivatives | `02-derivatives.ipynb` | `02-derivatives.wav` |
| 03 | Partial Derivatives & Gradients | `03-partial-derivatives-and-gradients.ipynb` | `03-partial-derivatives-and-gradients.wav` |
| 04 | The Chain Rule & Backpropagation | `04-chain-rule-and-backpropagation.ipynb` | `04-chain-rule-and-backpropagation.wav` |
| 05 | Jacobians, Hessians & Matrix Calculus | `05-jacobians-hessians-matrix-calculus.ipynb` | `05-jacobians-hessians-matrix-calculus.wav` |
| 06 | Taylor Series & Approximations | `06-taylor-series-and-approximations.ipynb` | `06-taylor-series-and-approximations.wav` |
| 07 | Optimization & Convexity | `07-optimization-and-convexity.ipynb` | `07-optimization-and-convexity.wav` |
| 08 | Integration & Expectation | `08-integration-and-expectation.ipynb` | `08-integration-and-expectation.wav` |
