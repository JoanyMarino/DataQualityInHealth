## Proposal section 2c: Tentative List of Packages (DQ)

**Requirement**: Include a _tentative list_ of packages for the task view. This should encompass the "core" packages
  and a collection of relevant packages, ideally grouped by sections within the topic. It is not important, yet,
  that the list of sections or packages is already exhaustive.
   The goal is not to cover "every package" remotely related to the topic but rather the packages that clearly fall within the scope. The coverage should be similar to what an (introductory) text book on the topic would cover. Non-CRAN packages may also be included but the focus of CRAN task views should be packages on CRAN (as the name conveys).
   
**Ratings**: Task views should not rate the packages or endorse certain "best" packages but rather give an overview of what is available. A bit of emphasis to the more important packages can be given in two ways: (1) The most important packages can be flagged as "core" packages. (2) In the information text the more important packages can be listed first in the respective sections.
  
Please see [README.md](README.md) for a comprehensive list and preview of the Task View. Currently, it consists of XX packages (including YY core packages). 
  
*The following sections will be incorporated in the README.md linked above*

The packages in this view can be roughly structured into the following topics. 
If you think that some package is missing from the list, please file an issue in the GitHub repository or contact the maintainers.

### 3. Descriptive features with the possibility of performing targeted checks
     
This section includes R packages that combine a wide range of
descriptive features as well as the possibility to perform targeted
checks. They focus on DQA and can be applied also by users with limited
programming knowledge. These packages also generate report documents
that allow for rating DQ issues. 

#### Core packages

-   `r pkg("dataquieR", priority = "core")` is designed to conduct data quality assessments in data collections for research. 
     It makes strong use of metadata (e.g. collected in spreadsheets) and checks the formal compliance of study data with expectations defined in the metadata. 
     The data quality assessments cover the dimensions completeness, consistency, and accuracy, as proposed by the framework of Schmidt et al. (2020). 
     For technical details see Richter et al. (2021).
     
-   `r pkg("DQAstats", priority = "core")`

-   `r pkg("pointblank", priority = "core")`


#### Other relevant packages

-   `r pkg("DescTools")` generates descriptive reports, but also
provides functions with statistical tests for specific accuracy issues.
Despite its broad scope, the automatic reports are descriptive only, and
DQ specific applications require programming R code.

-   `r pkg("MOQA")` produces reports with a separate PDF file for
for each variable, which may result in many files when
analysing large data sets. For `r pkg("MOQA")`, only one general threshold for
numerical variables can be used to define missing codes, i.e. all values
in any variable above that threshold are treated as missing values in
the same way while the package completely ignores NA values. If
inadmissible categorical values exist in the data, `r pkg("MOQA")` crashes with
an R error message, and cannot handle datetime variables.