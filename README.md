# 🚀 Microsoft-Fabric-Ecommerce-Customer360

## 📌 Project Overview

This project demonstrates an end-to-end Data Engineering solution built using **Microsoft Fabric** following the **Medallion Architecture (Bronze → Silver → Gold)**.

The solution ingests raw customer data, performs data cleaning and transformation using **PySpark**, builds a business-ready **Customer360** dataset, and delivers interactive business insights through **Power BI**. The complete workflow is automated using **Microsoft Fabric Pipelines**.

---

## 🏗️ Architecture

```
                Raw CSV Files
                     │
                     ▼
           Bronze Lakehouse
          (Raw Data Storage)
                     │
                     ▼
            Bronze Notebook
                     │
                     ▼
           Silver Lakehouse
      (Data Cleaning using PySpark)
                     │
                     ▼
            Silver Notebook
                     │
                     ▼
             Gold Lakehouse
         (Customer360 Analytics)
                     │
                     ▼
             Gold Notebook
                     │
                     ▼
             Semantic Model
                     │
                     ▼
             Power BI Dashboard
                     │
                     ▼
        Microsoft Fabric Pipeline
```

---

# 📂 Project Structure

```
Microsoft-Fabric-Customer360
│
├── README.md
├── notebooks
│   ├── BronzeNotebook.ipynb
│   ├── SilverNotebook.ipynb
│   └── GoldNotebook.ipynb
│
├── screenshots
│   ├── bronze_lakehouse.png
│   ├── silver_lakehouse.png
│   ├── gold_lakehouse.png
│   ├── pipeline.png
│   ├── semantic_model.png
│   └── dashboard.png
│
└── sample_data
```

---

# 📊 Dataset

The project uses five datasets:

- Customers
- Orders
- Payments
- Support Tickets
- Web Activities

---

# ⚙️ Technologies Used

- Microsoft Fabric
- PySpark
- Microsoft Fabric Pipelines
- Lakehouse
- Delta Tables
- OneLake
- Power BI
- Semantic Model
- Data Modeling
- ETL
- Medallion Architecture

---

# Bronze Layer

### Objective

Store raw data exactly as received without applying any transformations.

### Activities

- Imported raw CSV datasets
- Created Bronze Lakehouse
- Converted CSV files into Delta Tables using PySpark
- Preserved original data for auditing purposes

Tables Created

- customers
- orders
- payments
- support_tickets
- web_activities

---

# Silver Layer

### Objective

Clean and standardize raw data.

### Data Cleaning Performed

✔ Removed duplicate records

✔ Trimmed unnecessary spaces

✔ Converted emails to lowercase

✔ Standardized customer names

✔ Standardized gender values

✔ Converted multiple date formats into DateType

✔ Replaced invalid values

✔ Converted negative amounts into positive values

✔ Handled missing values

✔ Standardized payment methods

✔ Removed invalid records

---

# Gold Layer

### Objective

Create a business-ready analytical dataset.

Created a **Customer360** table by joining:

- Customers
- Orders
- Payments
- Support Tickets
- Web Activities

The Gold layer provides a unified customer view for reporting and analytics.

---

# 📈 Power BI Dashboard

The interactive dashboard provides insights including:

- Total Customers
- Total Orders
- Total Revenue
- Average Order Value
- Payment Method Distribution
- Device-wise Revenue
- Customer Location Analysis
- Support Ticket Status
- Customer Demographics

Dashboard Screenshot

![Dashboard](Screenshots/dashboard.png)

---

# 🔄 Fabric Pipeline

The complete ETL process is automated using **Microsoft Fabric Pipeline**.

Pipeline Workflow

```
Bronze Notebook
        │
        ▼
Silver Notebook
        │
        ▼
Gold Notebook
        │
        ▼
Semantic Model Refresh
```

Features

- Automated notebook execution
- Sequential workflow
- Semantic Model refresh
- Ready for scheduled execution

Pipeline Screenshot

![Pipeline](Screenshots/pipeline.png)

---

# 💡 Key Learnings

Through this project I gained hands-on experience with:

- Medallion Architecture
- Lakehouse Architecture
- ETL Design
- Data Engineering using Microsoft Fabric
- PySpark Data Cleaning
- Delta Tables
- Fabric Pipelines
- Semantic Models
- Power BI Reporting
- Customer360 Analytics

---

# 🚀 Future Enhancements

- Incremental Data Loading
- Change Data Capture (CDC)
- Slowly Changing Dimensions (SCD)
- Parameterized Pipelines
- Automated File Ingestion using Copy Data Activity
- Data Quality Validation
- Pipeline Notifications
- CI/CD Deployment

---

# 📷 Project Screenshots

## Bronze Lakehouse

![Bronze](Screenshots/bronze_lakehouse.png)

---

## Silver Lakehouse

![Silver](Screenshots/silver_lakehouse.png)

---

## Gold Lakehouse

![Gold](Screenshots/gold_lakehouse.png)

---

## Semantic Model

![Semantic Model](Screenshots/semantic_model.png)

---

## Power BI Dashboard

![Dashboard](Screenshots/dashboard.png)

---

# 👨‍💻 Author

**Rishav Kumar**

LinkedIn: *(Add your LinkedIn profile link)*

GitHub: *(Add your GitHub profile link)*

---

## ⭐ If you found this project helpful, don't forget to star this repository.
