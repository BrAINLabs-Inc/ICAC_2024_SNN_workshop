# Exploring Spiking Neural Networks

Welcome to the ICAC 2024 SNN Workshop repository! This is a hands-on introduction to **Spiking Neural Networks (SNNs)** — neural networks that mimic biological brains through discrete spike events.

## 🚀 Quick Start

All notebooks run in **Google Colab** with zero setup. Just click and start:

1. [Izhikevich Neuron](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/Izhikevich_Neuron.ipynb) - Learn neuron dynamics
2. [LIF Neuron Model](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/LIF_Neuron_Model.ipynb) - Simplified spiking neurons
3. [STDP Learning](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/STDP_unsupervised.ipynb) - Unsupervised learning rules
4. [SNN MNIST](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/SNN_implementation_of_MNIST_dataset.ipynb) - Train SNNs on digit recognition
5. [ANN MNIST](https://colab.research.google.com/github/BrAINLabs-Inc/ICAC_2024_SNN_workshop/blob/main/Notebooks/ANN_implementation_of_MNIST_dataset.ipynb) - Traditional neural network baseline

## 📚 Tutorials & Documentation

Learn more about each topic:

- **[What are SNNs?](docs/01_Introduction.md)** - Overview and why SNNs matter
- **[Neuron Models](docs/02_Neuron_Models.md)** - Izhikevich and LIF explained
- **[Learning Rules](docs/03_STDP_Learning.md)** - Spike-timing dependent plasticity
- **[Training SNNs](docs/04_SNN_Training.md)** - Backprop through time & surrogate gradients
- **[Performance Comparison](docs/05_Results.md)** - SNN vs ANN on MNIST

## 📊 What You'll Learn

- How biological neurons inspire artificial neural networks
- Mathematical models of spiking neurons
- Unsupervised learning with STDP
- Training spiking networks with backpropagation
- Real-world applications on MNIST dataset

## 🛠 Technologies Used

- **PyTorch** - Deep learning framework
- **snnTorch** - SNN library
- **Matplotlib** - Visualization
- **NumPy** - Numerical computing

## 📖 Session Structure

**Session 1: Foundations**
- Izhikevich neuron model
- Leaky Integrate-and-Fire (LIF) neurons
- Spike dynamics visualization

**Session 2: Learning**
- Spike-Timing Dependent Plasticity (STDP)
- Unsupervised weight adaptation
- Temporal causality in learning

**Session 3: Applications**
- End-to-end SNN training
- Classification on MNIST
- Performance vs traditional ANNs

## 📝 Resources

- [snnTorch Documentation](https://snntorch.readthedocs.io/)
- [BRIAN2 Simulator](https://briansimulator.org/)
- [Izhikevich Model Details](https://www.izhikevich.org/publications/whichmod.htm)

## 🎯 Key Results

- **ANN Baseline**: 75.93% test accuracy on MNIST (1 epoch)
- **SNN Training**: Successfully demonstrates surrogate gradients & BPTT
- **Training Time**: ~15-30 min per notebook on Colab GPU

## 📖 Citation

```bibtex
@workshop{BrAINLabs2024SNN,
  title={Exploring Spiking Neural Networks},
  author={BrAINLabs-Inc},
  booktitle={ICAC 2024},
  year={2024},
  url={https://github.com/BrAINLabs-Inc/ICAC_2024_SNN_workshop}
}
```

## 📄 License

MIT License - see LICENSE file for details.

---

**Workshop Date**: ICAC 2024 | **Organization**: [BrAINLabs-Inc](https://github.com/BrAINLabs-Inc)
