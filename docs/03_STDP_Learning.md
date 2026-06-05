# Spike-Timing Dependent Plasticity (STDP)

## Overview

STDP is an unsupervised learning rule where synaptic connections strengthen or weaken based on the **relative timing** of pre- and post-synaptic spikes.

## The Core Principle

**"Neurons that fire together wire together"** — but with timing sensitivity.

```
If presynaptic neuron fires BEFORE postsynaptic neuron:
  → Connection STRENGTHENS (potentiation)

If presynaptic neuron fires AFTER postsynaptic neuron:
  → Connection WEAKENS (depression)

If firing is simultaneous or far apart:
  → Minimal change
```

## Mathematical Form

```
ΔW ∝ exp(-|Δt| / τ_stdp)

Where:
  Δt = time difference between spikes
  τ_stdp = learning window (typically 10-100ms)
```

## Why This Matters

✓ **Biological**: Mirrors how real brains learn
✓ **Causal**: Only strengthens when pre-activity predicts post-activity
✓ **Local**: Depends only on local spike information (no global loss)
✓ **Unsupervised**: Requires no labels or target signals

## What Happens in the Notebook

The STDP notebook demonstrates:

1. **Network Setup**: 10 neurons, 3 layers
2. **Spike Generation**: Random input patterns
3. **Weight Adaptation**: STDP modifies connection strengths
4. **Visualization**: Watch weights change as spikes occur
5. **Patterns Emerge**: Network self-organizes from random initial state

## Connection to Supervised Learning

While STDP is unsupervised, it's foundational for understanding how SNNs learn:
- Session 3 builds on these principles using supervised backpropagation
- Both involve temporal dynamics and spike-timing relationships
- STDP shows learning is possible without explicit loss functions

## Key Insights

✓ Learning rules can be local and spike-based
✓ Temporal causality is important
✓ Networks self-organize through interaction
✓ Biological realism doesn't require labels

## Next Steps

→ See [SNN Training](04_SNN_Training.md) to learn supervised learning with SNNs
