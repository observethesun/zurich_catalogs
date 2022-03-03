# zurich_catalogs

This repository contains digitized coordinates of sunspots, faculae and promenences from the catalogs of the Zurich Observatory in late 19th and early 20th centuries.

### Data source

References to the original catalogs:

| Years   |      Reference  |
|----------|----------|
|1887—1892 | https://doi.org/10.7891/e-manuscripta-48586 |
|1893—1898 | https://doi.org/10.7891/e-manuscripta-48585 |
|1899—1902 | https://doi.org/10.7891/e-manuscripta-48587 |
|1903—1905 | https://doi.org/10.7891/e-manuscripta-48583 |
|1906—1910 | https://doi.org/10.7891/e-manuscripta-48850 |
|1911—1915 | https://doi.org/10.7891/e-manuscripta-48849 |
|1916—1920 | https://doi.org/10.7891/e-manuscripta-48848 |

### Description of the digitization process

Numerical coordinates were recognized using the neural network model. More details on the process are in the paper [Reconstruction of the solar activity from the catalogs of the Zurich observatory]().

### Data description

Digitized coordinates are given in ```.csv``` files with the following format:

| Column name   |      Description      |  Data type |
|----------|----------|------|
| Date |  Date yyyy-mm-dd of the observation | str |
| Object |  Type of the object (sunspot, facula, prominence) | str |
| Column_1 |  Coordinate β | float |
| Column_2 |  Coordinate λ' | float |
| Column_3 |  Coordinate λ+k | float |
| Column_4 |  Coordinate b | float |
| Column_5 |  Coordinate l | float |
| Column_6 |  Coordinate L | float |
| Confidence_1 |  Confidence for Column_1 | float |
| Confidence_2 |  Confidence for Column_2 | float |
| Confidence_3 |  Confidence for Column_3 | float |
| Confidence_4 |  Confidence for Column_4 | float |
| Confidence_5 |  Confidence for Column_5 | float |
| Confidence_6 |  Confidence for Column_6 | float |
| Regression_2 |  True if the value in the Column_2 was computed based on the value in the Column_3 | bool |
| Regression_3 |  True if the value in the Column_3 was computed based on the value in the Column_2 | bool |
| Regression_5 |  True if the value in the Column_5 was computed based on the value in the Column_6 | bool |
| Regression_6 |  True if the value in the Column_6 was computed based on the value in the Column_5 | bool |
| Source |  Catalog name and page number | str |
| Row |  Row number of the observation (starts from 1) | int |
| Empty |  True if the row is empty | bool |

### Notes on data usage

The automatic digitization process was optimized to reduce the number of incorrect results as much as possible. Estimated errors rate for values with unit confidence is below 1%. Low confidence values indicate cases where the results might require verification.

We welcome contributions via Issues and Pull-Requests to this repository with errors corrections.

For visual estimation of the digitization results we provide ```.pdf``` files with page-by-page comparison of original and digitized tables in [Dropbox](https://www.dropbox.com/scl/fo/4bp33o3hwui5oudogjk2e/h?dl=0&rlkey=kqcxesk63ui6vjjzk3jqxa8e1).

### Citing this work
```
E. Illarionov, R. Arlt. Reconstruction of the solar activity from the catalogs of the Zurich observatory. 2022.
```
