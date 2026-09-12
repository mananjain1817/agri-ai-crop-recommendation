# \# 🌱 AI Crop Recommendation System

# 

# An AI-based crop recommendation system that predicts a suitable crop based on soil and environmental conditions using a \*\*Random Forest Classifier\*\*.

# 

# The system takes seven agricultural parameters as input and provides a crop recommendation through a \*\*Streamlit web application\*\*.

# 

# \---

# 

# \## 📌 Project Overview

# 

# Selecting a suitable crop depends on several soil and environmental conditions. This project applies machine learning to identify patterns between these conditions and recommended crops.

# 

# The model uses the following seven input parameters:

# 

# \- Nitrogen (N)

# \- Phosphorus (P)

# \- Potassium (K)

# \- Temperature

# \- Humidity

# \- Soil pH

# \- Rainfall

# 

# Based on these inputs, the trained model predicts the most suitable crop from the available crop classes in the dataset.

# 

# \---

# 

# \## 🎯 Objectives

# 

# The main objectives of this project are:

# 

# \- Apply machine learning to an agricultural problem

# \- Build a crop recommendation model using Random Forest

# \- Use soil and environmental parameters for prediction

# \- Evaluate the model on unseen test data

# \- Save the trained machine learning model for reuse

# \- Provide an interactive prediction interface using Streamlit

# 

# \---

# 

# \## 🤖 Machine Learning Approach

# 

# \### Algorithm

# 

# The project uses a \*\*Random Forest Classifier\*\* for crop classification.

# 

# The machine learning pipeline consists of:

# 

# 1\. Dataset loading

# 2\. Data cleaning

# 3\. Feature selection

# 4\. Missing-value checking

# 5\. Stratified train-test split

# 6\. Feature scaling using `StandardScaler`

# 7\. Random Forest classification

# 8\. Model evaluation

# 9\. Model serialization using Joblib

# 

# \### Model Configuration

# 

# The Random Forest model uses:

# 

# \- `n\_estimators = 300`

# \- `random\_state = 42`

# \- `class\_weight = "balanced"`

# \- `n\_jobs = -1`

# 

# \### Dataset Split

# 

# The dataset is divided into:

# 

# \- \*\*80% training data\*\*

# \- \*\*20% testing data\*\*

# \- `random\_state = 42`

# 

# A stratified split is used so that the crop classes are proportionally represented in the training and testing sets.

# 

# \---

# 

# \## 📊 Dataset

# 

# This project uses the \*\*Crop Recommendation Dataset\*\* available on Kaggle.

# 

# \### Dataset Source

# 

# https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset

# 

# The dataset contains:

# 

# \- \*\*2,200 samples\*\*

# \- \*\*22 crop classes\*\*

# \- \*\*8 columns\*\*

# &#x20; - 7 input features

# &#x20; - 1 target label

# 

# \### Input Features

# 

# | Feature | Description |

# |---|---|

# | N | Nitrogen content |

# | P | Phosphorus content |

# | K | Potassium content |

# | temperature | Temperature |

# | humidity | Humidity |

# | ph | Soil pH |

# | rainfall | Rainfall |

# 

# \### Target

# 

# The target column is:

# 

# ```text

# label

# ```

# 

# which represents the recommended crop.

# 

# The dataset CSV is intentionally not included in the GitHub repository. It is excluded using `.gitignore`.

# 

# After downloading the dataset, place it at:

# 

# ```text

# data/Crop\_recommendation.csv

# ```

# 

# \---

# 

# \## 📈 Model Performance

# 

# The Random Forest classifier achieved:

# 

# \# \*\*99.32% Accuracy\*\*

# 

# on the held-out \*\*20% test set\*\*.

# 

# The test set contained \*\*440 samples\*\*.

# 

# \### Classification Performance

# 

# The model achieved strong classification performance across the 22 crop classes.

# 

# Most classes achieved precision, recall, and F1-scores close to \*\*1.00\*\*, with only a small number of classification errors in the test set.

# 

# The overall accuracy was:

# 

# ```text

# 0.9932

# ```

# 

# or:

# 

# ```text

# 99.32%

# ```

# 

