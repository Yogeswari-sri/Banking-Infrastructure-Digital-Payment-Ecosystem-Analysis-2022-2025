# India’s Banking Payment and ATM Infrastructure dataset-using-Python-
An end-to-end Python-based Exploratory Data Analysis (EDA) on RBI ATM and payment systems infrastructure. Analyzes ATM deployment (On-site vs Off-site), POS expansion, and card issuance dynamics across Public and Private sector Indian banks using Pandas, Seaborn, and statistical profiling.

----------------------------
**Project Objective**
The Primary Objective of this project is to profile banking performance across commercial and specialized banking sectors by evaluating four key operational pillars:
1.	Customer Card Adoption
2.	Spending Efficiency
3.	Merchant QR Integration
4.	ATM Infrastructure Deployment Strategies
Rather than viewing all banks as a single monolith, this project breaks down how full-service commercial mega-banks compare against niche, specialized payment institutions."

-------------------

**India’s Banking Payment and ATM Infrastructure dataset**

To achieve this primary objective, I structured the analysis around four core statistical sub-goals:

•	First, Quantifying Central Tendency & Data Dispersion: Measuring averages (Mean) and median customer touchpoints, while analyzing Variance, Standard Deviation, Skewness, and Kurtosis to ensure mega-banks do not distort industry standards.

•	Second, Profiling Single Features through Univariate Analysis: Examining the exact distribution of total cardholder bases and evaluating customer spending patterns (avg_spend_per_cc) using histograms and boxplots to spot high-value performance outliers.

•	Third, Assessing Channel Synergy through Bivariate Analysis: Evaluating how card volume converts into actual transaction processing value, ranking institutions by spending efficiency, and calculating correlation matrices between merchant QR networks and debit card adoption.

•	Fourth, Evaluating Network Strategy through Multivariate Analysis: Analyzing On-Site versus Off-Site ATM footprints to determine if institutions prioritize branch-centric operations or retail convenience, while mapping multi-channel interactions across Credit, Debit, and QR ecosystems simultaneously using pairplots.

---------------------------------------
  
  Statistical Profiling: Evaluates central tendency, dispersion, skewness, and kurtosis across financial metrics.
  
  Outlier Mitigation: Applies IQR-based Winsorization (Capping) to handle heavy-tailed payment volumes without removing critical bank-level records.
  
  Multivariate Exploratory Analysis: Evaluates channel efficiency using custom-engineered ratios and correlation heatmaps.

  --------------------------------------
  
  **Data Architecture & Pipeline Raw Banking Data / Synthetic RBI Feed**
  
**1. Inspection & Cleaning**
     
  (Duplicates Removal & Null Detection)
  
**2. Hierarchical Missing Value Imputation**

 (Bank Name Median ➔ Category Median ➔ Overall Median)

**3. Feature Engineering**
     
  (Total ATMs, POS Ratio, Off-Site Share, Card Density)
  
**4. Statistical Profiling & IQR Capping**
  
**5. EDA Visualizations Output**
    
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
