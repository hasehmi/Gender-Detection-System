# Real-Time Gender Detection

Detects faces in a live webcam feed and classifies each as male/female in real time, using Haar Cascade face detection + a Random Forest classifier on flattened face images — a lightweight approach that runs on ordinary hardware without a GPU.

## Project structure

```
├── gender_detection.ipynb   # Training + live webcam detection
└── requirements.txt
```

## Important: running the live detection

The training section runs anywhere (Colab, local, etc.) and only needs a Kaggle account for `kagglehub` to fetch the dataset. **The live webcam detection section must be run locally on a machine with a physical webcam** — it opens `cv2.VideoCapture(0)` and will hang in any cloud notebook (Colab, Kaggle notebooks, etc.), which have no camera access.

## Approach

1. **Face detection** — Haar Cascade (OpenCV's pretrained, fast face detector — no training needed).
2. **Classification** — faces are resized to 64×64 and flattened, then classified by a Random Forest. A Random Forest (not a CNN) is used deliberately: with only ~340 usable training images, a deep network would be prone to overfitting, while a Random Forest on pixel features is a reasonable, fast baseline.
3. **Live inference** — each detected face is classified and drawn on the video feed with a confidence percentage.

## Dataset

[Gender Detection Face dataset](https://www.kaggle.com/datasets/gmlmrinalini/genderdetectionface) (Kaggle), loaded via `kagglehub`. Capped at 1000 images per class for fast training; the actual dataset provided ~340 usable images total.

## Results

| Step | Result |
|---|---|
| Dataset | 340 face images |
| Classifier | Random Forest on flattened 64×64 images |
| Test accuracy | 86.76% |

## Running it locally

```bash
pip install -r requirements.txt
jupyter notebook gender_detection.ipynb
# Run the training cell first, then the live-detection cell (needs a webcam)
```

## What I'd improve with more time

- The dataset is small (340 images) — more data would give a more reliable accuracy estimate.
- Replace flattened-pixel Random Forest with a small CNN or pretrained face-embedding model — flattening throws away spatial structure a CNN would naturally use.
- Add lighting/pose augmentation, since both Haar Cascade detection and flattened-pixel classification are sensitive to lighting and head angle in a live feed.