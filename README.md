# Customer Segmentation Project
This project focuses on customer segmentation using transactional data from an online retail store. 
  
### Using RFM Analysis + K-Means Clustering  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/sharmacharvi/customer-segmentation-project/blob/main/customer_segmentation.ipynb)

---

## Project Overview  
This project performs **customer segmentation** using the *Online Retail Transactions Dataset*.  
The goal is to group customers based on their purchasing behaviour so that businesses can:

- Target the right customers  
- Improve marketing strategies  
- Increase sales and customer satisfaction  

The project uses **RFM Analysis (Recency, Frequency, Monetary)** combined with the **K-Means clustering algorithm** to identify meaningful and actionable customer groups.

---

## Dataset Used  
The dataset is loaded using **Kaggle’s Croissant API** and includes:

- InvoiceNo  
- StockCode  
- Description  
- Quantity  
- InvoiceDate  
- UnitPrice  
- CustomerID  
- Country  

These fields help build customer profiles and measure purchasing behaviour.

---

## Project Steps  
### **1. Data Loading**
- Loaded dataset using `mlcroissant` directly from the Kaggle Croissant URL.

### **2. Data Cleaning**
- Removed missing CustomerID values  
- Removed negative/zero Quantity  
- Removed zero UnitPrice  
- Standardized column names  

### **3 Feature Engineering**
- Created **RFM (Recency, Frequency, Monetary)** features per customer  
- Recency = Days since last purchase  
- Frequency = Count of invoices  
- Monetary = Average Unit Price  

### **4. Standardization**
- Scaled features using `StandardScaler`

### **5. Clustering**
- Used **K-Means** clustering  
- Best number of clusters selected using **Silhouette Score**  
- Assigned each customer to a cluster  

### **6. Visualisation**
- 3D scatter plot using Plotly (Recency-Frequency-Monetary)  
- Color-coded cluster groups  

### **7. Exporting Results**

## Generated File: `customer_segments.csv`

This CSV file contains the **final segmented customers** after performing  
RFM analysis and K-Means clustering. It is the main output of the project.

### **File Contents**

| Column Name | Description |
|------------|-------------|
| **CustomerID** | Unique ID of each customer |
| **Recency** | Days since customer last made a purchase |
| **Frequency** | Number of invoices (transactions) by the customer |
| **Monetary** | Average spending (UnitPrice) of the customer |
| **Cluster** | Assigned customer group based on K-Means |

---

###  **Example Preview**
*(This is just a sample structure — actual values will vary)*

| CustomerID | Recency | Frequency | Monetary | Cluster |
|------------|---------|-----------|----------|---------|
| 12345 | 12 | 4 | 10.5 | 0 |
| 17890 | 45 | 2 | 18.3 | 1 |
| 15432 | 8 | 7 | 5.0 | 2 |
| 19002 | 21 | 3 | 12.1 | 0 |

---

###  **Use of the File**
The output can be used for:

- Identifying high-value customers  
- Segment-based marketing campaigns  
- Customer retention strategies  
- Behavioural analytics  



