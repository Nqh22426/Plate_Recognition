# Plate Recognition

## Methods Used
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

## Dataset
📁 License Plate Detection Dataset

plate_detection_dataset/
├── positive/   # Images containing license plates
└── negative/   # Images without license plates

📁 Character Recognition Dataset

char_dataset/  # Images containing characters (26 Alphabet, 10 natural numbers)
├── 0/
├── 1/
├── 2/
├── ...
├── 9/
├── A/
├── B/
├── ...
└── Z/

## System Pipeline
- Image preprocessing (Gaussian blur, thresholding)
- License plate detection using contours
- Feature extraction (HOG + LBP)
- Classification using Random Forest
- Character segmentation and recognition

## How to run
1. Copy each code section to Google Colab
2. Create folder "license_plate_recognition" in Google Drive
3. Create required datasets above in that folder
4. Upload a vehicle image for testing (name "test_image") in that folder
5. Run all code sections