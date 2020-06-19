# USEPA Report and Other Standard Templates for Markdown/RMarkdown

![USEPA](https://www.epa.gov/sites/production/files/2013-06/epa_seal_verysmall_trim.gif)

This is a project to provide standard templates for EPA reports and other Agency documents for use with various flavors of [Markdown](https://www.markdownguide.org/) and [RMarkdown](https://rmarkdown.rstudio.com/). 

Project Status: *Conceptual*

## Benefits

The benefits of this project for EPA will include:
1. *Increased transparency in the research publication process*. As markdown is often closely tied with core tools used EPA researchers like RStudio, the same tools in which data are imported, processed, and through which models are created and results generated can also be used to render reporting output directly. When this output is for a standard EPA publication like an EPA report, the tables and figures appearing in the report can be more directly traced to the underlying tools, model and data. 
 
2. *Ability to better leverage git and git platform management tools*. Since git keeps track of changes in text files and Markdown is a text-based format, git can be used for keeping a record of changes and contributions to a Markdown or RMarkdown file. More broadly, the platforms like github/bitbucket have addons like the issue trackers and pull request discussions that can be very useful for managing the development of EPA publications.

3. *More streamlined revision processes*.  When revisions are needed in tables and figures in reports, the underlying code can be updated and the report regenerated without the messy and non-transparent copy and paste process that such revisions typically require.

4. *Better support for annual/regular report generation*. For reports released on a regular cycle where the structure of the report remains consistent, the underyling models can be updated and results regenerated, and associated text description changed without having to redo the report formatting process.

5. *Less formatting for researchers and staff.* Researcher want to focus on core research tasks and not have a lot of their time occupied by formatting tasks. 

## Background

md = Markdown
Rmd = RMarkdown

### EPA Reports and Template
ORD provides a standard report format for [EPA Science Reports](http://intranet.ord.epa.gov/communications/reports-and-publications). 
. The full report template is currently limited to Word docx with front and back cover images available in Adobe InDesign format.

### Pandoc is universal
[Pandoc](https://pandoc.org/) is the common utility to convert from Markdown to other formats and is used either directly or as an intermediate utility in this conversion, as in the case of converting from RMarkdown. Markdown and RMarkdown permit the specification of a template file that can be used to write the Markdown content into upon conversion. Pandoc can write directly to some output formats like HTML and Word docx, but for [PDF writing](https://pandoc.org/MANUAL.html#creating-a-pdf), it writes to a LATeX file and calls on the locally-installed LaTeX engine to generate the PDF. 

### RStudio/R conversion
In RStudio, the process of converting an RMarkdown document to another document form is called _knitting_ and [RStudio](https://rstudio.com/) embeds the [knitr](https://yihui.org/knitr/) package which can read R code along with RMarkdown as well as a YAML file specifying metadata to inform the conversion process. In this YAML a user can add a parameter that specifies the template for output writing.  The [RMarkdown Cheatsheet](https://rmarkdown.rstudio.com/lesson-15.html) is useful for getting up to speed quickly on this process in RStudio.
 
## Disclaimer

The United States Environmental Protection Agency (EPA) GitHub project code is provided on an "as is" basis
 and the user assumes responsibility for its use.  EPA has relinquished control of the information and no longer
  has responsibility to protect the integrity , confidentiality, or availability of the information.  Any
   reference to specific commercial products, processes, or services by service mark, trademark, manufacturer,
    or otherwise, does not constitute or imply their endorsement, recommendation or favoring by EPA.  The EPA seal
     and logo shall not be used in any manner to imply endorsement of any commercial product or activity by EPA or
      the United States Government.