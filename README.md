# Swahili Spam Detection - Training Repository

The training component of the Swahili Spam Detection system, containing datasets, training notebooks, and model evaluation infrastructure. This repository handles the machine learning aspects of the [main SSD project](https://github.com/patrick-paul/ssd).

## Project Structure

```bash
└── ssd-training/
    └── dataset/             # Training datasets
        └── combined_set.csv
        └── combined_set.xlsx
    └── Model_After_Training/
        └── model_after_tranining_28_jan_2025/
            └── swahiliSpamDetectionModel.pkl
        └── swahiliSpamDetectionModel.pkl
    └── stopwords/           # Swahili stopwords
        └── Common Swahili Stop-words.csv
    └── spamDetectionRef.ipynb   # Training notebook
    └── requirements.txt         # Dependencies
```

## Model Performance

### Performance Metrics

| Model                | Technique           | Accuracy | Precision | Recall | F1-score | AUC-ROC |
|---------------------|---------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | Count Vectorization | 0.9924   | 0.9925    | 0.9924 | 0.9923   | 0.9996  |
| Naive Bayes         | Count Vectorization | 0.9904   | 0.9905    | 0.9904 | 0.9905   | 0.9988  |
| SVM                 | Count Vectorization | 0.9933   | 0.9934    | 0.9933 | 0.9933   | 0.9995  |
| Random Forest       | Count Vectorization | 0.9933   | 0.9933    | 0.9933 | 0.9933   | 0.9993  |
| Logistic Regression | TF-IDF              | 0.9838   | 0.9842    | 0.9838 | 0.9837   | 0.9995  |
| Naive Bayes         | TF-IDF              | 0.9952   | 0.9952    | 0.9952 | 0.9952   | 0.9985  |
| SVM                 | TF-IDF              | 0.9914   | 0.9915    | 0.9914 | 0.9914   | 0.9999  |
| Random Forest       | TF-IDF              | 0.9924   | 0.9925    | 0.9924 | 0.9923   | 0.9998  |

## Getting Started

### Prerequisites
- Python 3.8+
- pip package manager

### Installation

1. Clone the repository
```bash
git clone https://github.com/patrick-paul/ssd-training.git
cd ssd-training
```

2. Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

## Dataset Information

- Contains over 6,000 labeled Swahili messages
- Binary classification (spam/ham)
- Available in CSV and Excel formats
- Includes regional language variations

## Model Details

### Best Performing Model
Random Forest with Count Vectorization:
- Accuracy: 0.9933
- Precision: 0.9933
- Recall: 0.9933
- F1-score: 0.9933
- AUC-ROC: 0.9993

### Key Features
- Robust against overfitting
- Consistent performance across metrics
- Excellent handling of text features
- Strong performance with Count Vectorization

## Dependencies

```
pandas
matplotlib
numpy
seaborn
nltk
scikit-learn
joblib
```

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook spamDetectionRef.ipynb
```

2. Follow the notebook sections:
   - Data preprocessing
   - Feature extraction
   - Model training
   - Performance evaluation
   - Model export

## Contributing

1. Fork the repository
2. Create your feature branch
3. Follow PEP-8 standards
4. Push your changes
5. Submit a pull request

## Future Improvements

- [ ] Expand dataset with more regional dialects
- [ ] Implement deep learning models
- [ ] Add automated model retraining pipeline
- [ ] Create comprehensive model testing suite
- [ ] Add model versioning system

## License

MIT License - See LICENSE.md for details

## Contact

- Developer: patrickpaul367@gmail.com
- GitHub: [@patrick-paul](https://github.com/patrick-paul)
- Project Link: https://github.com/patrick-paul/ssd-training

## Related Projects

- [Main SSD Application](https://github.com/patrick-paul/ssd) - The web application using these trained models