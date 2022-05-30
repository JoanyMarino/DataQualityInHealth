---
name: DataQualityInHealth
maintainers: Joany Mariño, Elisa Kasbohm, Stephan Struckmann, Lorenz A. Kapsner, Carsten O. Schmidt
email: joany.marino@uni-greifswald.de, elisa.kasbohm@uni-greifswald.de, stephan.struckmann@uni-greifswald.de, Lorenz.Kapsner@uk-erlangen.de, carsten.schmidt@uni-greifswald.de
version: 2022-05-18
---

*DataQualityInHealth* contains packages that help assess data quality, focusing on phenotypic data from health and social science studies.

Data quality is the degree to which data fulfills defined requirements, and it is an issue in all scientific fields. Evaluating data quality is essential in initial data analysis and quality monitoring processes to ensure valid research results. Base R already contains general functionalities for assessing data quality in a broad sense, and depending on the application, users may employ several packages. Yet, users will commonly need extensive programming to create comprehensive reports, with code being typically highly tailored to a specific data set. Therefore, it is important to identify packages with particular functionalities to facilitate conducting data quality analyses. Using these packages may also improve the comparable reporting on data quality across studies. However, the applicability of any such package, together with suitable data quality approaches, will differ across research fields as determined by the data structures, its requirements, and the representation of the latter in the metadata. 
This task view documents packages for data quality assessment, specifically for phenotypic data with a focus on health and social science studies. Prototypical data examples are results from clinical measurements (e.g., blood pressure) or responses to surveys and questionnaires. Nevertheless, this focus does not preclude the suitability of the documented packages for use in other research fields.

