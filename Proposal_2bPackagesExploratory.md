## Proposal section 2b: Tentative List of Packages (exploratory)

**Requirement**: Include a _tentative list_ of packages for the task view. This should encompass the "core" packages
  and a collection of relevant packages, ideally grouped by sections within the topic. It is not important, yet,
  that the list of sections or packages is already exhaustive.
   The goal is not to cover "every package" remotely related to the topic but rather the packages that clearly fall within the scope. The coverage should be similar to what an (introductory) text book on the topic would cover. Non-CRAN packages may also be included but the focus of CRAN task views should be packages on CRAN (as the name conveys).
   
**Ratings**: Task views should not rate the packages or endorse certain "best" packages but rather give an overview of what is available. A bit of emphasis to the more important packages can be given in two ways: (1) The most important packages can be flagged as "core" packages. (2) In the information text the more important packages can be listed first in the respective sections.
  
Please see [README.md](README.md) for a comprehensive list and preview of the Task View. Currently, it consists of XX packages (including YY core packages). 
  
*The following sections will be incorporated in the README.md linked above*

The packages in this view can be roughly structured into the following topics. 
If you think that some package is missing from the list, please file an issue in the GitHub repository or contact the maintainers.
  
### 1. Descriptive overviews and data exploration

#### Including reporting features

-  `r pkg("dlookr", priority = "core")` provides two different types of reports: one with detailed information on data quality issues (including missing values, outliers, cardinality, zeros and negative values) and one for exploratory data analysis (including a dataset overview, descriptive statistics with some data quality checks, normality tests and correlation analyses). 

-  `r pkg("DataExplorer")` produces a comprehensive report from a single function, including a dataset overview and a number of figures (for missing values, univariate distributions and correlations). The report also provides a principal component analysis.

-  `r pkg("SmartEDA")` produces a report similar to `r pkg("DataExplorer")`, but includes pairwise scatter plots for all pairs of variables and does not include a correlation heat map. The dataset overview is more extensive compared to `r pkg("DataExplorer")`.

-  `r pkg("summarytools")` generates a brief, but concise HTML report, which can be triggered by a single command call. 


#### GUI-based 

-  `r pkg("ExPanDaR")` provides a Shiny application for data exploration and analysis, from which R Notebook code can be exported for documentation and reproduction. The application includes various univariate and bivariate plots, descriptive statistics, correlation analysis and regression analyses. 

- `r pkg("explore")` provides a Shiny application for data exploration (including a dataset overview, descriptive statistics, univariate and bivariate plots and decision trees) and can generate descriptive reports for the complete dataset or single variables. 

#### Descriptive overview without stand-alone reports

-  `r pkg("clickR")` provides descriptive statistics for each variable, grouped by data type. The package provides a function for quality checks on a variable, which includes missing values, empty entries, outliers, possible miscodings of numeric values as strings, and a matching visualization. It also includes functions for data cleaning, such as fixing factor level names.

-  `r pkg("mStats")` provides a dataset overview and descriptive statistics for each variable. Duplicates in the dataset can be identified. For plots, the package includes a function for histograms and for pairwise variable plots. 

-  `r pkg("skimr")` provides, using a single command call, a dataset overview and descriptive statistics for each variable grouped by data type. There are various options for customization.

-  `r pkg("StatMeasures")` provides a dataset overview and functions for data description depending on the data type. Duplicate observations and duplicated keys can be identified.  

-  `r pkg("xray")` gives a dataset overview with focus on missing values, empty entries and specific values (0, Inf), which are considered 'anomalous'. The package includes histograms and bar charts to visualize distributions.

-  `r pkg("funModeling")` provides a dataset overview, descriptive statistics and some data quality checks (missing values, specific values (0, Inf), cardinality). The package also includes functions for data visualization, correlation analysis and data cleaning.

#### Dataset visualization

-  `r pkg("visdat", priority = "core")` visualizes entire datasets highlighting missing values, (estimated or actual) data types, (dis-)agreements with global conditions, correlations, and differences between datasets of the same dimension. 

-  `r pkg("inspectdf", priority = "core")` equips each of its functions with a matching plot, but also provides the output in a tabular format. The package considers categorical and numerical variables, data types, missing values, correlations and memory usage. Each function can be applied to compare two datasets.

#### Additional statistical support

-  `r pkg("DescTools")` is a large collection of functions for data description, data exploration and statistical analyses.

