## Proposal section 1: Scope

**Requirement**: Include one or two paragraphs about the scope of the task view, outlining the inclusion and exclusion criteria as well as relevant sections within the topic. *A task view should be on a topic with a rather clear scope that should neither be too narrow nor too wide.*

*DataQualityInHealth* contains packages that help assessing the data quality of health data. These quality checks inspect the integrity, completeness, consistency and accuracy of the data, which is an essential step within initial data analysis to ensure valid results. They can also be part of a monitoring process, e.g., to ensure consistent assessments in a long-term cohort study.

The package list is divided in three major sections:

-   Packages that explicitly focus on data quality assessments and combine targeted data quality checks with descriptive or explorative features,
-   packages that focus on data exploration and statistical analyses, but provide data quality-related functions, and
-   packages that perform focused data quality checks based on an input of rules.

The applicability of packages also depends on the structure of data and metadata. Because data quality is an issue in many different fields of science, hence for a broad variety of data types and metadata formats, this task view focuses data quality assessment tools specifically for health data.

We include packages, if they 

 - fall into one of the three categories mentioned above, 
 - are applicable to health data in various formats, 
 - provide a sufficient number of data quality checks.

For the latter, we compared packages in reference to a data quality framework for observational health research data (@schmidt2021). As a threshold for inclusion, the packages need to address at least three data quality dimensions and four domains of the reference framework.

Packages are excluded, if they don't run as expected or produce major errors on two example data sets from https://dataquality.ship-med.uni-greifswald.de/ExampleDataDescription.html.

**To do**:

-   [x] Add inclusion and exclusion criteria.
-   [x] Explain the necessity of a narrow scope for this task view.
-   [x] Rewrite according to the structure of the list of packages.
