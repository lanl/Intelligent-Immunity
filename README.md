# Early Diagnostic Biomarker Analysis with Machine Learning (O#: O4878)

## Overview

This repository contains R Statistical Software (version 4.2.2) developed for analyzing and building machine learning classifers for transcriptomic and proteomic datasets to identify potential biomarkers for early diagnostic testing of diseases. 

This particular repository serves as a static snapshot of the code used in the following study: [Factors Influencing Accuracy, Interpretability and Reproducibility in the use of Machine Learning in Biology](https://www.researchsquare.com/article/rs-4171489/v1)

---

## Features

- **Data Preprocessing**:
  - Normalization of transcript and protein data to a [0,1] scale using min/max scaling.
  - Handling missing data with domain-specific methods, including imputation and feature pruning.

- **Machine Learning Classifiers**:
  - Implements Random Forest (RF), Neural Networks (NN), Generalized Linear Models (GLM), Support Vector Machines (SVM), and Naïve Bayes (NB).
  - Uses R packages such as `RandomForest`, `neuralnet`, `glmnet`, `e1071`, and `naivebayes`.

- **Feature Selection**:
  - Recursive feature elimination (RFE) for RF, NN, SVM, and NB models.
  - Elastic-net regularization for GLM to handle correlated predictors.

- **Hyperparameter Tuning**:
  - Supports automated hyperparameter optimization using 5-fold cross-validation with the `caret` package.
  - Includes grid search capabilities for model-specific parameters.

- **Model Evaluation**:
  - Computes metrics such as accuracy, sensitivity, specificity, precision, and area under the ROC curve (AUC).
  - Allows analysis of model performance with varying training set sizes.

---

## Prerequisites

- **R Version**: (version 4.2.2) or higher.
- **Required R Packages**:
Here is the complete list of required R packages for the project:

### Machine Learning Libraries:
- `randomForest`
- `glmnet`
- `naivebayes`
- `neuralnet`
- `nnet`
- `e1071`
- `klaR`
- `kernlab`
- `RSNNS`

### Basic Libraries:
- `plyr`
- `tidyverse`
- `xtable`
- `readxl`

### Visualization Libraries:
- `ggthemes`
- `hrbrthemes`
- `viridis`
- `colorspace`
- `ggpubr`

### Machine Learning Utility Libraries:
- `caret`
- `pROC`

To install all these packages, use the following command:

```R
install.packages(c(
  "randomForest", "glmnet", "naivebayes", "neuralnet", "nnet", "e1071", 
  "klaR", "kernlab", "RSNNS", "plyr", "tidyverse", "xtable", "readxl", 
  "ggthemes", "hrbrthemes", "viridis", "colorspace", "caret", "ggpubr", "pROC"
))
```
## Code Files

This repository contains two `.Rmd` R Markdown files, each dedicated to analyzing a specific dataset. Both files include code, documentation, and visualizations to facilitate understanding and reproducibility. Note that not all files are included in this repository and this code will not run out of the box. The code in this repository is meant to complement the published paper.  

### **1. `transcripts-LPS-code.Rmd`**
   - **Purpose**: This file contains the code and documentation for processing and analyzing the transcript dataset. It walks through data preprocessing steps, including normalization and handling missing values, followed by the implementation and evaluation of machine learning models.
   - **Contents**:
     - Detailed explanation of preprocessing steps specific to transcript data.
     - Implementation of multiple classifiers (Random Forest, Neural Networks, GLM, SVM, Naïve Bayes).
     - Hyperparameter tuning procedures for model optimization.
     - Visualization of model performance metrics, including accuracy and ROC curves.
     - Feature importance analysis via RFE.

---

### **2. `protien-LPS-code.Rmd`**
   - **Purpose**: This file is dedicated to the protein dataset, handling unique challenges such as higher missingness and variability. It provides a complete workflow for data preprocessing, model building, and result interpretation.
   - **Contents**:
     - Custom preprocessing pipeline for handling missing protein data, including imputation and feature pruning.
     - Training and evaluation of machine learning models tailored to the protein dataset.
     - Hyperparameter tuning for each classifier.
     - Visualizations of the dataset's structure, missingness patterns, and model performance.
     - Visualization of model performance metrics, including accuracy and ROC curves.
     - Feature importance analysis via RFE.


---

Both files are designed to be modular, enabling users to modify or extend the workflows as needed for other datasets or research objectives. They combine code execution with explanatory text to ensure clarity and accessibility.
## Applications

- Identification of early diagnostic biomarkers for diseases.
- Development of robust classifiers for "fat"(many-features-few-observations) biological data.

---

## Contact

For inquiries or access to the datasets, please contact the corresponding author. Additional details about the project and methods are provided in the associated publication. [](url) 

---

## License

This code is made available for research purposes. For other uses, contact the repository owner for permissions.

This program is Open-Source under the BSD-3 License.

 

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

 
 - Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

 
 - Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

 
 - Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

 

(End of Notice)

---

## Copyright for O# O4878
© 2025. Triad National Security, LLC. All rights reserved.

This program was produced under U.S. Government contract 89233218CNA000001 for Los Alamos National Laboratory (LANL), which is operated by Triad National Security, LLC for the U.S. Department of Energy/National Nuclear Security Administration. All rights in the program are reserved by Triad National Security, LLC, and the U.S. Department of Energy/National Nuclear Security Administration. The Government is granted for itself and others acting on its behalf a nonexclusive, paid-up, irrevocable worldwide license in this material to reproduce, prepare. derivative works, distribute copies to the public, perform publicly and display publicly, and to permit others to do so.

 

(End of Notice)


---

## Acknowledgments

This work was supported by the Defense Threat Reduction Agency (DTRA).

