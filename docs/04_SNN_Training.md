# Training Spiking Neural Networks

## Overview

This tutorial summarizes how we train SNNs on real classification tasks using modern deep learning techniques.

## The Challenge: Non-Differentiable Spikes

The spike function is a Heaviside step function:

```
S = 1 if V > threshold
S = 0 otherwise

Problem: dS/dV = 0 everywhere (gradient is zero!)
         No gradient flow for backpropagation
```

## The Solution: Surrogate Gradients

We use a clever trick:

```
Forward Pass: Use true spike function (binary output)
Backward Pass: Replace derivative with smooth approximation

Surrogate derivative: dS/dU ≈ 1 / (π(1 + (πU)²))
```

This is called the **arctan surrogate gradient** — it lets gradients flow while keeping spike generation binary.

## Architecture Overview

```
Static Image (28×28)
    ↓
[Input Layer: 784 neurons]
    ↓
[Hidden: 1000 LIF neurons]
    ↓
[Output: 10 LIF neurons]
    ↓
Predict digit class
```

## Temporal Processing

Instead of one feedforward pass, SNNs simulate **25 timesteps**:

1. Input stays constant across timesteps
2. Neurons accumulate and integrate
3. Spikes occur as membrane potential crosses threshold
4. Loss computed at each timestep
5. Total loss = sum of all timestep losses

## Key Training Techniques

| Technique | Why It Matters |
|-----------|----------------|
| **BPTT** | Backpropagation Through Time — tracks gradients across timesteps |
| **Surrogate Gradients** | Overcomes spike discontinuity |
| **Rate Coding** | Decode output as spike count (most spikes = predicted class) |
| **Adam Optimizer** | Learning rate 5e-4, momentum-based updates |

## What Happens During Training

1. **Initialization**: Random spike patterns, random weights
2. **Iteration 50**: Network starts organizing (70%+ accuracy!)
3. **Iteration 100+**: Convergence continues, loss stabilizes
4. **Final**: 75.93% test accuracy after 1 epoch

## Important Insights

✓ **Surrogate gradients actually work** — SNNs are trainable
✓ **25 timesteps is enough** for MNIST complexity
✓ **Rapid learning** — accuracy improves quickly
✓ **Standard tools apply** — PyTorch, Adam optimizer work fine

## Comparing to ANNs

```
ANN:  Single pass → Output logits → Cross-entropy loss
SNN:  25 passes → Spike trains → Rate decode → Sum loss across time
```

Both work! SNNs add temporal dimension and energy efficiency.

## Next Steps

→ See [Results & Performance](05_Results.md) to compare SNN vs ANN performance
