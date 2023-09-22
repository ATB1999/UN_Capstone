# UN_Capstone
Capstone Project which develops a Conflict regression model at a sub-national scale in Africa for conflict prediction and explainability of underlying factors.

The main dataset from which everything is derived is Afrogrid, at the forefront of conflict research, which includes grids of 60x60 km information about sub-regions in Africa from multiple variables and studies of reference (Priogrid, SCAD...). You can find the latest version in the [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/LDI5TK). Above you can visualize many of the papers that my team used to inform our approach, as well as the final written report associated to the project.

After different approaches, it was seen that no further data cleaning was needed apart from the ones of missing values, as anomalies and outliers were limited and the models performance excelled when not a lot of manipulations were done to the data. Precisely, what we did was a conservative approach to maintain as much data as possible:

* We eliminated variables from 2003 onwards due to the vast amount of missing values.
* We created a low fidelity linear regression model, took the coefficients and cross-checked them against a pearson Correlation or multicollinearity matrix. All variables that were highly correlated and with low importance were thrown out.
* We then ran the models with a simple imputer within a Scikit-learn pipeline, fine-tuning the models hyperparameters with GridSearchCV.

The results enabled good national and granular predictions, as well as derived explanations of the conflict phenomenon backed up with such metrics.

Lastly, you can also visualize QGIS visualizations for Central African Republic for a month. I was not in charge of that part of the project, but it was illustrative enough to get to know how this geospatial software can help in issues like these.
