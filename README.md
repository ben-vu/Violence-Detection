🥊 Violence Detection in Videos using Transformer Models

📌 Overview

The goal of this project is to build an AI system capable of automatically identifying violent content in videos. Using a dataset of hockey clips, we train and evaluate models that classify videos into:

Fight (Violent) → Label 1
Non-Fight (Non-violent) → Label 0

The project demonstrates:

End-to-end video data processing
Frame extraction and preprocessing
Transformer-based modeling for video classification
Evaluation of model performance

📂 Dataset
Dataset: Hockey Fight Detection Dataset
Source: Kaggle (via kagglehub)
Size: ~1000 video clips (.avi format)
Classes:
fi*.avi → Fight
no*.avi → Non-fight
📥 Download

The dataset is automatically downloaded using:

pip install kagglehub
import kagglehub
path = kagglehub.dataset_download("...")
🛠️ Project Pipeline
1. Data Acquisition & Verification
Automatically downloads dataset
Verifies dataset integrity
Confirms total number of video files
2. Data Exploration
Random video sampling (fight vs non-fight)
Video playback (converted from .avi → .mp4)
Frame inspection using OpenCV
3. Preprocessing
Extract frames from videos
Resize and normalize frames
Convert videos into model-friendly format
4. Dataset Splitting
Train / Validation / Test split:
80% Training
10% Validation
10% Testing
5. Model Development
Transformer-based architecture for video classification
Handles temporal relationships across frames
6. Training
GPU acceleration (CUDA if available)
Reproducibility using fixed random seeds
7. Evaluation
Model tested on unseen data
Performance metrics tracked (e.g., accuracy)
🧠 Technologies Used
Python
PyTorch
OpenCV
NumPy
Matplotlib
Scikit-learn
KaggleHub
⚙️ Installation

Clone the repository and install dependencies:

git clone <your-repo-url>
cd <repo-name>
pip install -r requirements.txt

Or manually install core libraries:

pip install torch torchvision opencv-python matplotlib scikit-learn kagglehub
▶️ Usage

Run the notebook:

jupyter notebook Violence_Detection_Transformer_Models.ipynb

Or in Google Colab:

Upload the notebook
Run all cells sequentially
📊 Results

The model learns to distinguish between fight and non-fight scenes by analyzing:

Motion patterns
Player interactions
Temporal frame relationships

(Add your final accuracy, loss curves, or confusion matrix here if available)

🚀 Future Improvements
Use larger and more diverse violence datasets
Implement advanced video transformers (e.g., TimeSformer, ViViT)
Real-time video stream detection
Improve robustness to lighting and camera angles
Deploy as a web or surveillance system
⚠️ Ethical Considerations
Misclassification risks (false positives/negatives)
Privacy concerns in surveillance applications
Potential bias in dataset (sports-specific violence only)

📄 License

This project is for educational and research purposes.
