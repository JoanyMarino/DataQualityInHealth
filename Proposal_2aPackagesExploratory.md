## Proposal section 2a: Tentative List of Packages (exploratory)

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
  
* GUI-based: ExPanDaR includes exporting reports as R Markdown Notebooks, while explore generates HTML reports. Both packages include additional features for statistical inference, such as regression analysis and decision trees,

* dlookr stands out for incorporating two different types of reports with detailed information on DQ issues and exploratory data analysis, respectively, in the form of PDF or HTML files. In contrast, {summarytools} generates a brief, but concise HTML report, which can be triggered by a single command call. The latter applies also to {DataExplorer}, but this package produces a more comprehensive report than {summarytools} including a wider range of figures, such as for example correlation heat maps. Another package which includes a report is {SmartEDA}. The report of this package is similar to {DataExplorer}'s report, but includes pairwise scatter plots for all pairs of variables instead of a correlation heat map. Also, the data overview is more extensive compared to {DataExplorer}. A principal component analysis is included in the report produced by {DataExplorer

*  The packages {clickR}, {mStats}, {skimr}, {StatMeasures} and {xray} are examples for packages that mainly give a descriptive variable overview but do not include stand-alone reports. 

*  visdat follows a unique approach by providing mainly graphical output. While the package \texttt{inspectdf} also equips each of its functions with a matching plot, it differs from \texttt{visdat} in providing the output in a tabular format. Both packages are able to compare two data sets, but \texttt{inspectdf} offers more functionalities in this regard.
  
  
