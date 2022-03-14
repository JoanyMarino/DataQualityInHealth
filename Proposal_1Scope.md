## Proposal section 1: Scope

**Requirement**: Include one or two paragraphs about the scope of the task view, outlining the inclusion and exclusion criteria
  as well as relevant sections within the topic.
  *A task view should be on a topic with a rather clear scope that should neither be too narrow nor too wide.*
  
*DataQualityInHealth* contains packages that help assessing the fitness for use / data quality 
of medical data. 

The Package list is divided in two major sections: Packages that address
R programmers, and packages that also address users with limited programming skills.
Also, there are sections related to sub-tasks of data quality assessments, i.e. to data integrity,
data completeness, data consistency and data accuracy (@schmidt2021).

The applicability of packages also depends on the structure of data and 
metadata. Because data quality is an issue in many different fields of science,
hence for a broad variety of data types and metadata formats, this task
view focuses data quality assessment tools specifically for medical data.  

Packages are listed, if they

  - explicitly refer to data quality
  - are applicable to data in wide format
  - address at least two data quality dimensions / XXX domains (@schmidt2021, 
    XXX_ maybe, we should list also the other large DQ frameworks, i.e. Kahn, 
    ...)
  - provide functions that run without errors on example data

**To do**: 

- [ ] Add inclusion and exclusion criteria.
- [ ] Explain the necessity of a narrow scope for this task view.
- [ ] Rewrite according to the structure of the list of packages.
