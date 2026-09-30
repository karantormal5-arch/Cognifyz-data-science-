# Cognifyz Technologies - Data Science Internship

Data analysis of a restaurant dataset (9,551 restaurants, 21 columns) completed as part of the **Cognifyz Technologies Data Science Internship**. I completed **Level 1** and **Level 2** of the task list.

**Author:** Karan Tormal

---

## Repository Structure

```
.
├── Cognifyz_Level1.ipynb      # Level 1: Exploration, Descriptive & Geospatial Analysis
├── Cognifyz_Level2.ipynb      # Level 2: Table Booking/Delivery, Price Range, Feature Engineering
├── Dataset_.csv               # Original dataset
├── Dataset_engineered.csv     # Dataset with engineered features (output of Level 2, Task 3)
└── README.md
```

---

## Level 1

| Task | What was done |
|------|---------------|
| **Task 1: Data Exploration & Preprocessing** | Checked shape (9,551 rows x 21 columns), handled missing values (only `Cuisines` had 9, filled with "Unknown"), converted data types, analysed the target `Aggregate rating` and its class imbalance |
| **Task 2: Descriptive Analysis** | Mean, median, std and skew of numerical columns; distribution of Country Code, City and Cuisines; top cuisines and cities |
| **Task 3: Geospatial Analysis** | Plotted restaurant locations (latitude/longitude), distribution across cities and countries, correlation between location and rating |

**Key findings**
- The target is imbalanced: *Average* 39.1%, *Not rated* 22.5%, *Good* 22.0%, *Very Good* 11.3%, *Excellent* 3.2%, *Poor* 1.9%.
- Top cuisines: North Indian (3,960), Chinese (2,735), Fast Food (1,986). Top city: New Delhi (5,473).
- About 90.6% of restaurants are from Country Code 1, so the data is heavily concentrated in one country.
- Latitude/Longitude have only a weak correlation with rating (-0.12 / -0.21), so these are not strong predictors on their own.

---

## Level 2

| Task | What was done |
|------|---------------|
| **Task 1: Table Booking & Online Delivery** | Percentage of restaurants offering each service, average rating with vs without table booking, online delivery across price ranges |
| **Task 2: Price Range Analysis** | Most common price range, average rating per price range, rating colour analysis |
| **Task 3: Feature Engineering** | Created name length, address length, number of cuisines, and binary features (`Has Table Booking`, `Has Online Delivery`, `Is Delivering Now`) |

**Key findings**
- 12.1% of restaurants offer table booking and 25.7% offer online delivery.
- Restaurants with table booking have a higher average rating (3.44 vs 2.56).
- Online delivery is most common in price range 2 (41.3%) and least common in price range 4 (9.0%).
- Most common price range is 1 (46.5% of restaurants). Average rating rises with price range, from about 2.0 (range 1) to about 3.8 (range 4).
- The colour with the highest average rating is **Dark Green** (about 4.66, the *Excellent* class).

---

## How to Run

1. Clone the repository
   ```bash
   git clone <your-repo-link>
   cd <repo-folder>
   ```
2. Install the requirements
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   pip install folium   # optional, for the interactive map in Level 1
   ```
3. Keep `Dataset_.csv` in the same folder as the notebooks, then open them
   ```bash
   jupyter notebook
   ```
4. Run all cells (Kernel → Restart & Run All).

---

## Tools Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

---

#cognifyz #cognifyzTech #cognifyzTechnologies
