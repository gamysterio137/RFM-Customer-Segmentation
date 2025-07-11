# Customer Segmentation with RFM & K-Means Clustering

This project performs customer segmentation using the RFM (Recency, Frequency, Monetary) model and unsupervised machine learning (K-Means Clustering) on real-world e-commerce data. The goal is to categorize customers based on their purchasing behavior and derive actionable insights for business strategy.

---

## Objective

Segment customers into meaningful groups based on their purchase recency, frequency, and total monetary value. These segments help businesses:
- Identify high-value customers
- Personalize marketing and retention strategies
- Improve customer lifetime value (CLV)
- Reduce churn and boost engagement

---

## Key Techniques Used

- **RFM Feature Engineering** – Recency, Frequency, and Monetary value computation per customer
- **Data Cleaning & Preprocessing** – Handling missing values, cancellations, and outliers
- **K-Means Clustering** – Grouping customers based on scaled RFM values
- **Elbow Method** – Determining optimal number of clusters
- **Segmentation** – Classifying customers into Low, Mid, and High value segments
- **Data Visualization** – Count plots, box plots, 3D scatter plots, and segment profiling

---

## Dataset

- **Source**: [UCI Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Description**: Transactional data from a UK-based online retail store (2010–2011)
- **Size**: ~541,000 records  
- **Attributes**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## Project Workflow

1. **Data Cleaning**  
   - Removed rows with missing `CustomerID`
   - Excluded cancelled transactions and non-positive quantities/prices

2. **RFM Calculation**  
   - `Recency`: Days since last purchase  
   - `Frequency`: Number of purchases  
   - `Monetary`: Total amount spent  

3. **Feature Scaling & Clustering**  
   - Applied StandardScaler on RFM values  
   - Used Elbow Method to choose `k = 4` for K-Means  
   - Clustered customers into 4 groups

4. **RFM Scoring & Segment Labeling**  
   - Assigned R, F, M scores (0–3) per customer  
   - Computed total `RFM_Score` and labeled segments:
     - `0–2`: Low Value  
     - `3–4`: Mid Value  
     - `5–9`: High Value  

5. **Visualization**  
   - Countplot of segments  
   - Boxplots of monetary values by segment  
   - 3D scatter plot of RFM clusters

---

## Visuals

- 3D Cluster Plot of Recency, Frequency, and Monetary  
- Elbow Plot to determine optimal `k`  
- Segment-wise distributions and spending profiles

---

## Conclusion

This project demonstrates how unsupervised learning and transactional data can be used to uncover valuable customer insights. By segmenting customers based on RFM values, businesses can tailor their marketing efforts, improve customer engagement, and drive long-term growth.

---

## Tools & Technologies

- Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)
- Jupyter Notebook
- Excel / CSV for dataset


