# RBI-ATM-Payment-Systems-Infrastructure-Analysis-using-Python-
An end-to-end Python-based Exploratory Data Analysis (EDA) on RBI ATM and payment systems infrastructure. Analyzes ATM deployment (On-site vs Off-site), POS expansion, and card issuance dynamics across Public and Private sector Indian banks using Pandas, Seaborn, and statistical profiling.
----------------------------
**Project Objective**
RBI ATM & Payment Systems Infrastructure Analysis is a data-driven project evaluating the evolution of retail banking channels in India. Utilizing monthly banking stats, this analysis explores physical ATM footprints, POS terminal deployment, debit/credit card issuance patterns, and card density metrics between Public and Private sector banks. The project incorporates rigorous data cleaning (hierarchical imputation & duplicate handling), feature engineering, statistical profiling, and multivariate visualizations using Python.
-------------------

**RBI ATM & Payment Systems Infrastructure Analysis**
  An end-to-end Python data analytics project examining the evolution of retail payment infrastructure across public and private sector Indian banks using Reserve Bank of India (RBI) transaction data.
  
  Table of Contents Project Overview Key Features Data Architecture & Pipeline Feature Engineering Project Structure Installation & SetupVisualizations & Key Insights Technologies Used Project Overview Digital payment adoption and physical banking footprints have transformed rapidly across India. This project performs an in-depth Exploratory Data Analysis (EDA) on multi-year ATM, POS terminal, and credit/debit card deployment statistics.
  
  By benchmarking Public Sector Banks against Private Sector Banks, this analysis highlights structural shifts in delivery channel preferences, card issuance density, and payment point expansion .Key Features Robust Data Cleaning: Implements multi-tier Hierarchical Imputation (Bank Name $\right arrow$ Bank Category $\right arrow$ Global Median) to resolve missing values without distorting sectoral variances.

---------------------------------------
  
  Statistical Profiling: Evaluates central tendency, dispersion, skewness, and kurtosis across financial metrics.
  
  Outlier Mitigation: Applies IQR-based Winsorization (Capping) to handle heavy-tailed payment volumes without removing critical bank-level records.
  
  Multivariate Exploratory Analysis: Evaluates channel efficiency using custom-engineered ratios and correlation heatmaps.

  --------------------------------------
  
  Data Architecture & Pipeline Raw Banking Data / Synthetic RBI Feed
  
                    │
                    
                    ▼
                    
     1. Inspection & Cleaning
     
  (Duplicates Removal & Null Detection)
  
                    │
                    
                    ▼
                    
  2. Hierarchical Missing Value Imputation

 (Bank Name Median ➔ Category Median ➔ Overall Median)

                    │
     
                    ▼
     
        3. Feature Engineering
     
  (Total ATMs, POS Ratio, Off-Site Share, Card Density)
  
                    │
                    
                    ▼
                    
   5. Statistical Profiling & IQR Capping
      
                    │
      
                    ▼
      
    5. EDA Visualizations Output
    
 (Univariate, Bivariate, Multivariate Plots)
 
**Feature Engineering** 
  To gain deeper operational insights beyond raw counts, the following derived metrics were calculated: **Metric Formula Business Purpose Total** ATMs$\text{On-Site ATMs} + \text{Off-Site ATMs}$ Measures total physical ATM footprint.

  **POS-to-ATM Ratio** $\frac{\text{POS Terminals}}{\text{Total ATMs}}$ Tracks digital merchant terminal growth vs physical cash access.
  
  **Off-Site Share** (%)$\left(\frac{\text{Off-Site ATMs}}{\text{Total ATMs}}\right) \times 100$ Evaluates bank presence beyond core branch locations.
  
  **Card Density per ATM** $\frac{\text{Debit Cards}}{\text{Total ATMs}}$ Assesses physical ATM network utilization capacity.
  
  **Project Structure**├── data/
│   └── rbi_atm_card_data.csv          # Banking dataset
├── outputs/
│   ├── univariate_analysis.png        # Distribution & count plots
│   ├── bivariate_analysis.png         # Sector comparisons & scatter plots
│   └── multivariate_analysis.png      # Correlation matrix & time trends
├── rbi_infrastructure_analysis.py    # Main pipeline execution script
├── requirements.txt                   # Python dependencies
└── README.md                          # Project documentation
