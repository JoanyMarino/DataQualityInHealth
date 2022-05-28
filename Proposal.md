# Scope

*DataQualityInHealth* contains packages that help to assess the quality of data with a focus on phenotypic data from health and social science studies 

Data quality is the degree to which data fulfils defined requirements. It is an issue in all scientific fields. Evaluating data quality is essential in initial data analysis and quality monitoring processes in order to ensure valid research results. Base R already contains general functionalities to evaluate data quality broadly. Hence, data quality analysis may utilize several different R packages depending on the application. Yet, extensive programming will commonly be needed to create comprehensive reports and any code is typically highly tailored to some specific data set. Therefore it is important to identify packages with specific functionalities to facilitate the conduct of data quality analyses. This may also improve the comparable reporting on data quality across studies. As typical data structures and requirements and the representation of the latter in metadata determine the applicability of any such package, suitable approaches will differ across fields of science.  

This task view documents packages for data quality assessment specifically for phenotypic data with a focus on health and social science studies. Prototypcial data examples are results from clinical measurements (e.g. blood pressure) or responses to surveys and questionnaires. This focus does not preclude the suitability of the documented packages for use in other fields of research.

Quality checks performed by the targeted packages include inspecting a range of data quality dimensions such as integrity (The degree to which the data conforms to structural and technical requirements.), completeness (The degree to which expected data values are present.), consistency (The degree to which data values are free of breaks in conventions or contradictions.), and accuracy (The degree of agreement between observed and expected distributions and associations.). 

The packages are broadly divided according to their capabilities into three major groups: packages that explicitly focus on data quality assessments (these usually 
combine targeted data quality checks with descriptive or explorative features), packages that target data exploration and statistical analyses but provide data quality-related functions, and packages that perform focused data quality checks based on an input of rules and requirements. Many have functionalities that span more than one category. We include packages, if they fall (at least) into one of the three categories mentioned above, are applicable to spreadsheet type data as commonly used in phenotypic data collected in the health data in various formats, and provide a sufficient number of data quality checks. For the latter, we compared packages in reference to a data quality framework for observational health research data 
([Schmidt et al. 2021](https://doi.org/10.1186/s12874-021-01252-7)). As a threshold for inclusion, the packages need to address at least three data quality dimensions and four domains of the reference framework. Packages that do not run as expected or produce major errors when applied to evaluate 
[publicly available data sets](https://dataquality.ship-med.uni-greifswald.de/ExampleDataDescription.html) are not included.

# Packages 

Please see [this document](DataQualityInHealth.md) for the list of packages and a preview of the Task View. 
Currently, it consists of 27 packages (including 9 core packages).  
  
# Overlap 

Data quality assessment and monitoring are included in other task views only to a smaller extent. Some views list specific applications, for example, hydrological data quality in the [Hydrology](https://CRAN.R-project.org/view=Hydrology) task view. The [MissingData](https://CRAN.R-project.org/view=MissingData) task view reviews data completeness and imputation in detail, which we consider as part of a data quality assessment. Similarly, quality inspection during general data processing is addressed in the [OfficialStatistics](https://CRAN.R-project.org/view=OfficialStatistics) task view but limited to assertion checking packages. We aim to minimize overlap with these broad task views by concentrating on observational health data. A potential overlap with a focus on medical data would be the [ClinicalTrials](https://CRAN.R-project.org/view=ClinicalTrials); however, [ClinicalTrials](https://CRAN.R-project.org/view=ClinicalTrials) places a greater emphasis on the design and analysis of clinical trial data, while the packages that are included in DataQualityInHealth are meant to be used at a different point in the research pipeline, namely, during ongoing data collections or when the data becomes available before the start of substantive statistical analyses. 
  
# Maintainers 

The primary co-maintainers are Elisa Kasbohm (@ekasb) and Joany Mariño (@JoanyMarino). Co-maintainers include: Stephan Struckmann (@struckma), Lorenz A. Kapsner (@kapsner), and Carsten O. Schmidt (@c3schmidt).
