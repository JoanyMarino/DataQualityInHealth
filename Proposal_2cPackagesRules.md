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

These packages follows the idea of a rule-based
checking, similar to software unit-testing-functions. 

#### Check and report rule violations

-   `r pkg("dataReporter")` can report issues and descriptive overviews in different formats (R
Markdown, PDF, HTML and MS-Word). 

-   `r pkg("IPDFileCheck")`

-   `r pkg("sanityTracker")`


#### Possibility of integration in test-frameworks

These packages run a set of tests and summarise their results:

-   `r pkg("testthat")`

-   `r pkg("assertive")`: provides a large number of check functions,
among them checks for specific string patterns (email addresses, ISBN
codes, US zip codes, etc.). 

-   `r pkg("assertr")`

-   `r pkg("observer")`

-   `r pkg("validate")` implements the Hiridoglu-Berthelot function to be used to detect outliers with skewed
distributions ; with the add-on packages `r pkg("errorlocate")` and `r pkg("lumberjack")`, `r pkg("validate")` can also be used for traceable data curation.

The packages `r pkg("observer")` and `r pkg("validate")` even comprise notification management
functions.