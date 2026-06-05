# Exploring Spiking Neural Networks

Workshop materials for the [ICAC 2024](https://icac.lk/) (6th International Conference on Advancements in Computing) pre-conference workshop on [Exploring Spiking Neural Networks](https://icac.lk/preconference-workshops/).

Workshop recording: [Google Drive](https://drive.google.com/file/d/16I4Rfyuw2CHjNAfu2K_6PrMMZbYlhmYC/view?usp=drive_link) | Slides: [PDF](https://github.com/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Slides/Exploring_Spiking_Neural_Networks.pdf)

---

## About This Workshop

Spiking Neural Networks (SNNs) are neural networks that communicate through discrete spike events, closely mimicking how biological brains work. Unlike traditional ANNs that use continuous activations, SNNs fire binary spikes at specific moments in time - enabling energy-efficient computation on neuromorphic hardware.

This workshop is divided into 3 progressive sessions, from neuron fundamentals through to real-world classification tasks.

<img width="1505" height="851" alt="image" src="https://github.com/user-attachments/assets/f4538d3a-cbb2-4be9-afbe-143f81fc78e2" />


---

## Hands-On Sessions

| Session | Description | Notebook |
| --- | --- | --- |
| Session 1 | Part 1: Izhikevich Neuron Model | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/Izhikevich_Neuron.ipynb) |
| | Part 2: LIF Neuron Model | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/Leaky_Integrate_and_Fire_(LIF)_neuron_model.ipynb) |
| Session 2 | STDP Learning Algorithm | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/STDP_unsupervised.ipynb) |
| Session 3 | Part 1: SNN Implementation with MNIST Dataset | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/SNN_implementation_of_MNIST_dataset.ipynb) |
| | Part 2: ANN Implementation with MNIST Dataset | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/ANN_implementation_of_MNIST_dataset.ipynb) |

Notebooks are designed to run standalone and include all necessary setup. Recommended to run in Google Colab.

<img width="1365" height="774" alt="image" src="https://github.com/user-attachments/assets/90a5652f-5823-469f-a784-22f7e1e07c7e" />


---

## Documentation

Summaries of what each session covers:

- [Introduction to SNNs](docs/01_Introduction.md) - What SNNs are and why they matter
- [Neuron Models](docs/02_Neuron_Models.md) - Izhikevich and LIF models explained
- [STDP Learning](docs/03_STDP_Learning.md) - Spike-timing dependent plasticity
- [Training SNNs](docs/04_SNN_Training.md) - Surrogate gradients and backpropagation through time
- [Results and Comparison](docs/05_Results.md) - SNN vs ANN performance on MNIST

---

## References

**Research Papers**
- [Training Spiking Neural Networks Using Lessons From Deep Learning](https://ieeexplore.ieee.org/abstract/document/10242251)

**Textbooks**
- [Dynamical Systems in Neuroscience: The Geometry of Excitability and Bursting](https://drive.google.com/file/d/1qRoJr6TRUYNFI74v8GdpAalsCrZkh2UR/view?usp=sharing)
- [Theoretical Neuroscience](https://drive.google.com/file/d/1DEpJKvVgZoTcjk9pDy-FNBK7AZm7ryph/view?usp=sharing)

---

## Resources

- [BRIAN2: Python based Spiking Neural Networks Library](https://briansimulator.org/)
- [snnTorch: Gradient based Spiking Neural Networks Training Library](https://snntorch.readthedocs.io/)
- [NeuCube-Py](https://github.com/KEDRI-AUT/NeuCube-Py)
- [Izhikevich Model Details](https://www.izhikevich.org/publications/whichmod.htm#izhikevich)
- [Neural Data Science - University of Tübingen](https://www.youtube.com/playlist?list=PL05umP7R6ij3SxudmSWFL_zGh0BMrRdrx)
- [Computational Neuroscience PhD Student YouTube](https://www.youtube.com/@CharlotteFraza/videos)
