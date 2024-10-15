# GANs for Stock Market Prediction

## Overview
This project leverages **Generative Adversarial Networks (GANs)** for predicting stock prices, using a **Gated Recurrent Unit (GRU)** generator and a **Convolutional Neural Network (CNN)** discriminator. GANs are capable of generating synthetic stock price sequences that mimic real-world market behavior, offering a novel approach to financial forecasting.


## Authors
- **Prof. Markos Katsoulakis**
- **Hari S. Iyer**

## Motivation
GANs have shown promising results in generating high-fidelity images and increasing resolution for various applications. In financial forecasting, they can capture complex patterns within historical data, making them an intriguing solution for stock price prediction.

## Project Structure
1. **Data Preparation**: 
   - Dataset includes the past 10 years of stock prices with 36 financial indicators.
   
2. **Model Architecture**:
   - **Generator (GRU)**: Processes input noise to generate realistic stock price sequences, capitalizing on GRU’s efficiency with sequential data.
   - **Discriminator (CNN)**: Trains to differentiate between real and generated sequences, classifying inputs as genuine or synthetic.

3. **Training Process**:
   - The GAN iteratively optimizes the discriminator’s ability to identify real versus generated data while refining the generator to produce realistic sequences. Through this min-max game, both networks improve iteratively.

4. **Evaluation**:
   - The model’s accuracy in predicting stock trends is evaluated through testing phases, with results demonstrating the potential of GANs in financial data prediction.

## Mathematical Foundation
- **Binary Cross-Entropy Loss**: Used to optimize the discriminator, which acts as a binary classifier.
- **Jensen-Shannon Divergence**: Applied to measure the similarity between the real and generated data distributions.
- **Conditional GANs (cGANs)**: Enable model precision by conditioning on additional information, enhancing the quality of generated predictions.

## Results
- The GAN model successfully generates stock price sequences that align closely with real data, improving forecast accuracy beyond traditional models.
- Visualization of generated sequences across epochs demonstrates a steady increase in realism.

## Future Work
1. **Integrate additional data sources**: such as financial news sentiment analysis.
2. **Experiment with advanced GAN variations** like Wasserstein GAN for enhanced stability.
3. **Expand model testing** on diverse stock indices to assess robustness.

## Getting Started

### Prerequisites
- Python 3.7+
- Libraries: TensorFlow, Pandas, NumPy, Matplotlib

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/GAN-stock-prediction.git
   cd GAN-stock-prediction
