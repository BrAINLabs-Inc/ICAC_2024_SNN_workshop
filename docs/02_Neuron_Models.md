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

- **v** - membrane potential
- **u** - recovery variable
- **I** - input current
- **a, b, c, d** - parameters that shape firing behavior (regular spiking, bursting, etc.)

<img width="654" height="682" alt="image" src="https://github.com/user-attachments/assets/e99a34ff-57e5-4fbb-937d-9e979b49ef53" />


| **Baseline** | **Resting rate typically around -70 mV** | **Neuron is "at rest" but charged and ready to fire** |
|---|---|---|
| Threshold | The stimulus is strong enough to trigger the process | Voltage-gated Sodium (Na+) channels open, causing a rapid rise in voltage. |
| Overshoot | Peak of the action potential where the inside becomes positive | Cell is fully depolarized. Na+ channels closed and Potassium (K+) channels open. |
| Undershoot | Voltage drops below the baseline(Hyperpolarization) | K+ channels stay open a bit too long, making the cell extra negative and temporarily resistant to another signal. |


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

* **Integration** - incoming current $I(t)$ pushes the voltage *up*
* **Leak** - the resistance term pulls the voltage *back down* toward resting state

The time constant **$\tau = RC$** tells you *how fast* this happens. A large $\tau$ means the membrane charges and leaks slowly. A small $\tau$ means it responds quickly.

In discrete form with decay rate $\beta$:

$$
V[t+1] = \beta * V[t] + \text{input} - \text{reset}
$$

A decay rate of β = 0.95 (used in Session 3) means the membrane loses 5% of its charge per timestep.

<img width="554" height="493" alt="image" src="https://github.com/user-attachments/assets/bd87133b-77ab-4dab-a7b6-e8d465f177e9" />

## Lapicque's Equation vs Leaky Integrate-and-Fire (LIF) Model

### Overview

Lapicque's equation and the LIF model are **not the same**. The LIF model is an extension of Lapicque's original work, adding a critical leak mechanism that makes neuronal behavior more biologically realistic.

---

### 1. Origin & Core Idea

| Feature | Lapicque (1907) | LIF Model |
|---------|-----------------|-----------|
| **Proposed by** | Louis Lapicque, 1907 | Extended from Lapicque, 20th century |
| **Core concept** | Pure capacitor — charge only accumulates | Capacitor + resistor — charge leaks away |
| **Analogy** | A cup with no hole (water only fills up) | A cup with a hole (water leaks unless refilled) |

---

### 2. Shared Limitations

Both models simplify away significant neuroscience:

- No voltage-gated ion channels (Na⁺, K, Ca²⁺)
- No realistic action potential waveform
- No dendritic computation or spatial structure
- No spike-frequency adaptation (unless extensions added)
- No stochastic noise in ion channel dynamics

For more biological detail, see: **Hodgkin-Huxley (1952)**, **AdEx model**, or **conductance-based models**.

---

### 3. Applications

#### Lapicque

- Primarily a **historical and theoretical reference**
- Foundation for understanding integrate-and-fire neuron models

#### LIF Model

- **Computational neuroscience** - large-scale neural simulations
- **Neuromorphic engineering** - Intel Loihi, IBM TrueNorth chips
- **Spiking neural networks (SNNs)** - energy-efficient AI hardware
- Preferred due to simplicity + biological plausibility

---

### 4. Key Takeaway

> **LIF = Lapicque + one leak term**
>
> Adding $-\frac{(V - V_{rest})}{R_m}$ to Lapicque's equation introduces:
> - A time constant τ
> - Realistic sub-threshold decay
> - Biologically credible behavior
> - Better temporal integration properties
>
> This single addition transforms an oversimplified historical model into the most widely used neuron model in computational neuroscience.

*References: Lapicque (1907), Tuckwell (1988), Gerstner & Kistler (2002) — Spiking Neuron Models*

---

## Which Model to Use

| Model | Complexity | Biological Realism | Training Ease | Best For |
|-------|-----------|-------------------|---------------|----------|
| Izhikevich | Higher | Very high | Harder | Understanding biology |
| LIF | Lower | Good | Easier | Building trainable SNNs |

---

## What the Notebooks Cover

- Visualizing membrane potential over time
- Observing how input current amplitude affects spike rate
- Exploring excitatory vs inhibitory neuron dynamics
- Understanding threshold, reset, and refractory mechanisms

---

Previous: [Introduction](01_Introduction.md) | Next: [STDP Learning](03_STDP_Learning.md)
