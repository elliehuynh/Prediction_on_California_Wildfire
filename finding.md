To address the research questions in readme.md, I used Jupyter notebooks for their convenience and clarity. Each notebook is described below:

Q1.ipynb:
This notebook connects to the SQLite database and extracts wildfire records specific to California.
It then visualizes the spatial distribution of wildfires—based on fire size—using a GIS map.

Q2-4.ipynb:
This notebook answers Questions 2 through 4. 
I used Seaborn for data visualization and conducted a basic climate trend analysis by comparing wildfire activity with climate indices such as the El Niño 3.4 Index and the North Pacific Oscillation Index. 
There appears to be a slight correlation between wildfire peaks and El Niño years (e.g., 1991–92, 1997–98, 2007–08, 2015–16), although the wildfire peaks tend to lag slightly behind the climate events.

Additionally, the notebook analyzes seasonal patterns by month and day of the year. The data clearly shows that wildfires are most frequent during the boreal summer, with activity beginning to rise in April and peaking between late June and early July (day 173–192). 
In terms of severity, Class A fires occur most frequently, while more severe classes (D, E, F, G) are less common and show no significant trends. Notably, Class B fires have declined since 2007, and Class A fires dropped between 2008 and 2010 before returning to around 4,000 occurrences per year after 2011. The analysis of fire causes also reveals that "Miscellaneous" and "Equipment Use" are the leading causes of wildfires.

Kettle_Q5-*.ipynb:
This section focuses on predictive modeling of wildfire frequency and severity on a monthly basis. Three models were evaluated:


Model	MAE	MSE	RMSE
MLP	26.4925	4093.7791	63.9826
RF	21.5793	2892.7273	53.7841
RF-AVE	22.1633	3135.1573	55.9925
MLP: Shallow neural network

RF: Random Forest

RF-AVE: Random Forest with spatial pattern averaging

The predictive plots can be found in the respective notebooks. Note that annual predictions can be derived by summing the model outputs across months.
