# Aegis-Public-Health
An end-to-end system for analyzing the impact of vaccination on mortality using COVID-19 and World Bank data. Features include statistical validation, advanced time-series modeling (SARIMAX/VAR), a governance layer for auditability, and an interactive dashboard for policy simulation.

README.md
Comprehensive COVID-19 Data Analysis System
Multi-layer Framework for Assessing Vaccination Impact on COVID-19 Mortality Across WHO Regions

Overview
This repository contains a comprehensive multi-layer COVID-19 data analysis system designed to integrate epidemiological indicators with World Bank development indicators, in order to evaluate the impact of vaccination on mortality rates across different WHO regions.
The system follows a structured end-to-end pipeline including:
•	Automated multi-source data collection
•	Robust preprocessing & regional aggregation
•	Statistical validation & model selection
•	Advanced time-series modeling with governance controls
•	Interactive policy simulation dashboard

	Key Objectives
•	Quantify the relationship between vaccination rates and mortality trends
•	Identify optimal lag times between vaccination rollout and mortality impact
•	Compare patterns across WHO regions
•	Ensure reproducibility using a structured pipeline and strong governance layer
________________________________________
	Key Features
	 Automated data acquisition from:
•	COVID-19 repositories (Google / official sources)
•	World Bank APIs (multi-year socioeconomic and development indicators)
	Data processing & validation:
•	Cleaning, missing value handling, outlier treatment
•	Regional aggregation across WHO regions
•	Vaccination start-date estimation per region/country
	Advanced statistical modeling:
•	SARIMAX (seasonality & exogenous variables)
•	VAR / VECM (multivariate modeling and causality patterns)
•	Statistical tests for stationarity, normality, and model selection
	Governance & audit layer:
•	Decision logs and rationale
•	Validation certificates
•	Anomaly detection reports
•	Audit trails for reproducibility and traceability
	Interactive dashboard:
•	Region selection
•	Policy simulation (+50% / −20% vaccination change)
•	Lag adjustment (0–120 days)
•	Real-time visual interpretation of outcomes
________________________________________
	Architecture (Layer-Based Pipeline)
Layer	Module	Description	Output
1	Data Collection	Collects COVID-19 + World Bank data	Combined CSV dataset
2	Data Processing	Cleans, preprocesses, aggregates	Cleaned & regional datasets
3	Statistical Analysis	Model tests and recommendations	JSON results and recommendations
4	Governance & Modeling	SARIMAX/VAR/VECM + reporting + governance	Reports, visualizations, logs
-	Dashboard	Interactive visualization and policy simulation	Web dashboard
	Repository Structure
covid-19-analysis-system/
│
├── src/
│   ├── layer1_data_collection.py
│   ├── layer2_data_processing.py
│   ├── layer3_statistical_analysis.py
│   ├── layer4_governance_modeling.py
│   └── dashboard.py
│
├── data/                       # Optional: sample data only
├── aggregated_data/            # Output from Layer 2
├── outputs/                    # Main outputs (plots, reports, JSON, CSV)
│   ├── csv/
│   ├── json/
│   ├── plots/
│   ├── reports/
│   └── pdf/
│
├── governance/                 # Governance logs, audit trails, decisions
├── logs/                       # System logs
│
├── docs/
│   ├── methodology.md
│   ├── data_dictionary.md
│   └── reproducibility.md
│
├── requirements.txt
├── LICENSE
└── README.md

 
Installation
Prerequisites
•	Python 3.8+
•	Recommended: 16GB RAM
•	Disk space: ≥10GB
Install Dependencies
pip install -r requirements.txt

If you don’t have a requirements.txt, create one with:
pip freeze > requirements.txt
	Quick Start (Run the Full Pipeline)
python src/layer1_data_collection.py

	Quick Start (Run the Full Pipeline)
Step 1 — Data Collection
python src/layer1_data_collection.py
Step 2 — Data Processing
python src/layer2_data_processing.py
Step 3 — Statistical Analysis
python src/layer3_statistical_analysis.py
Step 4 — Governance & Modeling
python src/layer4_governance_modeling.py
Launch Dashboard
python src/dashboard.py
Dashboard will run at:
 http://127.0.0.1:8050/
________________________________________
 Output Files & Reports
Generated artifacts are automatically organized under:
•	outputs/plots/ → time-series and model diagnostics
•	outputs/csv/ → tabular results per region and model
•	outputs/json/ → structured model results
•	outputs/reports/ → detailed analytical reports
•	outputs/pdf/ → final PDF reports
•	governance/ → decision logs, anomaly reports, validation certificates
________________________________________
Dashboard Capabilities
The dashboard supports:
•	Region selection (single region / all regions)
•	Lag time adjustment (0–120 days)
•	 Policy simulation (vaccination change: −20% to +50%)
•	 Anomaly detection
•	Visualization of vaccination vs mortality relationships
________________________________________
Models Implemented
•	SARIMAX: univariate and multivariate time-series with exogenous regressors
•	VAR: multivariate time-series modeling and response dependencies
•	VECM: cointegration-based modeling for long-term relationships
________________________________________
Data Sources
This project uses public and licensed data sources such as:
•	COVID-19 repositories (e.g., Google, official datasets)
•	World Bank Open Data APIs
Note: Raw full datasets are not included in this repository due to size and reproducibility policy.
Only sample datasets or download scripts are provided.
________________________________________
Reproducibility Notes
To ensure reproducibility:
•	Each layer checks for required input files before execution
•	Outputs are versioned and stored with consistent naming
•	Governance logs maintain audit trails for decisions and anomalies
•	Detailed logs are stored under the logs/ folder

	Troubleshooting
Common Issues
1) File Not Found
•	Ensure layers are executed sequentially
•	Confirm paths match your local project directory
2) Memory Errors
•	Process in smaller chunks
•	Use a machine with more RAM
3) API Timeouts
•	Retry mechanism exists
•	Run during off-peak hours
4) Dashboard Not Loading
•	Verify previous layers completed successfully
•	Confirm dependencies installation
________________________________________
Citation (Recommended)
If you use this repository, please cite as:
@software{covid_analysis_system_2026,
  author       = {[Your Name]},
  title        = {Comprehensive COVID-19 Data Analysis System},
  year         = {2026},
  url          = {https://github.com/[yourusername]/covid-19-analysis-system},
  version      = {1.0.0}
}


License
This project is licensed under the MIT License.
See the LICENSE file for details.

Author
Mahnaz Nouri
Email:
Mahnaznouri1981@gmail.com   , 
Mahnaznoori@gmail.com

