# 🚢 Titanic: Machine Learning from Disaster

## Predicting Passenger Survival Using Real-World Data Analysis

![Python Version](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Last Commit](https://img.shields.io/github/last-commit/AkshataJv/Titanic---Machine-Learning-from-Disaster)
![Repo Size](https://img.shields.io/github/repo-size/AkshataJv/Titanic---Machine-Learning-from-Disaster)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

> **Note:** This is a learning project documenting my journey into machine learning and data science. It's not perfect—it's honest. I'm sharing both what worked and what didn't.

---

## 📋 Table of Contents

- [Why I Built This](#why-i-built-this)
- [Quick Start](#quick-start)
- [Project Status](#project-status)
- [What This Project Does](#what-this-project-does)
- [Key Findings](#key-findings)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [The Process](#the-process)
- [Decision Log](#decision-log)
- [What Broke (And How I Fixed It)](#what-broke-and-how-i-fixed-it)
- [Results](#results)
- [What I Learned](#what-i-learned)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [Connect With Me](#connect-with-me)

---

## 🎯 Why I Built This

**The Real Reason:**

Everyone says "start with the Titanic dataset." I wanted to understand *why* this is the go-to beginner project.

Turns out: It's not about ships. It's about learning to think with data.

**What I Wanted to Learn:**
- How to handle missing data (there's a lot of it)
- How to engineer features from messy real-world data
- How to evaluate if a model is actually working (not just getting lucky)
- How to document my thinking process for future me

**The Challenge:**

Given passenger data (age, class, gender, etc.), can I predict who survived the disaster?

Not because it's useful for time travel, but because it teaches every fundamental concept of data science.

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/AkshataJv/Titanic---Machine-Learning-from-Disaster.git
cd Titanic---Machine-Learning-from-Disaster

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook
```

**Navigate to:** `notebooks/` and run the notebooks in order

**Expected Output:** ~81% prediction accuracy on validation set

---

## 📌 Project Status

**Current Version:** v1.0.0  
**Status:** ✅ Active Development  
**Last Updated:** January 2025

**What's Working:**
- ✅ Data cleaning and preprocessing
- ✅ Feature engineering (FamilySize, Title extraction, Age binning)
- ✅ Multiple model implementations (Logistic Regression, Random Forest, SVM)
- ✅ Cross-validation framework
- ✅ Comprehensive documentation

**What's Next:**
- 🔄 Ensemble methods (Stacking, Voting)
- 🔄 Hyperparameter tuning with GridSearchCV
- 🔄 Interactive web app deployment (Streamlit)
- 🔄 Complete blog post on Medium

---

## 💡 What This Project Does

This project builds a machine learning model to predict Titanic passenger survival based on features like:

- **Demographics:** Age, Gender
- **Socioeconomic Status:** Ticket class, Fare paid
- **Family Information:** Number of siblings/spouses, parents/children aboard
- **Travel Details:** Port of embarkation, Cabin information

**Primary Goal:** Achieve >80% prediction accuracy on unseen test data

**Real Goal:** Learn to think through data problems systematically and document the entire process

---

## 🔍 Key Findings

### What the Data Revealed:

**1. Gender was the strongest predictor**
- Females: 74% survival rate
- Males: 19% survival rate
- Aligns with "women and children first" evacuation policy

**2. Passenger class mattered significantly**
- 1st class: 63% survival
- 2nd class: 47% survival
- 3rd class: 24% survival
- Socioeconomic status = access to lifeboats

**3. Age showed nuanced patterns**
- Children (<16 years): Higher survival rates
- Relationship was non-linear, requiring age binning
- 177 missing age values complicated the analysis

**4. Family size had a "sweet spot"**
- Solo travelers: Lower survival
- Small families (2-4 people): Higher survival
- Large families (5+ people): Lower survival (likely separated during evacuation)

**Most Surprising Insight:**  
The engineered "FamilySize" feature (SibSp + Parch + 1) improved model performance more than any hyperparameter tuning I attempted.

---

## 🛠️ Technologies Used

### Core Libraries:
```python
pandas==1.3.5          # Data manipulation and analysis
numpy==1.21.5          # Numerical operations
matplotlib==3.5.1      # Data visualization
seaborn==0.11.2        # Statistical visualization
scikit-learn==1.0.2    # Machine learning algorithms
jupyter==1.0.0         # Interactive notebooks
```

### Machine Learning Models:
- **Logistic Regression** (Baseline model)
- **Decision Tree Classifier** (For comparison)
- **Random Forest Classifier** (Final model - best performance)
- **Support Vector Machine** (Alternative approach)

### Development Environment:
- Jupyter Notebook for interactive analysis
- Python 3.8+
- Git & GitHub for version control

---

## 📁 Project Structure

```
Titanic---Machine-Learning-from-Disaster/
│
├── data/
│   ├── train.csv              # Training dataset (891 passengers)
│   ├── test.csv               # Test dataset (418 passengers)
│   └── gender_submission.csv  # Sample submission format
│
├── notebooks/
│   ├── 01_exploratory_data_analysis.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_model_training.ipynb
│
├── src/
│   ├── preprocessing.py       # Data cleaning functions
│   ├── features.py            # Feature engineering utilities
│   ├── models.py              # Model training & evaluation
│   └── utils.py               # Helper functions
│
├── results/
│   ├── visualizations/        # EDA plots and charts
│   └── predictions.csv        # Final predictions for submission
│
├── requirements.txt           # Python dependencies
├── .gitignore                # Git ignore rules
├── LICENSE                   # MIT License
└── README.md                 # This file
```

---

## 💻 Installation & Setup

### Prerequisites:
- Python 3.8 or higher
- pip package manager
- Jupyter Notebook

### Step-by-Step Installation:

**1. Clone the Repository:**
```bash
git clone https://github.com/AkshataJv/Titanic---Machine-Learning-from-Disaster.git
cd Titanic---Machine-Learning-from-Disaster
```

**2. Create Virtual Environment (Recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

**3. Install Dependencies:**
```bash
pip install -r requirements.txt
```

**4. Download Dataset:**
The dataset is included in the `data/` folder. Alternatively, download from:
[Kaggle Titanic Competition](https://www.kaggle.com/c/titanic/data)

**5. Launch Jupyter Notebook:**
```bash
jupyter notebook
```

---

## 🔄 The Process

### Phase 1: Exploratory Data Analysis (EDA)

**What I Did:**
- Analyzed the distribution of each feature
- Identified patterns in missing data
- Visualized survival rates across different categories
- Explored correlations between features

**Key Discovery:**  
Missing data wasn't random. Age was missing for ~20% of passengers, Cabin for ~77%, and Embarked for just 2. This required different handling strategies for each.

**Visualizations Created:**
- Survival rate by gender and class
- Age distribution histograms
- Correlation heatmaps
- Family size vs survival analysis

---

### Phase 2: Data Cleaning

**Challenge 1: Missing Age Values (177 out of 891)**

**Attempts:**
1. Drop all rows with missing age → Lost too much data
2. Fill with overall median → Ignored class-based age patterns
3. **Final solution:** Fill with median age grouped by Pclass and Sex

**Reasoning:** Age patterns varied significantly by passenger class. First-class passengers were generally older than third-class.

```python
# Implementation
df['Age'].fillna(df.groupby(['Pclass', 'Sex'])['Age'].transform('median'), inplace=True)
```

---

**Challenge 2: Missing Cabin Values (687 out of 891)**

**Attempts:**
1. Extract cabin letter as feature → Too many missing values
2. **Final solution:** Create binary "HasCabin" feature

**Reasoning:** Having a cabin number correlated with survival (wealthier passengers had cabin assignments). The presence/absence of cabin data was more informative than the cabin letter itself.

```python
# Implementation
df['HasCabin'] = df['Cabin'].notna().astype(int)
```

---

**Challenge 3: Missing Embarked Values (2 passengers)**

**Solution:** Fill with mode (most common port: Southampton)

**Reasoning:** Only 2 missing values meant minimal impact on the model. Used the most frequent value.

```python
# Implementation
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
```

---

### Phase 3: Feature Engineering

**New Features Created:**

**1. FamilySize**
```python
df['FamilySize'] = df['SibSp'] + df['Parch'] + 1
```
**Why:** Combined family members to capture total family unit size. Solo travelers and very large families both showed lower survival rates.

---

**2. IsAlone**
```python
df['IsAlone'] = (df['FamilySize'] == 1).astype(int)
```
**Why:** Binary indicator for solo travelers who had distinctly different survival patterns.

---

**3. Title Extraction**
```python
df['Title'] = df['Name'].str.extract(' ([A-Za-z]+)\.', expand=False)
```
**Why:** Titles (Mr., Mrs., Miss, Master) encode both gender and social status. Reduced 18 unique titles to 5 common categories for better model generalization.

**Title Grouping:**
- Rare titles → 'Rare'
- Mlle, Ms → 'Miss'
- Mme → 'Mrs'

---

**4. AgeGroup Binning**
```python
df['AgeGroup'] = pd.cut(df['Age'], 
                        bins=[0, 12, 18, 35, 60, 100],
                        labels=['Child', 'Teen', 'Adult', 'Middle-aged', 'Senior'])
```
**Why:** Non-linear relationship between age and survival. Children had highest survival rates. Binning captured life stages better than raw age.

---

**5. FareBin**
```python
df['FareBin'] = pd.qcut(df['Fare'], q=4, labels=['Low', 'Medium', 'High', 'VeryHigh'])
```
**Why:** Fare had extreme outliers. Binning into quartiles captured price tier rather than exact amounts.

---

### Phase 4: Model Selection & Training

**Models Tested:**

| Model | Training Accuracy | Validation Accuracy | Cross-Val Score | Notes |
|-------|------------------|---------------------|-----------------|-------|
| Logistic Regression | 80.4% | 78.9% | 79.2% ± 1.8% | Simple baseline |
| Decision Tree | 86.7% | 76.5% | 77.1% ± 2.3% | Overfitting issues |
| Random Forest | 84.3% | 81.7% | 81.0% ± 1.5% | **Best performer** |
| SVM | 83.1% | 80.2% | 80.5% ± 1.9% | Good alternative |

**Final Model Choice: Random Forest Classifier**

**Why Random Forest Won:**
1. Best validation accuracy (81.7%)
2. Most consistent cross-validation scores (±1.5% variance)
3. Handles non-linear relationships well
4. Natural feature importance ranking
5. Less prone to overfitting than single decision tree

**Final Hyperparameters:**
```python
RandomForestClassifier(
    n_estimators=100,         # 100 decision trees
    max_depth=7,              # Limit depth to prevent overfitting
    min_samples_split=10,     # Minimum samples to split a node
    min_samples_leaf=5,       # Minimum samples in leaf nodes
    random_state=42           # Reproducibility
)
```

---

## 📝 Decision Log

### Trade-off 1: Accuracy vs Interpretability
**Decision:** Random Forest over Logistic Regression  
**Trade-off:** Gained 3% accuracy but lost direct coefficient interpretation  
**Reasoning:** For a learning project, I prioritized performance while still maintaining some interpretability through feature importance analysis.

---

### Trade-off 2: Feature Engineering vs Data Collection
**Decision:** Extensive feature engineering with existing data  
**Trade-off:** Time spent creating features vs collecting more data  
**Reasoning:** Limited to Kaggle's fixed dataset. Feature engineering was the only controllable variable.

---

### Trade-off 3: Missing Data Handling
**Decision:** Impute missing values instead of dropping rows  
**Trade-off:** Introduced some noise but preserved sample size  
**Reasoning:** With only 891 training samples, couldn't afford to lose 20% due to missing ages.

---

### Trade-off 4: Model Complexity
**Decision:** Ensemble method (Random Forest) over simple model  
**Trade-off:** Longer training time and more parameters  
**Reasoning:** Small dataset meant training time wasn't a concern. Extra complexity yielded measurable performance gains.

---

## 🐛 What Broke (And How I Fixed It)

### Bug #1: Feature Leakage

**What Happened:**  
Initial model achieved 95% accuracy. Too good to be true.

**The Problem:**  
Accidentally included PassengerId in the feature set.

**How I Found It:**  
Feature importance analysis showed PassengerId as the top predictor. That made no logical sense.

**The Fix:**  
```python
# Explicitly drop ID and target columns
features = df.drop(['PassengerId', 'Survived', 'Name', 'Ticket'], axis=1)
```

**Lesson Learned:**  
Always validate feature importance. If something seems too good, investigate immediately.

---

### Bug #2: Data Type Mismatch

**What Happened:**  
Model training crashed with: `ValueError: could not convert string to float`

**The Problem:**  
After encoding, some columns still contained mixed types (strings + numbers).

**How I Found It:**  
```python
print(df.dtypes)  # Revealed 'object' type where I expected 'int64'
print(df.select_dtypes(include='object').columns)
```

**The Fix:**  
```python
# Ensure all features are numeric
df = df.apply(pd.to_numeric, errors='coerce')
```

**Lesson Learned:**  
Always check data types before feeding to sklearn. The error messages aren't always clear about the root cause.

---

### Bug #3: Overfitting

**What Happened:**  
Training accuracy: 88%, Validation accuracy: 72%

**The Problem:**  
Decision tree was too deep, memorizing training data patterns.

**How I Found It:**  
Large gap between training and validation scores indicated overfitting.

**The Fix:**  
```python
# Add constraints to prevent overfitting
DecisionTreeClassifier(max_depth=7, min_samples_leaf=5)
```

**Lesson Learned:**  
High training accuracy means nothing if the model can't generalize. Always check validation performance.

---

### Bug #4: Preprocessing Inconsistency

**What Happened:**  
Predictions on test set threw: `ValueError: X has 9 features but model was trained on 10 features`

**The Problem:**  
Applied different preprocessing steps to train vs test data.

**How I Found It:**  
Compared feature columns between train and test sets after preprocessing.

**The Fix:**  
```python
# Create reusable preprocessing function
def preprocess_data(df):
    # All preprocessing steps in one function
    # Apply consistently to train and test
    return df

train_processed = preprocess_data(train_df)
test_processed = preprocess_data(test_df)
```

**Lesson Learned:**  
Create preprocessing pipelines, don't hardcode transformations. Consistency is critical.

---

## 📊 Results

### Final Model Performance:

**Training Set:**
- **Accuracy:** 84.3%
- **Precision:** 82.1%
- **Recall:** 78.9%
- **F1-Score:** 80.5%

**Validation Set (5-Fold Cross-Validation):**
- **Mean Accuracy:** 81.0% ± 1.5%
- **Min Score:** 79.3%
- **Max Score:** 82.7%

**Kaggle Public Leaderboard:**
- **Score:** 0.789 (78.9% accuracy)
- **Rank:** Top 35% of all submissions

---

### Feature Importance:

**Top 10 Features Contributing to Predictions:**

1. **Title** (26.3%) - Social status and gender encoded
2. **Fare** (18.7%) - Wealth indicator
3. **Age** (15.2%) - Life stage matters
4. **Sex** (14.8%) - Strongest demographic predictor
5. **Pclass** (12.1%) - Socioeconomic status
6. **FamilySize** (5.4%) - Engineered feature
7. **Embarked** (3.2%) - Port of boarding
8. **SibSp** (2.1%) - Siblings/spouse count
9. **Parch** (1.4%) - Parents/children count
10. **IsAlone** (0.8%) - Solo traveler indicator

---

### Confusion Matrix:

```
                Predicted
                No    Yes
Actual   No   [105    16]
         Yes  [ 18    40]
```

**Interpretation:**
- **True Negatives (105):** Correctly predicted non-survival
- **False Positives (16):** Predicted survival but didn't survive
- **False Negatives (18):** Predicted non-survival but survived
- **True Positives (40):** Correctly predicted survival

**Where the Model Struggles:**  
Middle-aged male passengers in 2nd class with moderate fares. These cases have mixed signals that confuse the model.

---

## 🎓 What I Learned

### Technical Skills Gained:

**1. Data Cleaning is 70% of the Work**  
I spent significantly more time handling missing values and inconsistencies than building models. This is normal in real-world data science.

**2. Feature Engineering > Algorithm Selection**  
Creating the FamilySize feature improved accuracy by 4%, while switching from Random Forest to XGBoost only improved by 0.5%.

**3. Validation Strategy is Critical**  
Single train-test split gave misleading results. Cross-validation revealed the model's true performance and variance.

**4. Overfitting is Subtle**  
High training accuracy feels good, but it's meaningless if validation suffers. Always check both metrics.

**5. Domain Knowledge Matters**  
Understanding the "women and children first" policy guided my feature engineering decisions effectively.

---

### Conceptual Insights:

**1. Perfect Data Doesn't Exist**  
Every dataset has issues: missing values, outliers, inconsistencies. Learn to work with imperfection.

**2. Models Don't Understand Context**  
They find statistical patterns in numbers. You provide the domain knowledge and meaningful interpretation.

**3. Simplicity Often Wins**  
A simple model that works reliably beats a complex model that's fragile and hard to explain.

**4. Documentation is Future-Proofing**  
I returned to this code after 2 weeks. My comments and documentation saved me hours of reverse-engineering my own logic.

---

## 🔮 Future Improvements

### If I Had More Time:

**Technical Enhancements:**

1. **Ensemble Methods**  
   Combine Random Forest, XGBoost, and Logistic Regression using voting or stacking.

2. **Advanced Feature Engineering**  
   - Extract more information from Name (surnames, nationality)
   - Cabin deck level analysis
   - Interaction features (Age × Class, Sex × Fare)

3. **Hyperparameter Optimization**  
   Use GridSearchCV or RandomizedSearchCV for systematic tuning.

4. **Deep Learning Approach**  
   Build a neural network with PyTorch/TensorFlow for comparison.

5. **Deployment**  
   Create Streamlit or Flask web app for interactive predictions.

---

### Learning Goals:

1. **Peer Review**  
   Get 5 people to review this code and provide feedback on approach and code quality.

2. **Blog Post**  
   Write comprehensive Medium article explaining the journey and insights.

3. **Production Readiness**  
   Add unit tests, error handling, logging, and comprehensive documentation.

4. **Compare Approaches**  
   Study top Kaggle kernels and understand what made them successful.

---

## 🤝 Contributing

This is a learning project, but feedback and suggestions are always welcome!

### Ways to Contribute:

**1. Suggest Improvements**  
Found a better approach? Open an issue or PR to share your insights.

**2. Report Bugs**  
If something doesn't work as expected, please let me know.

**3. Share Your Experience**  
Worked on Titanic too? Let's compare approaches and learn from each other!

**4. Improve Documentation**  
Spot a typo or unclear explanation? PRs welcome!

---

### How to Contribute:

```bash
# Fork the repository on GitHub

# Clone your fork
git clone https://github.com/YOUR_USERNAME/Titanic---Machine-Learning-from-Disaster.git

# Create a feature branch
git checkout -b feature/your-improvement

# Make your changes and commit
git commit -m "Add: brief description of your changes"

# Push to your fork
git push origin feature/your-improvement

# Open a Pull Request on GitHub
```

---

## 📬 Connect With Me

I'm actively learning data science and documenting the journey. Let's connect and learn together!

**Professional:**
- 💼 **LinkedIn:** [linkedin.com/in/akshata-jadhav-5b5611344](https://linkedin.com/in/akshata-jadhav-5b5611344)
- 💻 **GitHub:** [@AkshataJv](https://github.com/AkshataJv)
- 📧 **Email:** [akshata.mjv@gmail.com]

**Writing:**
- 📝 **Medium:** medium.com/@akshata.mjv

---

### About Me:

🎓 **BTech in AI & Data Science** at K.K. Wagh Institute, Nashik  
📚 **Currently Learning:** Python, Machine Learning, Data Analysis, SQL  
🔭 **Working On:** Real-world data science projects, documenting the learning process  
💬 **Ask Me About:** My learning journey, data science struggles, project ideas  
⚡ **Fun Fact:** I Google syntax daily and I'm okay with that

---

### What I Write About:

- The honest (messy) process of learning data science
- Mistakes I've made and how I fixed them
- Lessons that tutorials skip
- Real project challenges and solutions

**Follow along if you're on a similar journey!**

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**You are free to:**
- Use this code for learning
- Modify and adapt for your projects
- Share with others

**Just remember to:**
- Give attribution
- Include the original license

---

## 🙏 Acknowledgments

- **Kaggle** - For providing the dataset and competition platform
- **K.K. Wagh Institute** - For education and support in AI & Data Science
- **The Data Science Community** - For countless tutorials, Stack Overflow answers, and inspiration
- **Every Tutorial That Confused Me** - Made me dig deeper and truly understand

---

## 📚 Resources That Helped Me

### Learning Resources:
- [Kaggle Titanic Tutorial](https://www.kaggle.com/c/titanic) - Starting point
- [Pandas Documentation](https://pandas.pydata.org/docs/) - Data manipulation
- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html) - ML algorithms
- [StatQuest (YouTube)](https://www.youtube.com/c/joshstarmer) - Understanding ML concepts
- [Real Python](https://realpython.com/) - Python and pandas tutorials

### Tools & Platforms:
- **Jupyter Notebook** - Interactive development
- **GitHub** - Version control and collaboration
- **Stack Overflow** - Debugging everything
- **Kaggle Kernels** - Learning from others' approaches

---

## 💭 Final Thoughts

This project isn't about achieving the highest Kaggle score or building the most complex model.

**It's about:**
- Learning to think systematically with data
- Documenting the messy process, not just polished results
- Building something real, breaking it, and fixing it
- Understanding WHY things work, not just WHAT works

**If you're learning data science:**

✓ Don't aim for perfection—aim for completion  
✓ Don't hide mistakes—learn from them  
✓ Don't just build—document your thinking  
✓ Don't compare your chapter 1 to someone else's chapter 20

**Remember:**

Interviewers don't hire perfect projects.  
They hire people who can solve problems.

Your project is just the proof that you can think, debug, and improve.

---

**Built with curiosity. Debugged with patience. Documented with honesty.**

*Last Updated: January 2025*

---

<div align="center">

**⭐ If this project helped you, consider starring the repo!**

**🐛 Found a bug or have a question? Open an issue!**

**💬 Want to collaborate? Reach out on LinkedIn!**

**📣 Share this with someone learning data science!**

</div>

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/AkshataJv/Titanic---Machine-Learning-from-Disaster?style=social)
![GitHub forks](https://img.shields.io/github/forks/AkshataJv/Titanic---Machine-Learning-from-Disaster?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/AkshataJv/Titanic---Machine-Learning-from-Disaster?style=social)

---

**Made with 💜 by [Akshata Jadhav](https://github.com/AkshataJv)**
