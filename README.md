Leading Causes of Death in the United States (1999–2017)

An exploratory data analysis of the ten leading causes of death in the U.S. over nearly two decades, using CDC mortality data. The goal was to turn a large public-health dataset into clear, interactive visuals that make national and state-level trends easy to read.


What the project does

Cleans and prepares a CDC dataset of the 10 leading causes of death (1999–2017, national and state level).
Runs exploratory data analysis to compare causes and trace patterns over time.
Builds choropleth, density, and bubble maps for state-level comparisons.
Produces interactive charts (scatter, box, and a data table) to explore mortality by state, year, and cause.

Dataset
Source: National Center for Health Statistics (NCHS), CDC data portal.
Name: Leading Causes of Death in the United States, 1999–2017.
Shape: 10,867 rows × 6 columns (annual death counts and age-adjusted death rates).

Link: https://www.cdc.gov/nchs/data-visualization/mortality-leading-causes/index.htm


Key takeaways

Heart disease and cancer are the two deadliest causes by a wide margin. By age-adjusted death rate, heart disease ranks highest (median around 195), with cancer close behind (around 175). Every other cause sits far lower, with median rates under roughly 55.

Mortality is concentrated in those top two causes. The gap between heart disease/cancer and the rest (stroke, diabetes, suicide, kidney disease, and others) is large and consistent.

Deaths are unevenly spread across states. In the 2017 choropleth, most states fall at the low end while a handful stand out much higher, largely reflecting population differences.

The raw data needed real cleaning. About 6,991 of the 10,867 rows were missing death counts. I handled the missing values and filtered to a complete 3,876-row subset for the deaths-based analysis.


Tools

Python · Pandas · NumPy · Matplotlib · Seaborn · Plotly · Dash · Folium · GeoPandas · Jupyter Notebook

How to run
bash
# 1. clone the repo
git clone https://github.com/Ceciliakamau/LEADING-CAUSES-OF-DEATH.git
cd LEADING-CAUSES-OF-DEATH

# 2. (optional) create a virtual environment
python3 -m venv venv
source venv/bin/activate        # on Windows: venv\Scripts\activate

# 3. install the libraries
pip install pandas numpy matplotlib seaborn plotly dash folium geopandas jupyter

# 4. open the notebook
jupyter notebook

Download the dataset from the CDC link above and place the CSV in the project folder, then run the notebook cells top to bottom.

Repository contents
analysis.ipynb — the full analysis and visualizations.
README.md — this file.
