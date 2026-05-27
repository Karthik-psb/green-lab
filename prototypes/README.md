# Prototypes

Code, notebooks, and model experiments for green-lab.

We are currently in Phase 0 (research and scoping). This folder is empty but planned structure is documented below.

## Planned Structure

prototypes/
- disease-detection/ — crop disease classification experiments
  - notebooks/ — Jupyter notebooks for training and evaluation
  - models/ — saved model weights and configs (use Git LFS for large files)
  - src/ — Python modules for data loading, training, inference
  - requirements.txt — Python dependencies
- irrigation-scheduling/ — irrigation advisory model (Phase 3)
- yield-prediction/ — satellite-based yield prediction (Phase 2-3)
- android-app/ — Android client for the disease detection MVP

## Tech Stack

- Python 3.10+, PyTorch + TorchVision
- On-device inference: TensorFlow Lite (Android, wider budget device support)
- Model targets: EfficientNet-Lite or MobileNetV3 for on-device; ResNet-50 for server-side research
- Android: Kotlin, minSdkVersion 21 (Android 5.0), targets 90% of Indian active Android devices
- Data management: DVC for large file tracking

## Contribution Guidelines

- Notebooks must run top-to-bottom without modification
- No hardcoded paths — use relative paths or environment variables
- Log all experiments (Weights and Biases or MLflow)
- Commit a model card with each checkpoint: training data, accuracy, failure modes, ethical considerations
