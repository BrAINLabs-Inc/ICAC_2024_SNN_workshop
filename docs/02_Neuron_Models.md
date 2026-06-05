# Neuron Models

## Overview

This tutorial summarizes the neuron models implemented in the workshop notebooks.

## Izhikevich Neuron Model

The Izhikevich model captures diverse spiking behaviors with just two differential equations:

```
dv/dt = 0.04*v² + 5*v + 140 - u + I
du/dt = a*(b*v - u)

if v ≥ 30mV: v = c, u = u + d
```

### What It Does

- **v**: Membrane potential (voltage)
- **u**: Recovery variable (adaptation)
- **I**: Input current
- **a, b, c, d**: Parameters that change neuron behavior

### Key Features

✓ Captures regular spiking, bursting, chattering patterns
✓ Biologically realistic dynamics
✓ Can model excitatory and inhibitory neurons
✓ Relatively simple mathematics

### Parameters

- **Excitatory neurons**: Larger c and d values (stronger hyperpolarization after spike)
- **Inhibitory neurons**: Different recovery dynamics (faster response)

## Leaky Integrate-and-Fire (LIF) Model

Simpler than Izhikevich, the LIF is the workhorse of modern SNNs:

```
τ_m * dV/dt = -(V - V_L) + I/g_L

if V ≥ V_threshold: V = V_reset + refractory period
```

### What It Does

- **V**: Membrane potential
- **V_L**: Resting potential
- **g_L**: Leak conductance (how fast voltage decays)
- **τ_m**: Time constant for integration

### Key Features

✓ Linear subthreshold dynamics (easier to train)
✓ Standard model in neuromorphic computing
✓ Works well with backpropagation
✓ Interpretable parameters

### Decay Rate (β)

In discrete form, we use:
```
V[t+1] = β * V[t] + input - reset
```

Where **β = 0.95** means 5% decay per timestep.

## Comparison

| Model | Complexity | Biological Realism | Training Ease | Use Case |
|-------|-----------|-------------------|---------------|----------|
| Izhikevich | High | Very high | Harder | Understanding biology |
| LIF | Low | Good | Easier | Building practical SNNs |

## What We Learn

✓ How neurons integrate input over time
✓ When and why neurons spike
✓ How parameters affect firing patterns
✓ Visualization of membrane dynamics

## Next Steps

→ See [STDP Learning](03_STDP_Learning.md) to learn how neurons adapt their connections
