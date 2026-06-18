# Neuron Models

[Back to README](../README.md)

## Overview

Session 1 covers two neuron models that form the foundation of this workshop: the Izhikevich model and the Leaky Integrate-and-Fire (LIF) model.

## Izhikevich Neuron Model

The Izhikevich model captures diverse spiking behaviors using two coupled differential equations:

```
dv/dt = 0.04*v² + 5*v + 140 - u + I
du/dt = a*(b*v - u)
if v >= 30mV: v = c, u = u + d
```

- **v** — membrane potential
- **u** — recovery variable
- **I** — input current
- **a, b, c, d** — parameters that shape firing behavior (regular spiking, bursting, etc.)

<img width="654" height="682" alt="image" src="https://github.com/user-attachments/assets/e99a34ff-57e5-4fbb-937d-9e979b49ef53" />


The notebook demonstrates how changing these parameters produces different neuron types, with real-time visualizations of spike rasters and membrane dynamics.

## Leaky Integrate-and-Fire (LIF) Model

The LIF simplifies neuron dynamics while retaining the essential spiking behavior used in most modern SNNs:

$$
\tau \frac{dV}{dt} = -(V(t) - V_{rest}) + R I(t)
$$

$$
V(t) = V_{rest}, \text{ if } V(t) = V_{thresh}
$$

---

The voltage $V(t)$ across the membrane changes over time according to two competing forces:

* **Integration** — incoming current $I(t)$ pushes the voltage *up*
* **Leak** — the resistance term pulls the voltage *back down* toward resting state

The time constant **$\tau = RC$** tells you *how fast* this happens. A large $\tau$ means the membrane charges and leaks slowly. A small $\tau$ means it responds quickly.

In discrete form with decay rate $\beta$:

$$
V[t+1] = \beta * V[t] + \text{input} - \text{reset}
$$

A decay rate of β = 0.95 (used in Session 3) means the membrane loses 5% of its charge per timestep.

<img width="554" height="493" alt="image" src="https://github.com/user-attachments/assets/bd87133b-77ab-4dab-a7b6-e8d465f177e9" />


## Which Model to Use

| Model | Complexity | Biological Realism | Training Ease | Best For |
|-------|-----------|-------------------|---------------|----------|
| Izhikevich | Higher | Very high | Harder | Understanding biology |
| LIF | Lower | Good | Easier | Building trainable SNNs |

## What the Notebooks Cover

- Visualizing membrane potential over time
- Observing how input current amplitude affects spike rate
- Exploring excitatory vs inhibitory neuron dynamics
- Understanding threshold, reset, and refractory mechanisms

---

Previous: [Introduction](01_Introduction.md) | Next: [STDP Learning](03_STDP_Learning.md)