The quality checks performed by the targeted packages include inspecting a range of data quality dimensions, such as integrity (the degree to which the data conforms to structural and technical requirements), completeness (the degree to which expected data values are present), consistency (the degree to which data values are free of breaks in conventions or contradictions), and accuracy (the degree of agreement between observed and expected distributions and associations). 
The packages are broadly divided according to their capabilities into three major groups: packages that explicitly focus on data quality assessments (these usually combine targeted data quality checks with descriptive or explorative features), packages that target data exploration and statistical analyses but provide data quality-related functions, and packages that perform focused data quality checks based on rule input. 
However, many have functionalities that span more than one category. We include packages, if they fall (at least) into one of the three categories mentioned above, are applicable to health data in various formats, and provide a sufficient number of data quality checks. For the latter, we compared packages in reference to a data quality framework for observational health research data ([Schmidt et al. 2021](https://doi.org/10.1186/s12874-021-01252-7)). As a threshold for inclusion, the packages need to address at least three data quality dimensions and four domains of the reference framework. Packages that do not run as expected or produce major errors when applied to evaluate a [publicly available data sets](https://dataquality.ship-med.uni-greifswald.de/ExampleDataDescription.html) are not included.

# Packages 

## Descriptive-explorative features together with targeted checks
     
These packages perform targeted data quality checks, but also provide descriptive or explorative features. These packages also generate data quality assessment reports that allow for rating data quality issues.  

-   `r pkg("pointblank", priority = "core")` is a general-purpose package for data quality assessments. Data quality checks are included via specific validation functions that the user can compile into an "agent". This enables to create customized reports for data quality. The package also provides a pre-defined report, which includes a data overview and some figures (e.g., pairwise plots of variables, correlation heat maps, and a visualization of missing values). 

-   `r pkg("dataReporter", priority = "core")` provides a pre-defined report including a data overview, some checks (e.g., for potential data type mismatches, miscoded missing values or outliers), and a summary for each variable. This package is the successor of `r pkg("dataMaid")`. 

-   `r pkg("dataquieR", priority = "core")` is designed to conduct data quality assessments in data collections for epidemiological research. 
     It makes strong use of metadata (e.g., collected in a spreadsheet) and checks the formal compliance of study data with expectations defined in the metadata. The concept of the package follows the data quality framework of [Schmidt et al. (2020)](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-021-01252-7). 
     For technical details see [Richter et al. (2021)](https://doi.org/10.21105/joss.03093).
  
-   `r pkg("DQAstats", priority = "core")` provides a data quality assessment for electronic health records. It integrates metadata and allows to compare two datasets by design. The package is aligned to the data quality framework described by [Kahn et al. (2016)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5051581/). Details on the implementation and connection with the metadata repository are described in [Kapsner et al. (2021)](https://www.thieme-connect.de/products/ejournals/abstract/10.1055/s-0041-1733847). The add-on package `r pkg("DQAgui")` enriches this package with a graphical user interface (GUI) based on [R shiny](https://cran.r-project.org/package=shiny).

-   `r pkg("MOQA")` focuses on single variables and provides separate functions and reports for numeric and categorical variables. The reports are created as separate PDF files for each variable, including an overview of the data elements and visualizations of their distribution. The package was motivated by the data quality guidelines of [Nonnemacher et al. (2014)](https://library.oapen.org/bitstream/handle/20.500.12657/39363/datenqualitat-in-der-medizinischen-forschung.pdf?sequence=1).

## Descriptive overviews and data exploration

These packages focus on data exploration and yield descriptive summaries and overviews of the data.

### Packages including reporting features

-  `r pkg("dlookr", priority = "core")` provides two different types of reports: one with detailed information on data quality issues (including missing values, outliers, cardinality, zeros and negative values) and one for exploratory data analysis (including a dataset overview, descriptive statistics with some data quality checks, normality tests and correlation analyses). 

-  `r pkg("DataExplorer")` produces a comprehensive report from a single function, including a dataset overview and a number of figures (for missing values, univariate distributions and correlations). The report also provides a principal component analysis.

-  `r pkg("SmartEDA")` produces a report similar to `r pkg("DataExplorer")`, but includes pairwise scatter plots for all pairs of variables and does not include a correlation heat map. The dataset overview is more extensive compared to `r pkg("DataExplorer")`.

-  `r pkg("summarytools")` generates a brief, but concise HTML report, which can be triggered by a single command call. 

### GUI-based 

-  `r pkg("ExPanDaR")` provides a Shiny application for data exploration and analysis, from which R Notebook code can be exported for documentation and reproducibility. The application includes various univariate and bivariate plots, descriptive statistics, correlation analysis and regression analyses. 

- `r pkg("explore")` also offers a Shiny application for data exploration (including a dataset overview, descriptive statistics, univariate and bivariate plots and decision trees) and can generate descriptive reports for the complete dataset or single variables. 

### Descriptive overview without stand-alone reports

-  `r pkg("clickR")` supplies descriptive statistics for each variable, grouped by data type. The package provides a function for quality checks on a variable, which includes missing values, empty entries, outliers, possible miscodings of numeric values as strings, and a matching visualization. It also includes functions for data cleaning, such as fixing factor level names.

-  `r pkg("mStats")` generates a dataset overview and descriptive statistics for each variable, also identifying duplicates in the dataset. For plots, the package includes a function for histograms and for pairwise variable plots. 

-  `r pkg("skimr")` provides a function that produces a dataset overview and descriptive statistics for each variable grouped by data type. There are various options for customization.

-  `r pkg("StatMeasures")` outputs a dataset overview and has functions to describe the data elements depending on their type. Duplicate observations and duplicated keys can be identified.  

-  `r pkg("xray")` gives a dataset overview with a focus on missing values, empty entries and specific values (such as 0, Inf), which are considered 'anomalous'. The package includes histograms and bar charts to visualize distributions.

-  `r pkg("funModeling")` provides a dataset overview, descriptive statistics and some data quality checks (missing values, specific values (such as 0, Inf), cardinality). The package also includes functions for data visualization, correlation analysis and data cleaning.

### Dataset visualization

-  `r pkg("visdat", priority = "core")` visualizes entire datasets highlighting missing values, (estimated or actual) data types, (dis-)agreements with global conditions, correlations, and differences between datasets of the same dimension. 

-  `r pkg("inspectdf", priority = "core")` equips each of its functions with a matching plot, but also provides the output in a tabular format. The package considers categorical and numerical variables, data types, missing values, correlations and memory usage. Each function can be applied to compare two datasets.

### Additional statistical support

-  `r pkg("DescTools")` is a large collection of functions for data description, data exploration and statistical analyses.

## Rule-based input to perform highly focused checks

These packages follow the idea of a rule-based checking, similar to software unit-testing-functions as in `r pkg(testthat)`. 

### Packages that allow integration in test-frameworks

These packages run a set of tests and summarise their results.

-   `r pkg("validate", priority = "core")` can also be used for traceable data curation with the add-on packages `r pkg("errorlocate")` and `r pkg("lumberjack")`. It also comprises notification management functions. It supports a simplified R-like syntax as well as [SDMX](https://sdmx.org/) REST-web service URLs for importing data quality rules.

-   `r pkg("testdat", priority = "core")` integrates well with `r pkg(testthat)`, because it comprises functions that can be used in a unit test to test data for integrity, completeness and consistency issues.

-   `r pkg("assertr")` supports a pipeline-alike coding style for writing tests. It addresses mostly integrity and consistency issues.

-   `r pkg("assertive")` provides a large number of test functions, among them checks for specific string patterns (email addresses, ISBN
                          codes, US zip codes, etc.).

-   `r pkg("assertable")` evaluates simple and flexible assertions on data.frame or data.table objects. It addresses mostly data integrity.

### Packages that check and report rule violations

-   `r pkg("IPDFileCheck")` checks for availability of data and validates individual data values based on variable specific rules, for example, if any value for a variable is in a list of admissible categories.

-   `r pkg("sanityTracker")` checks a rule set and reports the samples for that a rule fails. It can generate a summary data frame to report failed checks.


# Links

- [Data Quality Assessment](https://dataquality.ship-med.uni-greifswald.de/dqassess.html)
- [Medical Informatics Initiative](https://www.medizininformatik-initiative.de/index.php/de)
- [MIRACUM (Medical Informatics in Research and Care in University Medicine)](https://www.miracum.org/en/)

# References 

- Mariño J, Kasbohm E, Struckmann S, Kapsner LA, Schmidt CO. [R Packages for Data Quality Assessments and Data Monitoring: A Software Scoping Review with Recommendations for Future Developments](https://www.mdpi.com/2076-3417/12/9/4238). Applied Sciences. 2022 Jan;12(9):4238.
- Kapsner LA, Mang JM, Mate S, Seuchter SA, Vengadeswaran A, Bathelt F, Deppenwiese N, Kadioglu D, Kraska D, Prokosch HU. [Linking a Consortium-Wide Data Quality Assessment Tool with the MIRACUM Metadata Repository](https://www.thieme-connect.de/products/ejournals/abstract/10.1055/s-0041-1733847). Applied Clinical Informatics. 2021 Aug;12(04):826-35.
- Schmidt CO, Struckmann S, Enzenbach C, Reineke A, Stausberg J, Damerow S, Huebner M, Schmidt B, Sauerbrei W, Richter A. [Facilitating harmonized data quality assessments. A data quality framework for observational health research data collections with software implementations in R](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-021-01252-7). BMC Medical Research Methodology. 2021 Dec;21(1):1-5.
- Weiskopf NG, Bakken S, Hripcsak G, Weng C. [A data quality assessment guideline for electronic health record data reuse](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5983018/). Egems. 2017;5(1).
- Liaw ST, Guo JG, Ansari S, Jonnagaddala J, Godinho MA, Borelli Jr AJ, de Lusignan S, Capurro D, Liyanage H, Bhattal N, Bennett V. [Quality assessment of real-world data repositories across the data life cycle: A literature review](https://www.ncbi.nlm.nih.gov/pmc/articles/pmc8475229/). Journal of the American Medical Informatics Association. 2021 Jul;28(7):1591-9.
- Lee K, Weiskopf N, Pathak J. [A framework for data quality assessment in clinical research datasets](https://www.ncbi.nlm.nih.gov/pmc/articles/pmc5977591/). InAMIA Annual Symposium Proceedings 2017 (Vol. 2017, p. 1080). American Medical Informatics Association.
- Kahn MG, Callahan TJ, Barnard J, Bauck AE, Brown J, Davidson BN, Estiri H, Goerg C, Holve E, Johnson SG, Liaw ST. [A harmonized data quality assessment terminology and framework for the secondary use of electronic health record data](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5051581/). Egems. 2016;4(1).
- Nonnemacher M, Nasseh D, Stausberg J. [Datenqualität in der medizinischen Forschung: Leitlinie zum adaptiven Management von Datenqualität in Kohortenstudien und Registern](https://library.oapen.org/bitstream/handle/20.500.12657/39363/datenqualitat-in-der-medizinischen-forschung.pdf?sequence=1). MWV Medizinisch Wissenschaftliche Verlagsgesellschaft; 2014.


# Contributions

The packages listed in this task view are undergoing rapid development, and new ones are being continuously released.
To keep the list up-to-date, we welcome and acknowledge suggestions for additions or improvements. 
To do so, please send your comments in GitHub by
[submitting an issue](https://github.com/cran-task-views/DataQualityHealth/issues),
or make some edits and
[submit a pull request](https://github.com/cran-task-views/pulls).
If you can't contribute on GitHub, please send an email to the mantainers listed above. 
If you have an issue with one of the packages discussed below, please contact
the maintainer of that package. For further details see the
[Contributing](https://github.com/cran-task-views/ctv/blob/main/Contributing.md)
guide. All contributions must adhere to the
[code of conduct](https://github.com/cran-task-views/ctv/blob/main/CodeOfConduct.md).
