# Differentiable Neural Computer - Architecture

## Basic Architecture

The Differentiable Neural Computer (DNC) consists of:

1. **Controller Neural Network**: The processing unit that interacts with memory
2. **External Memory**: Matrix of size N×W where N is the number of memory locations and W is the word size
3. **Read/Write Heads**: Mechanisms for interacting with memory

## Controller

The controller can be any differentiable neural network:
- Feedforward neural network
- LSTM
- Other RNN variants

It takes as input:
- External inputs
- Previous read vectors from memory
- Previous state (if using a recurrent controller)

## Memory

The memory is an N×W matrix where:
- N = number of memory locations
- W = word size (dimension of each vector stored in memory)

Unlike conventional computer memory, addressing is "fuzzy" - multiple locations can be accessed simultaneously to varying degrees.

## Memory Addressing Mechanisms

### 1. Content-based Addressing

Similar to attention mechanisms, this computes similarity between a lookup key and all memory locations.

### 2. Memory Allocation

Uses a "usage" vector to track which memory locations are free or used:
- Usage increases when locations are written to
- Locations can be freed using the free gate

### 3. Temporal Linkage

Tracks the order in which locations are written:
- Forward and backward links establish sequential relationships
- Enables sequential retrieval even after jumps in address space

## Operations

### 1. Read

- Combines content-based addressing with temporal linking
- Multiple read heads are possible
- Read vectors are fed back to the controller and contributed to output

### 2. Write

- Combines content-based addressing with allocation
- Uses "erase" and "write" vectors to modify content
- Uses write gate to determine write strength

## Key Differences from Neural Turing Machines (NTMs)

1. **Dynamic Memory Allocation**: DNCs can allocate new locations and free old ones
2. **Temporal Linkage**: DNCs track the order of writes, allowing sequential reads after jumps
3. **Content-Based Addressing**: Improved implementation compared to NTMs
