
## Instructions

* _Submission:_ [Open an issue](https://github.com/cran-task-views/ctv/issues) in the `ctv` repository with the title
   _CRAN task view proposal: MyTopic_ where _MyTopic_ should be replaced with the intended name of the task view in
   _CamelCase_.
* _Scope:_ Include one or two paragraphs about the scope of the task view, outlining the inclusion and exclusion criteria
  as well as relevant sections within the topic.
* _Packages:_ Include a _tentative list_ of packages for the task view. This should encompass the "core" packages
  and a collection of relevant packages, ideally grouped by sections within the topic. It is not important, yet,
  that the list of sections or packages is already exhaustive.
* _Overlap:_ Comment on potential overlap with already existing task views as well as with task views that might be
  created (or split off) in the future.
* _Maintainers:_ The proposal should be made by the person willing to act as the principal maintainer for the task view.
  Furthermore, task views should have teams of additional 1-5 co-maintainers and possible candidates for these can be listed
  as well in the proposal.
  
  ## Proposal
*_Issue title_: CRAN task view proposal: DataQualityHealth

* _Scope:_ Include one or two paragraphs about the scope of the task view, outlining the inclusion and exclusion criteria
  as well as relevant sections within the topic.
  
* _Tentative List of Packages:_ The packages in this view can be roughly structured into the following topics. If you think that some package is missing from the list, please file an issue in the GitHub repository or contact the maintainer.
  
### Descriptive overviews and data exploration
  
* GUI-based: ExPanDaR includes exporting reports as R Markdown Notebooks, while explore generates HTML reports. Both packages include additional features for statistical inference, such as regression analysis and decision trees,

* dlookr stands out for incorporating two different types of reports with detailed information on DQ issues and exploratory data analysis, respectively, in the form of PDF or HTML files. In contrast, {summarytools} generates a brief, but concise HTML report, which can be triggered by a single command call. The latter applies also to {DataExplorer}, but this package produces a more comprehensive report than {summarytools} including a wider range of figures, such as for example correlation heat maps. Another package which includes a report is {SmartEDA}. The report of this package is similar to {DataExplorer}'s report, but includes pairwise scatter plots for all pairs of variables instead of a correlation heat map. Also, the data overview is more extensive compared to {DataExplorer}. A principal component analysis is included in the report produced by {DataExplorer

*  The packages {clickR}, {mStats}, {skimr}, {StatMeasures} and {xray} are examples for packages that mainly give a descriptive variable overview but do not include stand-alone reports. 

*  visdat follows a unique approach by providing mainly graphical output. While the package \texttt{inspectdf} also equips each of its functions with a matching plot, it differs from \texttt{visdat} in providing the output in a tabular format. Both packages are able to compare two data sets, but \texttt{inspectdf} offers more functionalities in this regard.
  
### Rule-based input to perform highly focused checks
  
### Descriptive features with the possibility of performing targeted checks
  
* _Overlap:_ Comment on potential overlap with already existing task views as well as with task views that might be
  created (or split off) in the future.
  
* _Maintainers:_ The proposal should be made by the person willing to act as the principal maintainer for the task view.
  Furthermore, task views should have teams of additional 1-5 co-maintainers and possible candidates for these can be listed
  as well in the proposal.
