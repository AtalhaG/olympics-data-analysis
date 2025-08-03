# 🏅 Olympics Data Analysis

This repository contains exploratory data analysis (EDA) and visualization of athlete performance and characteristics in the Olympic Games, using the **[athlete_events.csv](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results)** dataset.

The goal is to understand patterns in age, height, weight, gender distribution, and medal achievements — with a special focus on Turkish athletes after the year 2000.

---

## 📁 Dataset

- **Source**: [Kaggle – 120 years of Olympic history](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results)
- **File**: `athlete_events.csv`
- **Rows**: 271,116  
- **Columns**: 15 (e.g., `Name`, `Sex`, `Age`, `Height`, `Weight`, `Team`, `Sport`, `Medal`, etc.)

---

## 🔧 Tools Used

- Python 🐍
- Pandas 🧮
- Matplotlib 📈
- Seaborn 🎨

---

## 📊 Key Analyses & Visualizations

### 🧹 Data Preprocessing
- Handled missing values in `Age`, `Height`, and `Weight`
- Created a new column `MedalPoint` with:
  - 🥇 Gold = 3 points  
  - 🥈 Silver = 2 points  
  - 🥉 Bronze = 1 point  
  - No medal = 0

---

### 📈 Scatter Plots

- Height vs. Weight by Gender  
- Height vs. Weight by Medal  
- Multi-variable scatter:  
  `hue = Sex`, `style = Medal`, `size = Age`

```python
sns.scatterplot(x="Height", y="Weight", hue="Sex", style="Medal", size="Age", data=data)

