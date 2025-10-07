# Titanic---Machine-Learning-from-Disaster
# 🚢 Titanic Survival Prediction Project

![GitHub repo size](https://img.shields.io/github/repo-size/AkshataJv/Titanic---Machine-Learning-from-Disaster) 
![GitHub contributors](https://img.shields.io/github/contributors/AkshataJv/Titanic---Machine-Learning-from-Disaster)
![GitHub stars](https://img.shields.io/github/stars/AkshataJv/Titanic---Machine-Learning-from-Disaster?style=social)
![GitHub forks](https://img.shields.io/github/forks/AkshataJv/Titanic---Machine-Learning-from-Disaster?style=social)

A comprehensive **data analysis and machine learning project** that predicts passenger survival on the Titanic using exploratory data analysis (EDA), feature engineering, and predictive modeling. This project showcases data cleaning, visualization, and model building in Python.

---

## 📑 Table of Contents
- [Features](#-features)  
- [Installation](#-installation-instructions)  
- [Usage](#-usage)  
- [Technologies Used](Programming Languages: Python 3.x
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
Tools: Jupyter Notebook / Google Colab
Domain: Data Analysis, Machine Learning, Kaggle Competitions)

## 🛠 Technologies Used
Programming Languages: Python 3.x
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
Tools: Jupyter Notebook / Google Colab
Domain: Data Analysis, Machine Learning, Kaggle Competitions

## 🤝 Contributing
- [Contributing](Contributions are welcome! Follow these steps:

1)Fork the repository.
2)Create a new branch:
git checkout -b feature/| Column / Feature  | Description                                          |
| ----------------- | ---------------------------------------------------- |
| `Pclass`          | Passenger class (1st, 2nd, 3rd)                      |
| `Sex`             | Gender of the passenger                              |
| `Age`             | Age of the passenger                                 |
| `SibSp`           | Number of siblings/spouses aboard                    |
| `Parch`           | Number of parents/children aboard                    |
| `Fare`            | Ticket fare paid                                     |
| `Embarked`        | Port of embarkation                                  |
| `Title`           | Extracted from `Name`, e.g., Mr, Mrs, Miss           |
| `Deck`            | Extracted from `Cabin`                               |
| `family_size`     | Calculated as `SibSp + Parch + 1`                    |
| `is_alone`        | 1 if passenger is alone, 0 otherwise                 |
| `fare_per_person` | `Fare / family_size`                                 |
| `FareBin`         | Fare grouped into bins for easier modeling           |
| `IsChild`         | 1 if passenger ≤ 12 years old, else 0                |
| `AgeGroup`        | Age categories: Child, Teen, Adult, etc.             |
| `Pclass_Title`    | Combination of `Pclass` and `Title` for more context |

3)Make your changes and commit:
git commit -m "Add feature X"
4)Push to the branch:
git push origin feature/  |
| ----------------- | ---------------------------------------------------- |
| `Pclass`          | Passenger class (1st, 2nd, 3rd)                      |
| `Sex`             | Gender of the passenger                              |
| `Age`             | Age of the passenger                                 |
| `SibSp`           | Number of siblings/spouses aboard                    |
| `Parch`           | Number of parents/children aboard                    |
| `Fare`            | Ticket fare paid                                     |
| `Embarked`        | Port of embarkation                                  |
| `Title`           | Extracted from `Name`, e.g., Mr, Mrs, Miss           |
| `Deck`            | Extracted from `Cabin`                               |
| `family_size`     | Calculated as `SibSp + Parch + 1`                    |
| `is_alone`        | 1 if passenger is alone, 0 otherwise                 |
| `fare_per_person` | `Fare / family_size`                                 |
| `FareBin`         | Fare grouped into bins for easier modeling           |
| `IsChild`         | 1 if passenger ≤ 12 years old, else 0                |
| `AgeGroup`        | Age categories: Child, Teen, Adult, etc.             |
| `Pclass_Title`    | Combination of `Pclass` and `Title` for more context |
5)Open a Pull Request on GitHub.)  
- [License](This project is licensed under the MIT License. See LICENSE
 for details.  
- [Contact / Support](Author: Akshata M Jadhav

GitHub: AkshataJv

Email: akshata.mjv@gmil.com

Issues: Submit an issue)  

---

## ✨ Features
- Detailed **Exploratory Data Analysis (EDA)** with visualizations for insights.  
- Advanced **feature engineering** (family size, titles, deck, fare per person, etc.).  
- Missing value handling and categorical encoding.  
- Predictive modeling using **Logistic Regression** (easily extendable to Random Forest, XGBoost, etc.).  
- Test dataset preprocessing and **Kaggle submission-ready output**.  
- Visually appealing plots using `matplotlib` and `seaborn`.  
- Step-by-step documented workflow for beginners and intermediates.  

---

## 💻 Installation Instructions

1. **Clone the repository**  
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
