# Javascript-FacadeMLP

Welcome to the **Javascript-FacadeMLP** repository! This project is a Multi-Layer Perceptron (MLP) implementation in JavaScript, featuring a Layer Facade design for enhanced control and modularity. The interactive web demo lets users easily experiment with neural network configuration, training, and evaluation — all in your browser.

## Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Getting Started](#getting-started)

## About the Project

This project demonstrates a Multi-Layer Perceptron neural network using a "Layer Facade" pattern, allowing for clean access to layer and neuron internals without sacrificing encapsulation. The included HTML interface gives you control over hidden/output layer activations, batch size, dataset loading/generation, metrics, and more.

### Built With
- **HTML**: Interactive web interface
- **JavaScript**: MLP implementation and Layer Facade logic

## Features

- Layer Facade pattern for easy layer and neuron property access
- Custom configuration for:
  - Number and size of input/hidden/output layers
  - Activation functions per layer (`sigmoid`, `tanh`, `relu`, `softmax`)
  - Learning rate, training epochs, batch size, folds for cross-validation
- Train with user data via CSV file upload or text paste
- Synthetic data generator for rapid MLP testing
- Save/load model to/from JSON files
- Evaluation metrics:
  - K-Fold Cross Validation accuracy
  - Per-class Precision, Recall, and F1 Score table
- Progress tracker for real-time epoch updates
- Single input prediction for manual testing

## Getting Started

To quickly try out the MLP Facade demo, simply:

### Prerequisites
You'll need a modern web browser.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/matthewJamesAbbott/Javascript-FacadeMLP.git
   ```
2. Open `index.html` in your web browser.

## Vercel Link
*Coming soon!* (Deploy your fork on [Vercel](https://vercel.com/) or use locally.)
