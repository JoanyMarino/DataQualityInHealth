## Proposal section 1: Scope

**Requirement**: Include one or two paragraphs about the scope of the task view, outlining the inclusion and exclusion criteria as well as relevant sections within the topic. *A task view should be on a topic with a rather clear scope that should neither be too narrow nor too wide.*

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
