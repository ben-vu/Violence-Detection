# 🥊 Violence Detection in Videos using Transformer Models

This project implements an AI system designed to automatically identify violent content in video streams. Using a dataset of hockey clips, the system employs Transformer-based architectures to classify videos into binary categories: **Fight** (Label 1) or **Non-Fight** (Label 0).

## 🚀 Features

- **Transformer-based Architecture**: Leverages self-attention mechanisms to handle complex temporal relationships across video frames.
- **End-to-End Pipeline**: Integrated workflow covering data acquisition, frame extraction, and model evaluation.
- **Automated Data Management**: Seamless dataset downloading and integrity verification via `kagglehub`.
- **GPU Acceleration**: Built-in support for CUDA to handle intensive video processing and training.

## 🧠 Requirements

- Python 3.x
- Jupyter Notebook or Google Colab
- Installed Python packages:
  `pip install torch torchvision opencv-python numpy matplotlib scikit-learn kagglehub`
- Active Kaggle account (for dataset access)

## ⚙️ How It Works

1. **Data Acquisition & Preprocessing**:
   - Downloads the **Hockey Fight Detection Dataset** (~1000 clips in .avi format).
   - Extracts individual frames and performs resizing/normalization.
2. **Temporal Modeling**:
   - The Transformer model analyzes sequences of frames rather than isolated images.
   - It identifies motion patterns and player interactions indicative of violence.
3. **Training & Validation**:
   - Data is split into **80% Training**, **10% Validation**, and **10% Testing**.
   - Uses fixed random seeds to ensure result reproducibility.
4. **Evaluation**:
   - Models are tested on unseen data to generate performance metrics including accuracy and loss.

## 📊 Results

The model achieves performance by analyzing three primary indicators:
- **Motion Patterns**: High-velocity transitions typical of physical altercations.
- **Player Interactions**: Proximity and contact dynamics.
- **Temporal Relationships**: How actions evolve over a specific frame window.

| Metric | Score |
| :--- | :--- |
| **Training Accuracy** | 98.75% |
| **Validation Accuracy** | 96.00% |
| **Test Accuracy** | 94.00% |

## 📁 Project Structure

- `Violence_Detection_Transformer_Models.ipynb`: Main notebook containing the full pipeline from data loading to evaluation.
- `requirements.txt`: List of necessary Python dependencies.
- `README.md`: Project documentation and setup guide.

## ⚠️ Ethical Considerations

- **Misclassification Risks**: Potential for false positives/negatives in security-critical contexts.
- **Privacy Concerns**: Implications of automated surveillance in public or private spaces.
- **Dataset Bias**: The model is optimized for sports-specific violence; performance may differ in other environments.

## 📄 License

This project is intended for educational and research purposes.
