# 🔬 Melanoma Skin Cancer Classifier

Upload any skin lesion photo and this AI model will tell you the probability that it's benign or malignant — built with a YOLOv8 classification model trained on over 10,000 real dermoscopic images.

Simply pick an image from your device, and the tool analyzes it in seconds, showing the predicted class and confidence percentage directly on the photo.

## ✨ Features

- Analyze **any skin lesion image** you choose from your own device
- Get an instant prediction: **benign** or **malignant**, with a confidence percentage
- Built on **YOLOv8** (Ultralytics) classification architecture
- Trained on a real-world dermoscopic image dataset from Kaggle
- Simple file-picker interface — no complicated setup to run a prediction
- Visual output with the result displayed directly on the image

## 🎯 Model Performance

| Metric | Score |
|--------|-------|
| Top-1 Accuracy | **92.5%** |
| Training epochs | 12 (early stopped from 20) |
| Model size | ~3 MB |
| Base architecture | YOLOv8n-cls |

Trained and validated on a held-out test set of 1,000 images, separate from the training data.

## 📊 Dataset

This project uses the **Melanoma Skin Cancer Dataset of 10,000 Images** from Kaggle, containing dermoscopic images labeled as `benign` or `malignant`.

Dataset source: [Kaggle - Melanoma Skin Cancer Dataset](https://www.kaggle.com/datasets/hasnainjaved/melanoma-skin-cancer-dataset-of-10000-images)

## 📦 Requirements

- Python 3.9 or newer
- No GPU required for inference (runs on CPU)

## 📥 Clone the Repository

```bash
git clone https://github.com/kamandNajari/Melanoma_Skin_Cancer_Classifier.git
cd Melanoma_Skin_Cancer_Classifier
```

## 🚀 Installation

```bash
pip install -r requirements.txt
```

If you don't already have PyTorch installed, install the lightweight CPU version first:

```bash
pip install torch --index-url https://download.pytorch.org/whl/cpu
```

## 📓 Running the Notebook

Make sure you have Jupyter installed:

```bash
pip install jupyter
```

Then launch it:

```bash
jupyter notebook
```

Open `melanoma.ipynb` from the Jupyter interface and run the cell (Shift + Enter).

## ▶️ How to Use

1. Run the notebook cell — a file picker window will open
2. Select any skin lesion image from your device (`.jpg`, `.jpeg`, `.png`, or `.bmp`)
3. The model analyzes the image and displays the result directly on it:
   - **Green label** → predicted benign, with confidence percentage
   - **Red label** → predicted malignant, with confidence percentage

## 🛠️ Tech Stack

- [Ultralytics YOLOv8](https://docs.ultralytics.com/) — image classification model
- [PyTorch](https://pytorch.org/) — deep learning framework
- [OpenCV](https://opencv.org/) — image loading, processing, and display
- [Kaggle API](https://www.kaggle.com/docs/api) — dataset access during training

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Medical Disclaimer

This project is for **educational and research purposes only**. It is **not a certified medical device** and its predictions should **never** be treated as a diagnosis. The model's output is a probability estimate based on a limited training dataset and can be wrong. If you notice any concerning skin changes, please consult a qualified dermatologist or physician for a proper evaluation.

---

Thank you for checking out this project! ✨
