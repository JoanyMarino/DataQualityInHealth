## Proposal section 2c: Tentative List of Packages (rules)

**Requirement**: Include a _tentative list_ of packages for the task view. This should encompass the "core" packages
  and a collection of relevant packages, ideally grouped by sections within the topic. It is not important, yet,
  that the list of sections or packages is already exhaustive.
   The goal is not to cover "every package" remotely related to the topic but rather the packages that clearly fall within the scope. The coverage should be similar to what an (introductory) text book on the topic would cover. Non-CRAN packages may also be included but the focus of CRAN task views should be packages on CRAN (as the name conveys).
   
**Ratings**: Task views should not rate the packages or endorse certain "best" packages but rather give an overview of what is available. A bit of emphasis to the more important packages can be given in two ways: (1) The most important packages can be flagged as "core" packages. (2) In the information text the more important packages can be listed first in the respective sections.
  
Please see [README.md](README.md) for a comprehensive list and preview of the Task View. Currently, it consists of XX packages (including YY core packages). 
  
*The following sections will be incorporated in the README.md linked above*

The packages in this view can be roughly structured into the following topics. 
If you think that some package is missing from the list, please file an issue in the GitHub repository or contact the maintainers.

### 2. Rule-based input to perform highly focused checks

These packages follow the idea of a rule-based checking, similar to software 
unit-testing-functions as in `r pkg(testthat)`. 

#### Possibility of integration in test-frameworks

These packages run a set of tests and summarise their results:

-   `r pkg("validate")` can also be used for traceable data curation with the add-on packages `r pkg("errorlocate")` and `r pkg("lumberjack")`. It also comprises notification management functions. It supports a simplified R-alike syntax as well as [SDMX](https://sdmx.org/) REST-web service URLs for importing data quality rules.

-   `r pkg("testdat")` integrates well with `r pkg(testthat)`, because it comprises functions that can be used in a unit test to test data for integrity, completeness and consistency issues.

-   `r pkg("assertr")` supports a pipeline-alike coding style for writing tests. It addresses mostly integrity and consistency issues.

-   `r pkg("assertive")`: provides a large number of check functions, among them checks for specific string patterns (email addresses, ISBN
                          codes, US zip codes, etc.).

-   `r pkg("assertable")` Simple, flexible, assertions on data.frame or data.table objects. It addresses mostly the data integrity.

#### Check and report rule violations

-   `r pkg("IPDFileCheck")` checks for availability of data and validates individual data values based on variable specific rules, e.g., if any value for a variable is in a list of admissible categories.

-   `r pkg("sanityTracker")` checks a rule set and reports the samples for that a rule fails. Can generate a summary data frame on failed checks.
