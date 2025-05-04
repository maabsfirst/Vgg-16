> Brain Tumor Detection (VGG16 CNN)
Short description: Binary classification of MRI scans (tumor vs. no tumor) using transfer‑learned VGG16.

Dependencies: Python 3.8+, TensorFlow/Keras, OpenCV, numpy, pandas, scikit-learn, matplotlib, kaggle.

Setup & Run:

# install
git clone <repo>
cd repo
pip install -r requirements.txt
# configure kaggle API
mkdir -p ~/.kaggle && cp kaggle.json ~/.kaggle/
# download data
kaggle datasets download -d ahmedhamada0/brain-tumor-detection -p data/
unzip data/brain-tumor-detection.zip -d data/
# train
python train.py

Key steps: data loading → resize/normalize → augmentation → fine‑tune VGG16 → train & evaluate.

Results: ~96.7% test accuracy, AUC ~0.98.

Next: cross‑validation, other backbones, 3D CNNs, deployment.

© Maab Nawaz — MIT License
