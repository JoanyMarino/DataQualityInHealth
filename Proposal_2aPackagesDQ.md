## Proposal section 2a: Tentative List of Packages (DQ)

**Requirement**: Include a _tentative list_ of packages for the task view. This should encompass the "core" packages
  and a collection of relevant packages, ideally grouped by sections within the topic. It is not important, yet,
  that the list of sections or packages is already exhaustive.
   The goal is not to cover "every package" remotely related to the topic but rather the packages that clearly fall within the scope. The coverage should be similar to what an (introductory) text book on the topic would cover. Non-CRAN packages may also be included but the focus of CRAN task views should be packages on CRAN (as the name conveys).
   
**Ratings**: Task views should not rate the packages or endorse certain "best" packages but rather give an overview of what is available. A bit of emphasis to the more important packages can be given in two ways: (1) The most important packages can be flagged as "core" packages. (2) In the information text the more important packages can be listed first in the respective sections.
  
Please see [README.md](README.md) for a comprehensive list and preview of the Task View. Currently, it consists of XX packages (including YY core packages). 
  
*The following sections will be incorporated in the README.md linked above*

The packages in this view can be roughly structured into the following topics. 
If you think that some package is missing from the list, please file an issue in the GitHub repository or contact the maintainers.

### 1. Descriptive-explorative features with the possibility of performing targeted checks
     
We include here R packages that perform targeted data quality checks, but also provide descriptive or explorative features. These packages also generate report documents of the data quality assessment that allow for rating data quality issues.  

#### Core packages

-   `r pkg("pointblank", priority = "core")` is a general-purpose package for data quality assessments. Data quality checks are included via specific validation functions that the user compiles into an "agent". This enables to create customized reports for data quality. The package also provides a pre-set report, which includes a data overview and some figures (pairwise plots of variables, correlation heat map, and a visualization of missing values). 
-   `r pkg("dataReporter", priority = "core")` provides a pre-set report including a data overview, some checks (for example checks for potential data type mismatches, miscoded missing values or outliers), and a summary for each variable. This package is the successor of `r pkg("dataMaid")`. 
-   `r pkg("dataquieR", priority = "core")` is designed to conduct data quality assessments in data collections for epidemiological research. 
     It makes strong use of metadata (e.g. collected in spreadsheets) and checks the formal compliance of study data with expectations defined in the metadata. The concept of the package follows the data quality framework of Schmidt et al. (2020). 
     For technical details see Richter et al. (2021).
-   `r pkg("DQAstats", priority = "core")` provides a data quality assessment for electronic health records. It integrates metadata and allows to compare two datasets by design. The data quality framework for which this package was developed is described in Kapsner et al. (2019). The add-on package `r pkg("DQAgui")` enriches this package with a GUI.



#### Other relevant packages

-   `r pkg("MOQA")` focuses on single variables and provides separate functions and reports for numeric and categorical variables. The reports are created as separate PDF files for each variable including an overview of the data elements and visualizations of their distribution. The package was motivated by the data quality guidelines by Nonnemacher et al. (2014).