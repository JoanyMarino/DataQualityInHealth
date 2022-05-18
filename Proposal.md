# Scope

*DataQualityInHealth* contains packages that help assess the quality of observational health research data. 

Data quality informs about the degree to which data fulfils defined requirements. Evaluating data quality is essential in initial data analysis and monitoring processes,
ensuring valid research results and consistent assessments in long-term studies. Assessing data quality is an issue across many scientific fields, including various data 
types and metadata formats. Base R already contains general functionality to evaluate data quality broadly, but the structure of the data and metadata will determine the 
applicability of more specialized packages. Hence, data quality analysis may be spread across packages depending on the application. 
This task view documents packages for data quality assessment specifically for health-related data from a methodological perspective. The quality checks
performed by these packages include inspecting the data's integrity, completeness, consistency, and accuracy. 

The packages are broadly divided according to their capabilities into three major groups: packages that explicitly focus on data quality assessments (these usually 
combine targeted data quality checks with descriptive or explorative features), packages that target data exploration and statistical analyses but provide data quality-related functions, and packages that perform focused data quality checks based on rule input. 
However, many have functionalities that span more than one category. We include packages, if they fall (at least) into one of the three categories mentioned above, are 
applicable to health data in various formats, and provide a sufficient number of data quality checks. For the latter, we compared packages in reference to a data quality 
framework for observational health research data 
[(Schmidt et al. 2021)](https://doi.org/10.1186/s12874-021-01252-7). As a threshold for inclusion, the packages need to address at least three data quality dimensions and
four domains of the reference framework. Packages that do not run as expected or produce major errors when applied to evaluate 
[publicly available data sets](https://dataquality.ship-med.uni-greifswald.de/ExampleDataDescription.html) are not included.

# Packages 

Please see https://github.com/JoanyMarino/DataQualityInHealth for the list of packages and preview of the Task View. 
Currently, it consists of 27 packages (including Y core packages).  
  
# Overlap 

Data quality assessment and monitoring are included in other task views only to a lesser extent. Some views list specific applications, for example, hydrological data quality in the [Hydrology](https://CRAN.R-project.org/view=Hydrology) task view. The [MissingData](https://CRAN.R-project.org/view=MissingData) task view reviews data completeness and imputation in detail, which we consider a part of a data quality assessment. Similarly, quality inspection during general data processing is addressed in the [OfficialStatistics](https://CRAN.R-project.org/view=OfficialStatistics) task view but limited to assertion checking packages. We aim to minimize overlap with these broad task views by concentrating on observational health data. A potential overlap with a focus on medical data would be the [ClinicalTrials](https://CRAN.R-project.org/view=ClinicalTrials); however, clinical trials data is a narrow type of observational health data. Moreover, [ClinicalTrials](https://CRAN.R-project.org/view=ClinicalTrials) places a greater emphasis on the design and analysis of clinical trial data, while the packages that we include in DataQualityInHealth are meant to be used at a different point in the research pipeline. 
  
# Maintainers 

The primary co-maintainers are Elisa Kasbohm (@ekasb) and Joany Mariño (@JoanyMarino). Co-maintainers include: Stephan Struckmann (@struckma) and Lorenz Kapsner (@kapsner).
