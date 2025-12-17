# Javascript-FacadeMLP

This repository contains a browser-based Multi-Layer Perceptron (MLP) implementation in JavaScript, with a facaded API that enables direct inspection and manipulation of per-layer and per-neuron properties.  
The application is intended for technical investigation, learning, and demonstration of MLP behavior with no hidden internals.

---

## Table of Contents

- [About](#about)
- [Features](#features)
- [Getting Started](#getting-started)
- [Basic Example](#basic-example)
- [Facade API](#facade-api)
- [Usage Notes](#usage-notes)
- [License](#license)

---

## About

Javascript-FacadeMLP provides a fully configurable feedforward neural network in the web browser.  
You can adjust architecture, inspect or modify network parameters at runtime, and monitor training analytics.  
The facade system makes every neuron output, weight, error, gradient, and optimizer state accessible through the user interface.

---

## Features

- Network configuration:
  - Input, output, and multi-hidden-layer width/depth adjustment
  - Activation selection per layer (`sigmoid`, `tanh`, `relu`, `softmax`)
  - Output activation selection
- Training options:
  - Batch size, learning rate, optimizer type (`SGD`, `Adam`, `RMSprop`)
  - Dropout and L2 regularization (lambda)
  - Early stopping and learning rate decay controls
  - Adjustable training/validation epochs
- Data handling:
  - Upload training data from CSV or paste directly
  - Synthetic data generator for multi-class tasks
  - Train/validation split support
- Monitoring:
  - Live training loss display and progress monitoring
  - Per-class performance metrics (precision, recall, F1)
  - Save/load model weights to/from JSON files
- Facade API:
  - Inspect any layer/neuron: outputs, errors, weights, biases, pre-activation values
  - Access gradients and optimizer state (per layer or neuron)
  - Review network topology, sizes, incoming/outgoing connections
  - Dynamic modification: add/remove layers or neurons
  - Generate and view activation/gradient histograms
  - Set neuron weights, biases, L2 lambda, and per-layer learning rates during runtime
- Inference:
  - Manual test vector input and prediction

---

## Getting Started

### Requirements

- A modern web browser (Chrome, Firefox, Edge, Safari, etc.)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/matthewJamesAbbott/Javascript-FacadeMLP.git
    ```
2. Open `index.html` with your browser.

_No additional installation or server needed._

---

## Basic Example

To create a 3-class classification demo:

1. Open `index.html`
2. Set network:
    - Input Size: `10`
    - Hidden Layer Sizes: `8,8,8`
    - Output Size: `3`
    - Hidden Layer Activation: `Sigmoid`
    - Output Layer Activation: `Softmax`
    - Learning Rate: `0.1`
    - Optimizer: `SGD`
3. Generate synthetic test data by clicking **Generate Test Data** (default 2500 samples per class)
4. Under **Training Configuration**:
    - Training Epochs: `50`
    - Batch Size: `32`
5. Click **Train Network** or **Train Network With Progress**
6. Use **Facade API Explorer** to inspect neuron values, weights, gradients, topology, and more.

---

## Facade API

The façade API (available via the web UI) enables inspection and modification of:

- Neuron outputs, errors, weights, biases, and pre-activations
- Gradients for any weight or bias (by index)
- Optimizer moments (m, v) and bias moments for supported optimizers
- Layer and neuron statistics (histograms, sizes, learning rates)
- Topology (incoming/outgoing connections)
- Add/remove neurons or layers
- Set values for neuron weights, biases, L2 regularization, or per-layer learning rate at runtime

All results and status messages are shown in the output panel. Most operations can be performed without stopping or restarting training.

---

## Usage Notes

- Recommended for use with moderate-sized networks (1–4 hidden layers, up to ~128 neurons/layer) for browser speed.
- Data is only processed client-side; your CSV/text is not uploaded to any server.
- Synthetic data generation is for demo purposes only.
- Saved models are downloaded as plain JSON and can be reloaded in the interface.

---

## License

MIT License.  
You are free to use, modify, and distribute for any purpose.

---

## Vercel Link

https://javascript-facade-mlp.vercel.app/
