Vignette on classifying household density categories using logistic regression and random forest models with California Household Travel Survey (CHTS) data; created as a class project for PSTAT 197A in Fall 2024.

# vignette-householdclassification

### Contributors

-   Rebecca Chang

-   Valerie De La Fuente

-   Mai Uyen Huynh

-   Tess Ivinjack

-   Shirley Wang

## Abstract

This vignette explores how logistic regression and random forest models can classify household density categories (urban, suburban, exurban, rural) using data from the 2010-2012 California Household Travel Survey (CHTS). The dataset includes variables such as household demographics, travel behaviors, vehicle ownership, parking preferences, work schedules, and active travel modes. By employing Principal Component Analysis (PCA), we reduce the dataset's high dimensionality, distilling numerous variables into a manageable set of key components that retain the most significant variance. Logistic regression, known for its interpretability, is then used to model the relationship between these principal components and household density categories, providing insights into how demographic and travel behavior variables influence classification. In contrast, random forest, an ensemble learning method, is employed to explore complex, non-linear relationships within the data, leveraging decision tree structures to enhance prediction accuracy. In our logistic regression model, we obtain a rather low accuracy of around 0.337, but in our random forest model, we obtain a higher accuracy of 0.462.

## Repository Contents

-   `Data` contains

    -   `processed` contains

        -   `personHHData_processed.Rds` - contains final data file used for our models
        -   `tune_results.rda` - contains random forest tuned model

    -   `raw` contains

        -   `counties` - a folder storing and managing spatial data in geographic information systems (GIS) for geospatial data processing

        -   `DataDictionary.xlsx` - a data file guide spreadsheet detailing each of the files listed below, with descriptions of each variable and the possible values they can take

        -   `hh_bgDensity.Rds` - contains cleaned block group density data that characterizes the urbanicity of areas surrounding the homes of CHTS respondents

        -   `HHData_111A.Rds` - contains cleaned household-level demographics, survey date, and home county information

        -   `PersonData_111A.Rds` - contains cleaned per-person data, including basic demographics, employment/student status, and travel behavior variables

-   `scripts` contains

    -   `drafts` - a folder with scripts of each member's progress throughout the project

    -   `vignette-script.R` - the final vignette script with line annotations

-   `imgs` contains

    -   `household-density.jpg`

-   `vignette.qmd` - the final vignette document

-   `vignette.html` - the final vignette document rendered in html format

## Reference List

-   Dataset Source/Information

    -   [California Department of Transportation Final Report](https://lede-admin.cal.streetsblog.org/wp-content/uploads/sites/52/2015/04/FinalReport.pdf)

    -   [InfrastructureUSA](https://infrastructureusa.org/california-household-travel-survey-2/)

    -   [Transportation Research Board](https://trid.trb.org/view/1308918)

    -   [DOE Data Explorer - U.S. Department of Energy Office of Scientific and Technical Information](https://www.osti.gov/dataexplorer/biblio/dataset/1924686)

-   Principal Component Analysis (PCA)

    -   [Principal Component Analysis](https://www.geeksforgeeks.org/principal-component-analysis-pca/)

-   Logistic Regression Model

    -   [ML from Scratch - Multinomial Logistic Regression](https://towardsdatascience.com/ml-from-scratch-multinomial-logistic-regression-6dda9cbacf9d)

-   Random Forest Model

    -   [Random Forest Algorithm in Machine Learning](https://www.geeksforgeeks.org/random-forest-algorithm-in-machine-learning/)
