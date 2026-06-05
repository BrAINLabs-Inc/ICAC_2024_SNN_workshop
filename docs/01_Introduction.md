# What are Spiking Neural Networks?

## Overview

Spiking Neural Networks (SNNs) are neural networks that communicate through discrete spike events, mimicking how biological brains work. Instead of continuous activation values, neurons fire binary spikes at specific moments in time.

## Traditional ANNs vs SNNs

| Aspect | ANN | SNN |
|--------|-----|-----|
| **Signal Type** | Continuous activations | Discrete spikes (binary events) |
| **Processing** | Single feedforward pass | Temporal dynamics over timesteps |
| **Computation** | All neurons fire every step | Only threshold-crossing neurons fire |
| **Energy** | High power consumption | Low power (sparse events) |
| **Hardware** | GPUs, CPUs | Neuromorphic accelerators |

## Why SNNs Matter

1. **Energy Efficiency**: Only fire when needed → massive power savings on neuromorphic hardware
2. **Neuromorphic Compatibility**: Native support on Intel Loihi, IBM TrueNorth processors
3. **Temporal Processing**: Naturally handle time-series and event-based data
4. **Brain-Inspired**: Closer match to biological neural computation

## Real-World Applications

- Event-based camera processing (DVS sensors)
- Real-time neuromorphic chips for robotics
- Low-power edge AI devices
- Temporal pattern recognition

## This Workshop Covers

✓ How spiking neurons work mathematically
✓ Building SNN models in PyTorch
✓ Training with surrogate gradients
✓ Classification tasks (MNIST)
✓ Comparing SNNs vs traditional ANNs

## Next Steps

→ Start with [Neuron Models](02_Neuron_Models.md) to understand the mathematics
