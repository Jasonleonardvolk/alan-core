# Differentiable Neural Computer (DNC) Implementations

## Official Implementation

### DeepMind's TensorFlow Implementation
- **Repository**: [google-deepmind/dnc](https://github.com/google-deepmind/dnc)
- **Framework**: TensorFlow, Sonnet
- **Description**: Official implementation by DeepMind, includes the copy task example
- **Features**:
  - Core DNC architecture
  - Access module with memory reading/writing
  - Temporal linkage tracking
  - Memory freeness tracking
  - Example training script for copy task

## PyTorch Implementations

### ixaxaar/pytorch-dnc
- **Repository**: [ixaxaar/pytorch-dnc](https://github.com/ixaxaar/pytorch-dnc)
- **Framework**: PyTorch
- **Description**: Implementation of DNC, Sparse Access Memory, and Sparse DNC
- **Features**:
  - Multiple memory types (DNC, SAM, SDNC)
  - FAISS integration for GPU acceleration
  - Copy task example
  - Support for different RNN controllers

### jingweiz/pytorch-dnc
- **Repository**: [jingweiz/pytorch-dnc](https://github.com/jingweiz/pytorch-dnc)
- **Framework**: PyTorch, Visdom
- **Description**: Implementation of both Neural Turing Machine and DNC with visualization
- **Features**:
  - Combined NTM and DNC codebase
  - Visualization with Visdom
  - Clear class hierarchy

### ypxie/pytorch-NeuCom
- **Repository**: [ypxie/pytorch-NeuCom](https://github.com/ypxie/pytorch-NeuCom)
- **Framework**: PyTorch
- **Description**: Pytorch implementation of DeepMind's DNC paper

### zeligism/dnc-torch
- **Repository**: [zeligism/dnc-torch](https://github.com/zeligism/dnc-torch)
- **Framework**: PyTorch
- **Description**: PyTorch implementation of the DNC
- **Features**:
  - Alternative loss calculation approach
  - Copy task implementation

### deepcpatel/differentiable_neural_computer
- **Repository**: [deepcpatel/differentiable_neural_computer](https://github.com/deepcpatel/differentiable_neural_computer)
- **Framework**: PyTorch
- **Description**: DNC implementation with bAbI QA and Copy tasks
- **Features**:
  - Support for both CPU and GPU
  - bAbI Question Answering task
  - Pattern Copy task

### AndreaCossu/DNC-pytorch
- **Repository**: [AndreaCossu/DNC-pytorch](https://github.com/AndreaCossu/DNC-pytorch)
- **Framework**: PyTorch (v0.4.1)
- **Description**: DNC implementation with different controller options
- **Features**:
  - Different controller implementations
  - Copy task

### lnpalmer/DNC
- **Repository**: [lnpalmer/DNC](https://github.com/lnpalmer/DNC)
- **Framework**: PyTorch
- **Description**: Minimal implementation of DNC in PyTorch

## TensorFlow Implementations

### Mostafa-Samir/DNC-tensorflow
- **Repository**: [Mostafa-Samir/DNC-tensorflow](https://github.com/Mostafa-Samir/DNC-tensorflow)
- **Framework**: TensorFlow
- **Description**: TensorFlow implementation focusing on key characteristics
- **Features**:
  - Copy task demonstration
  - bAbI 20QA task
  - Detailed documentation and guides

### bgavran/DNC
- **Repository**: [bgavran/DNC](https://github.com/bgavran/DNC)
- **Framework**: TensorFlow 1.2.rc0, Python 3.6
- **Description**: Implementation with visualization and multiple tasks
- **Features**:
  - Copy task, repeat copy task, bAbI QA task
  - Automatic Tensorboard visualization
  - Modular design with different controllers
  - Memory usage visualization

### psavine42/fun-with-dnc
- **Repository**: [psavine42/fun-with-dnc](https://github.com/psavine42/fun-with-dnc)
- **Framework**: PyTorch
- **Description**: Implementation with focus on planning tasks
- **Features**:
  - Air Cargo Problem implementation
  - Training schedule implementation as in original paper

## Related DNC Variants and Extensions

### LSaldyt/DNC-1
- **Repository**: [LSaldyt/DNC-1](https://github.com/LSaldyt/DNC-1)
- **Description**: Fork of bgavran/DNC with possible modifications

## Implementation Notes

When implementing or using a DNC, consider the following aspects:

1. **Controller Type**: Most implementations allow flexibility in choosing the controller (LSTM, feedforward, etc.)

2. **Memory Size**: The memory size can affect performance but models should generalize across different memory sizes

3. **Training Tasks**: Common tasks include:
   - Copy task: Testing basic memory operations
   - Repeat copy: Testing recall and repetition
   - bAbI QA: Testing reasoning capabilities

4. **Computational Efficiency**: DNCs are significantly more computationally expensive than standard RNNs or LSTMs

5. **Implementation Challenges**:
   - Getting memory addressing mechanisms right
   - Handling dynamic memory allocation
   - Implementing temporal linkage properly
   - Ensuring differentiability throughout