# > \*\*Important:\*\* The 99.32% result represents performance on this specific held-out dataset. It should not be interpreted as guaranteed real-world farming accuracy.

# 

# \---

# 

# \## 🌾 Example Prediction

# 

# The trained model can predict a crop from soil and environmental conditions.

# 

# \### Example Input

# 

# | Parameter | Value |

# |---|---:|

# | Nitrogen (N) | 90 |

# | Phosphorus (P) | 42 |

# | Potassium (K) | 43 |

# | Temperature | 25°C |

# | Humidity | 80% |

# | Soil pH | 6.5 |

# | Rainfall | 200 mm |

# 

# \### Prediction

# 

# ```text

# Recommended Crop: rice

# ```

# 

# \### Top 3 Predictions

# 

# ```text

# rice: 55.00%

# jute: 44.67%

# banana: 0.33%

# ```

# 

# > These values are the model's predicted class probabilities for the example input. They should not be interpreted as guaranteed crop suitability or expected agricultural yield.

# 

# \---

# 

# \## 🖥️ Streamlit Application

# 

# The project includes a Streamlit web application that allows users to enter the seven agricultural parameters and receive a crop recommendation.

# 

# Run the application using:

# 

# ```bash

# streamlit run app.py

# ```

# 

# The application provides an interactive interface for:

# 

# \- Entering soil parameters

# \- Entering environmental conditions

# \- Generating a crop recommendation

# \- Viewing the prediction

# 

# \---

# 

# \## 🚀 Installation

# 

# \### 1. Clone the Repository

# 

# ```bash

# git clone https://github.com/mananjain1817/agri-ai-crop-recommendation.git

# ```

# 

# Move into the project directory:

# 

# ```bash

# cd agri-ai-crop-recommendation

# ```

# 

# \---

# 

# \### 2. Create a Virtual Environment

# 

# Python \*\*3.11\*\* is recommended for the current project environment.

# 

# ```bash

# python -m venv .venv

# ```

# 

# \---

# 

# \### 3. Activate the Virtual Environment

# 

# \#### Windows PowerShell

# 

# ```powershell

# .\\.venv\\Scripts\\activate

# ```

# 

# \#### Windows Command Prompt

# 

# ```cmd

# .venv\\Scripts\\activate

# ```

# 

# \---

# 

# \### 4. Install Dependencies

# 

# ```bash

# pip install -r requirements.txt

# ```

# 

# \---

# 

# \## 📥 Dataset Setup

# 

# Download the Crop Recommendation Dataset from Kaggle:

# 

# https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset

# 

# After downloading it, place the CSV file inside the `data` directory.

# 

# The required path is:

# 

# ```text

# data/Crop\_recommendation.csv

# ```

# 

# The project structure should then contain:

# 

# ```text

# data/

# └── Crop\_recommendation.csv

# ```

# 

# \---

# 

# \## 🏋️ Train the Model

# 

# After placing the dataset in the correct location, run:

# 

# ```bash

# python src/train.py

# ```

# 

# The training script will:

# 

# \- Load the dataset

# \- Display the dataset shape

# \- Check the dataset columns

# \- Check for missing values

# \- Split the data into training and testing sets

# \- Build the preprocessing pipeline

# \- Train the Random Forest classifier

# \- Calculate evaluation metrics

# \- Save the trained model

# \- Generate evaluation reports

# 

# The trained model is saved to:

# 

# ```text

# models/crop\_recommendation\_pipeline.joblib

# ```

# 

# Generated evaluation files are saved in:

# 

# ```text

# reports/

# ```

# 

# \---

# 

# \## 🔮 Command-Line Prediction

# 

# The project also provides a command-line prediction script.

# 

# Example:

# 

# ```bash

# python src/predict.py --N 90 --P 42 --K 43 --temperature 25 --humidity 80 --ph 6.5 --rainfall 200

# ```

# 

# Expected output:

# 

# ```text

# Recommended Crop: rice

# 

# Top 3 predictions:

# rice: 55.00%

# jute: 44.67%

# banana: 0.33%

# ```

# 

# \---

# 

# \## 📁 Project Structure

# 

# ```text

