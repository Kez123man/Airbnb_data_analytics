# Airbnb Data Analytics
A complete, reproducible analytics project exploring Airbnb listings, pricing, and demand — built to demonstrate data analysis, modeling, and product thinking for employers.


TL;DR
- Cleaned, explored, and modeled Airbnb listings to derive actionable pricing and optimisation recommendations.
- End-to-end: data ingestion → cleaning → feature engineering → visualisations.
- Focus on reproducibility (notebooks + scripts), code quality, and communication-ready visualisations for stakeholders.

Table of Contents
- Project overview
- Tech stack
- Repository structure
- Quickstart (reproduce locally)
- Core analyses & notebooks
- Modeling & evaluation
- Deployment & demo
- How employers can validate your work
- Contributing and contact
- License

Project overview
This repository demonstrates a professional approach to data analytics and data science on Airbnb-style listing data. The goal is to answer business questions such as:
- What drives price and occupancy?
- Which listing attributes provide the best ROI for hosts?
- Which cities have the most properities and why?

The project emphasises:
- Clean, well-documented notebooks and modular scripts
- Clear visualisations

Key highlights (what to emphasize to employers)
- End-to-end reproducibility: environment specification, data preprocessing scripts, and notebooks that re-run from raw data to results.
- Feature engineering: text features (amenities), geospatial features (neighbourhood), and engineered terms..
- Communication: visualisations such as scatterplots, bar charts and heatmaps.

Tech stack
- Language: Python (pandas)
- Visualization: matplotlib,seaborn
- Notebooks: Jupyter / JupyterLab
- Reproducibility: pip/conda

Quickstart — reproduce in 5 minutes
1. Clone the repo
   git clone https://github.com/<your-username>/Airbnb_data_analytics.git
   cd Airbnb_data_analytics

2. Create environment and install
   python -m venv .venv
   source .venv/bin/activate   # use `.venv\Scripts\activate` on Windows
   pip install -r requirements.txt

   (Alternatively, use conda or the provided Dockerfile for exact reproducibility.)

3. Prepare data (example)
   Place raw CSV(s) into data/raw/ (see data/README for expected filenames), then:
   python src/data/prepare_data.py --input data/raw/listings.csv --output data/processed/listings.parquet

4. Run notebooks (optional)
   jupyter lab
   Open notebooks/01-data-exploration.ipynb and run top-to-bottom.

5. Train model (quick)
   python src/models/train.py --config configs/train_config.yaml

6. Launch demo dashboard (if included)
   streamlit run src/dashboard/app.py


License
MIT License — see LICENSE for details.

Appendix: 
Evaluation:
-More detailed visualisations
-Create some machine learning models
-Annotate notebook and create an executive summary
- Add unit tests for ETL functions and CI to run notebooks or smoke tests on builds.
- Include a small sample dataset and a fast path for reviewers to reproduce results in <5 minutes.
