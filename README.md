# Machine Learning Identification of Factors Associated with Exclusive Breastfeeding in Brazilian Infants

## Overview

This repository contains the complete code and analysis pipeline for the research article "Machine Learning Identification of Factors Associated with Exclusive Breastfeeding in Brazilian Infants: Cross-Sectional Analysis of the ENANI-2019 Survey". The study employs machine learning techniques to identify and quantify factors associated with exclusive breastfeeding (EBF) among Brazilian infants under six months of age.

## Study Summary

### Background
- **Objective**: Identify factors associated with exclusive breastfeeding status among Brazilian infants under six months using machine learning techniques
- **Data Source**: National Study of Child Nutrition (ENANI-2019), a comprehensive Brazilian household survey
- **Sample Size**: 1,960 infants under 6 months (46.9% exclusively breastfed)
- **Methods**: Systematic comparison of 9 machine learning algorithms with Elastic Net feature selection

### Key Findings
- **Best Model**: Logistic Regression achieved AUC 0.865 (95% CI: 0.829-0.898)
- **Strongest Risk Factor**: Previous bottle exposure (coefficient = -2.355)
- **Critical Period**: 2-4 months identified as vulnerable timeframe for EBF discontinuation
- **Selected Features**: 49 features from 118 available variables through Elastic Net regularization

## Repository Structure

```
predicao-amamentacao/
│
├── 1 - Dicionário_features/        # Feature dictionary and data exploration
│   ├── README.md                   # Data dictionary documentation
│   ├── analise_dados_csv.py        # Initial data analysis
│   └── gerar_features.py           # Feature generation scripts
│
├── 2 - menores de 6 meses/         # Filtering for infants <6 months
│   ├── filtrar_menores_6_meses.py  # Age filtering implementation
│   └── verificar_amamentacao.py    # Breastfeeding status verification
│
├── 3 - definição desmame/          # Weaning definition and classification
│   ├── variaveis.py                # Variable definitions
│   └── verificar_resultados.py     # Results validation
│
├── 4 - arquivo final sem bloco E/  # Data preparation without Block E
│   ├── remover_bloco_e.py          # Remove Block E variables
│   └── reorganizar_csv.py          # CSV reorganization
│
├── 5 - limpeza e pre processamento/ # Data cleaning and preprocessing
│   ├── missing.ipynb                # Missing data analysis
│   └── missing_cleaned.ipynb        # Cleaned dataset generation
│
├── 6 - limpeza e pre processamento/ # Advanced preprocessing
│   ├── limpeza_nearzero.ipynb      # Near-zero variance removal
│   └── avaliacao.ipynb             # Data quality assessment
│
├── 7 - limpeza do banco de dados/   # Database cleaning
│   └── transformandotarget2em0.ipynb # Target variable transformation
│
├── 8 - limpeza das variáveis/      # Variable cleaning and documentation
│   ├── limpeza.ipynb                # Variable cleaning pipeline
│   └── variable_documentation.md    # Variable descriptions
│
├── 9 - Train-Test DS/               # Train-test split implementation
│   └── train.ipynb                  # Dataset splitting procedures
│
├── 10 - Robust e regularizacao/    # Regularization and model selection
│   ├── robust-lasso.ipynb          # Lasso, Ridge, and Elastic Net comparison
│   └── elastic_net_selected_features.csv # Final feature selection
│
└── 11 - Algoritmo/                  # Final algorithm implementation
    ├── algo.ipynb                   # Model training and evaluation
    └── verificadordeporcentagem.ipynb # Performance validation

```

## Methodology

### Data Processing Pipeline
1. **Data Filtering**: Selected infants under 6 months from ENANI-2019 dataset
2. **Target Definition**: Applied WHO criteria for exclusive breastfeeding classification
3. **Feature Engineering**: Systematic reduction from 741 to 118 features
4. **Dimensionality Reduction**: Elastic Net regularization selected 49 final features
5. **Model Selection**: Compared 9 ML algorithms using nested cross-validation
6. **Validation**: Independent hold-out test set (20% of data)

### Machine Learning Algorithms Evaluated
- Logistic Regression (selected as optimal)
- Random Forest
- XGBoost
- LightGBM
- Gradient Boosting
- Support Vector Machine
- Decision Tree
- k-Nearest Neighbors
- Gaussian Naive Bayes

## Requirements

### Python Libraries
```python
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
xgboost>=1.5.0
lightgbm>=3.3.0
shap>=0.40.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

### Installation
```bash
# Clone the repository
git clone https://github.com/marcelosilva2604/predicao-amamentacao.git
cd predicao-amamentacao

# Install required packages
pip install -r requirements.txt
```

## Usage

### Running the Complete Pipeline
```python
# 1. Start with data filtering (folder 2)
python "2 - menores de 6 meses/filtrar_menores_6_meses.py"

# 2. Define outcome variable (folder 3)
python "3 - definição desmame/variaveis.py"

# 3. Clean and preprocess data (folders 5-8)
# Run Jupyter notebooks in sequential order

# 4. Perform train-test split (folder 9)
# Run train.ipynb

# 5. Apply regularization and select features (folder 10)
# Run robust-lasso.ipynb

# 6. Train and evaluate final model (folder 11)
# Run algo.ipynb
```

## Key Results

### Model Performance
- **AUC-ROC**: 0.865 (95% CI: 0.829-0.898)
- **Accuracy**: 79.8%
- **Sensitivity**: 81.5%
- **Specificity**: 78.4%

### Top Risk Factors (Negative Associations)
1. Previous bottle exposure: β = -2.355
2. Infant age (months): β = -1.101
3. Previous pacifier use: β = -0.627

### Top Protective Factors (Positive Associations)
1. Sought breastfeeding information: β = 0.597
2. Donated breast milk: β = 0.484
3. Birth weight: β = 0.370

## Reproducibility

All analyses use fixed random seeds (`random_state=42`) to ensure complete reproducibility. The code is designed to be run sequentially through the numbered folders.

## Data Availability

The original ENANI-2019 data are subject to the sharing policies of the national survey and can be requested from the study coordinators. Due to data protection regulations, the raw dataset is not included in this repository.

## Citation

If you use this code or methodology in your research, please cite:

```bibtex
@article{silva2025machine,
  title={Machine Learning Identification of Factors Associated with Exclusive
         Breastfeeding in Brazilian Infants: Cross-Sectional Analysis of the
         ENANI-2019 Survey},
  author={[Authors]},
  journal={[Journal]},
  year={2025},
  doi={[DOI]}
}
```

## Ethics

This secondary analysis of ENANI-2019 data was approved by the Research Ethics Committee (CAAE: 88863325.0.0000.0243) and followed the principles of the Declaration of Helsinki.

## Contributing

We welcome contributions to improve the analysis pipeline. Please submit issues for bugs or feature requests, and pull requests for code contributions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or collaboration opportunities, please contact the corresponding author through the repository issues or via the journal publication.

## Acknowledgments

- The Brazilian Ministry of Health for supporting the ENANI-2019 survey
- All families who participated in the ENANI-2019 study
- The research teams involved in data collection and processing

---

**Note**: This repository contains the analytical code only. The ENANI-2019 dataset must be obtained separately through official channels due to data protection regulations.