# agri-ai-crop-recommendation/

# │

# ├── data/

# │   └── README.md

# │

# ├── models/

# │   └── .gitkeep

# │

# ├── notebooks/

# │   └── .gitkeep

# │

# ├── reports/

# │   └── .gitkeep

# │

# ├── src/

# │   ├── train.py

# │   └── predict.py

# │

# ├── app.py

# ├── requirements.txt

# ├── .gitignore

# └── README.md

# ```

# 

# \---

# 

# \## 🛠️ Technologies Used

# 

# \- \*\*Python 3.11\*\*

# \- \*\*NumPy\*\*

# \- \*\*Pandas\*\*

# \- \*\*SciPy\*\*

# \- \*\*Scikit-learn\*\*

# \- \*\*Matplotlib\*\*

# \- \*\*Seaborn\*\*

# \- \*\*Joblib\*\*

# \- \*\*Streamlit\*\*

# \- \*\*Git\*\*

# \- \*\*GitHub\*\*

# 

# \---

# 

# \## 📦 Main Python Libraries

# 

# The project uses pinned dependency versions for reproducibility.

# 

# ```text

# numpy==2.4.6

# pandas==3.0.5

# scipy==1.17.1

# scikit-learn==1.9.1

# matplotlib==3.11.2

# seaborn==0.13.2

# joblib==1.6.0

# streamlit==1.63.0

# ```

# 

# \---

# 

# \## 🔄 Workflow

# 

# ```text

# &#x20;                ┌─────────────────────┐

# &#x20;                │   Crop Dataset      │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │   Data Processing   │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │  Train/Test Split   │

# &#x20;                │       80 / 20       │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │   Random Forest     │

# &#x20;                │     Classifier      │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │ Model Evaluation    │

# &#x20;                │     Accuracy        │

# &#x20;                │ Classification      │

# &#x20;                │     Report          │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │  Saved ML Pipeline  │

# &#x20;                └──────────┬──────────┘

# &#x20;                           │

# &#x20;                           ▼

# &#x20;                ┌─────────────────────┐

# &#x20;                │ Streamlit / CLI     │

# &#x20;                │    Prediction       │

# &#x20;                └─────────────────────┘

# ```

# 

# \---

# 

# \## ⚠️ Limitations

# 

# This project is an educational machine learning system trained on the available crop recommendation dataset.

# 

# The model's \*\*99.32% test accuracy should not be interpreted as guaranteed real-world farming accuracy\*\*.

# 

# Actual crop suitability can depend on many additional factors, including:

# 

# \- Local climate

# \- Soil type

# \- Soil quality

# \- Weather variation

# \- Irrigation availability

# \- Growing season

# \- Agricultural practices

# \- Disease and pest conditions

# \- Local geographic conditions

# 

# Therefore, predictions should be treated as \*\*machine-learning recommendations\*\*, not professional agricultural advice.

# 

# \---

# 

# \## 🔮 Future Improvements

# 

# Possible future improvements include:

# 

# \- Hyperparameter optimization

# \- Cross-validation

# \- Feature importance visualization

# \- Comparison with other machine learning algorithms

# \- Adding additional soil and environmental features

# \- Integration with real-time weather information

# \- Online deployment of the Streamlit application

# \- Improved agricultural recommendation logic

# \- Integration with IoT soil sensors

# \- Adding a CNN-based plant disease detection module

# 

# \---

# 

# \## 🎓 Academic Context

# 

# This project is developed as part of an \*\*AI / Machine Learning agricultural application\*\*.

# 

# The current implementation focuses on:

# 

# > \*\*Module A — Crop Recommendation using Random Forest\*\*

# 

# A future extension can include:

# 

# > \*\*Module B — Plant Disease Detection using CNN\*\*

# 

# \---

# 

# \## 👨‍💻 Author

# 

# \*\*Manan Jain\*\*

# 

# GitHub:

# 

# https://github.com/mananjain1817

# 

# Project Repository:

# 

# https://github.com/mananjain1817/agri-ai-crop-recommendation

# 

# \---

# 

# \## 📜 License

# 

# This project is intended primarily for educational and academic purposes.

