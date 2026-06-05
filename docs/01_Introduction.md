# Introduction to Spiking Neural Networks

[Back to README](../README.md)

## What Are SNNs?

Spiking Neural Networks (SNNs) are neural networks that communicate through discrete spike events, mimicking how biological brains work. Instead of continuous activation values, neurons fire binary spikes at specific moments in time.

## Traditional ANNs vs SNNs

| Aspect | ANN | SNN |
|--------|-----|-----|
| Signal Type | Continuous activations | Discrete spikes (binary events) |
| Processing | Single feedforward pass | Temporal dynamics over timesteps |
| Computation | All neurons fire every step | Only threshold-crossing neurons fire |
| Hardware | GPUs, CPUs | Neuromorphic accelerators |

## Why SNNs Matter

- **Energy Efficiency**: Sparse event-driven computation reduces power consumption on neuromorphic processors
- **Neuromorphic Hardware**: Native support on Intel Loihi and IBM TrueNorth processors
- **Temporal Processing**: Naturally handle time-series and event-based data
- **Biological Plausibility**: Closer match to actual neural mechanisms

## Real-World Applications

- Event-based camera processing (DVS sensors)
- Low-power edge AI devices
- Temporal pattern recognition
- Neuromorphic robotics

## Workshop Roadmap

- Session 1: Understand how spiking neurons work mathematically
- Session 2: Learn how connections adapt through spike timing (STDP)
- Session 3: Train SNNs on real data and compare against ANNs

---

Next: [Neuron Models](02_Neuron_Models.md)
