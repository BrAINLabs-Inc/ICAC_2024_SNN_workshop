# Spike-Timing Dependent Plasticity (STDP)

[Back to README](../README.md)

## Overview

Session 2 introduces STDP — an unsupervised learning rule where synaptic connections change based on the relative timing of pre- and post-synaptic spikes.

## The Core Principle

If a presynaptic neuron fires just before a postsynaptic neuron, the connection strengthens (potentiation). If the order is reversed, the connection weakens (depression). This captures a simple causal rule: activity that predicts a downstream spike gets reinforced.

```
Δt = t_post - t_pre

Δt > 0 (pre before post) → weight increases
Δt < 0 (post before pre) → weight decreases
```

The magnitude of change decays exponentially with the time difference:

```
ΔW ∝ exp(-|Δt| / τ_stdp)
```
<img width="730" height="486" alt="image" src="https://github.com/user-attachments/assets/3657baae-35d4-484f-964e-a37046c80f3a" />


## What the Notebook Demonstrates

- A small network of neurons receiving random input patterns
- STDP modifying connection weights based on spike timing
- Weights self-organizing without any labels or loss function
- Visualization of weight changes as learning progresses

## Key Properties

- **Unsupervised**: No labels or target outputs required
- **Local**: Each synapse updates based only on the two neurons it connects
- **Causal**: Strengthens connections where pre-activity predicts post-activity
- **Biologically grounded**: Observed in real cortical neurons

## Connection to Session 3

STDP provides intuition for how timing matters in SNN learning. Session 3 moves to supervised training with backpropagation, but the same temporal dynamics underlie both approaches.

---

Previous: [Neuron Models](02_Neuron_Models.md) | Next: [Training SNNs](04_SNN_Training.md)
