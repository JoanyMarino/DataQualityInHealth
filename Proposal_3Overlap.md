## Proposal section 3: Overlap

**Requirement**: Comment on potential overlap with already existing task views as well as with task views that might be
  created (or split off) in the future.

Data quality assessment and monitoring are included in other task views only to a lesser extent. Quality evaluation during general data processing is addressed in the r view("OfficialStatistics") task view, but mainly covers a few rule-based packages. The r view("MissingData") task view reviews data completeness and imputation in detail. Some other views list other specific data quality applications, for example, hydrological data in the r view("Hydrology") task view. Potential overlap with a focus on health-related data would be the r view("ClinicalTrials") task view. Nevertheless, r view("ClinicalTrials")' data monitoring and analysis sections do not yet include quality assessment. 

**To do**: 

- [ ] How do we minimize overlap? - I think we explain this in the scope section
- [x] Why does the existing overlap does not imply redundancy?
- [x] Check if any of our packages is already included in another task view? - Only in OfficialStatistics and MissingData
