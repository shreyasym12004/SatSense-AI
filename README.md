AI-Driven Satellite Signal Detection & Mitigation

📡 Overview
This project provides an automated system for identifying and cleaning interference in satellite communications. It uses a 1D-Convolutional Neural Network (1D-CNN) to classify raw IQ signals into four distinct states: Clean BPSK, Clean QPSK, High Noise, and Jamming.
When jamming is detected, the system automatically triggers a digital Notch Filter to remove the interference and restore the link quality, as measured by the Bit Error Rate (BER).
________________________________________
✨ Features
•	Direct IQ Processing: Uses raw In-phase and Quadrature data—no conversion to images required.
•	Real-Time Classification: Highly efficient 1D-CNN architecture suitable for low-latency satellite hardware.
•	Smart Mitigation: Autonomous activation of an IIR Notch Filter during interference events.
•	Performance Analytics: Built-in confusion matrix and BER calculation tools.
________________________________________
🛠️ Technologies Used
•	Python 3.10+
•	TensorFlow / Keras: Deep learning model construction and training.
•	SciPy: Signal processing and IIR filter implementation.
•	NumPy: High-performance numerical operations.
•	Matplotlib / Seaborn: Data visualization and performance heatmaps.
________________________________________
🚀 Getting Started
1. Prerequisites
If running locally, install the required packages:
Bash
pip install numpy scipy matplotlib tensorflow seaborn scikit-learn
2. Execution in Google Colab
1.	Open Google Colab.
2.	Enable GPU: Runtime > Change runtime type > T4 GPU.
3.	Upload or paste the provided code cells into the notebook.
4.	Run the Data Generation cell to create 4,000 synthetic signal samples.
5.	Run the Training cell; expect validation accuracy $>95\%$.
________________________________________
📦 Project Structure
The code is divided into five logical stages:
•	Stage 1: Data Synthesis: Generates BPSK/QPSK signals with AWGN and narrowband jamming.
•	Stage 2: Visualization: Displays constellation diagrams to inspect signal geometry.
•	Stage 3: CNN Training: Builds and trains the 1D neural network.
•	Stage 4: Inference & Remedy: Detects signal states and applies filtering logic.
•	Stage 5: Evaluation: Validates the model using a confusion matrix.
________________________________________
📊 Results & Mitigation
The primary goal is the reduction of the Bit Error Rate (BER). In our simulations, the AI correctly identifies jamming and applies a filter that reduces BER from 0.50 (unusable) to <0.01 (clean link).

