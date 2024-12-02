# Solar Cell Microcrack Detection

This project is focused on detecting microcracks in solar cells using advanced preprocessing, data augmentation, and deep learning models. The pipeline includes image preprocessing, structured data augmentation, and training convolutional neural networks (CNNs) such as ResNet50 and a custom CNN architecture.

## Features

- **Image Preprocessing**: Removes noise and unwanted rows/columns in grayscale images.
- **Data Augmentation**: Includes flipping, brightness/contrast adjustments, and jittering for enhanced dataset diversity.
- **Model Training**: Trains models with a balanced dataset, pseudo-labeling for semi-supervised learning, and early stopping to avoid overfitting.
- **Performance Evaluation**: Includes custom thresholds for prediction and confusion matrix visualization.
- **Automation**: Full dataset processing for streamlined microcrack detection.

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Libraries: `torch`, `torchvision`, `opencv-python`, `numpy`, `pandas`, `tqdm`, `matplotlib`, `scikit-learn`

Install required libraries using:
```bash
pip install -r requirements.txt
```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/solar-cell-microcrack-detection.git
   ```
2. Navigate to the project directory:
   ```bash
   cd solar-cell-microcrack-detection
   ```

---

## Project Structure

- `preprocessing.py`: Handles image preprocessing by removing black rows and cropping borders.
- `augmentation.py`: Implements structured data augmentation.
- `train.py`: Contains the model training and evaluation pipeline.
- `models.py`: Includes definitions for CNN architectures (CustomCNN, ResNet50).
- `utils.py`: Utility functions for metrics and plotting results.

---

## Usage

### 1. Preprocess Images
Use `preprocessing.py` to clean and crop input images:
```bash
python preprocessing.py --input_dir ./data/raw --output_dir ./data/processed
```

### 2. Data Augmentation
Apply augmentation to expand the dataset:
```bash
python augmentation.py --input_dir ./data/processed --output_dir ./data/augmented
```

### 3. Train the Model
Train a deep learning model with preprocessed and augmented data:
```bash
python train.py --train_dir ./data/augmented --epochs 100 --batch_size 32
```

---

## Results

- Preprocessed images demonstrate significant reduction in noise.
- Models achieve high accuracy and sensitivity on microcrack detection.

Sample output:
![Example Results](example_results.png)

---

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Contact

- For questions or feedback, please contact [alirezaakhavansafaei@gmail.com](mailto:alirezaakhavansafaei@gmail.com).
- visit our site: studylab.ir

