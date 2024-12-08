# Age and Gender Prediction from Face Images

## Project Overview
Multi-task deep learning model for simultaneously predicting age and gender from facial images, with a focus on bias mitigation and ethical considerations. The project implements progressively improved versions (v0, v1, v2) with enhanced architectures and bias mitigation strategies.

## Key Features
- Multi-task learning for age and gender prediction
- Confidence estimation for predictions
- Bias mitigation strategies
- Comprehensive evaluation across demographics
- Model interpretability analysis

## Model Performance (v2)
- Age Prediction: 4.34 years MAE
- Gender Classification: 91.25% accuracy (95.01% for high-confidence predictions)
- Age Confidence Rate: 100%
- Gender Confidence Rate: 83.32%

## Requirements
### Hardware
- NVIDIA RTX 3070 8GB VRAM (or similar)
- 16GB RAM
- Multi-core CPU (tested on AMD Ryzen 5800H)

### Software
- Python 3.8+
- PyTorch 2.0+
- CUDA 11.8+ (for GPU support)
- See requirements.txt for full dependencies

## Installation
```bash
# Clone the repository
git clone [your-repo-url]
cd [repo-name]

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Project Structure
```
.
├── notebooks/
│   ├── v0.ipynb        # Initial implementation
│   ├── v1.ipynb        # Enhanced architecture
│   └── v2.ipynb          # Final version with all improvements
├── data/
│   └── UTKFace/                # Dataset directory
├── README.md
└── requirements.txt
```

## Usage
1. First, place the UTKFace dataset in the data directory
2. Run the notebooks in order (v0 → v1 → v2)
3. Each notebook contains:
   - Data preprocessing
   - Model training
   - Evaluation
   - Bias analysis
   - Visualization

## Model Versions

### v0 (Baseline)
- Basic CNN architecture
- Simple multi-task learning
- Basic data augmentation

### v1 (Improved)
- Enhanced CNN with attention
- Improved loss weighting
- Better data handling
- LIME interpretability

### v2 (Final)
- Age-specific model branches
- Confidence estimation
- Advanced data augmentation
- Comprehensive bias mitigation

## Ethical Considerations
- Model shows bias towards certain demographics
- Not suitable for critical decision-making
- Should not be used for legal/financial applications
- Requires human oversight for sensitive applications

## License
MIT License

## Author
Petar krešimir Borić

## Acknowledgments
- UTKFace dataset
- The model architecture and bias mitigation strategies are inspired by:
CopyDas, A., Dantcheva, A., & Bremond, F. (2018). Mitigating Bias in Gender, Age and Ethnicity Classification: a Multi-Task Convolution Neural Network Approach. In European Conference on Computer Vision (ECCV) Workshops.
