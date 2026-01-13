1. Methods Used
🔹 Image Processing

- Gaussian Blur: Used to reduce noise before further processing.

- Contours Detection:
    - Detecting license plate regions
    - Segmenting individual characters from the plate

🔹 Feature Extraction

- HOG (Histogram of Oriented Gradients): Extracts shape and edge features, mainly used for character recognition.

- LBP (Local Binary Pattern): Captures texture information and improves robustness under varying lighting conditions.

🔹 Random Forest

- Used for license plate classification (plate / non-plate)

- Used for character recognition (0–9, A–Z)

2. Dataset
📁 License Plate Detection Dataset

plate_detection_dataset/
├── positive/   # Images containing license plates
└── negative/   # Images without license plates

📁 Character Recognition Dataset

char_dataset/
├── 0/
├── 1/
├── ...
├── 9/
├── A/
├── B/
├── ...
└── Z/

3. System Pipeline

- Image preprocessing (Gaussian blur, thresholding)

- License plate detection using contours

- Feature extraction (HOG + LBP)

- Classification using Random Forest

- Character segmentation and recognition