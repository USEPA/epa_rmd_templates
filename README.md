# USEPA Report and Other Standard Templates for Markdown/RMarkdown

![USEPA](https://www.epa.gov/sites/production/files/2013-06/epa_seal_verysmall_trim.gif)

This is a project to provide standard templates for EPA reports and other Agency documents for use with various flavors of [Markdown](https://www.markdownguide.org/) and [RMarkdown](https://rmarkdown.rstudio.com/). 

Project Status: Conceptual

## Background

[Pandoc](https://pandoc.org/) is the common utility used either directly to convert from Markdown to other formats. Markdown and RMarkdown permit the specification of a template file that can be used to write out the Markdown content into upon conversion. Pandoc can write directly to some output formats like HTML and Word docx, but for [PDF writing](https://pandoc.org/MANUAL.html#creating-a-pdf), it writes to a LATeX file and calls on the locally-installed LaTeX engine to generate the PDF. 

In RMarkdown, the process of converting an RMarkdown document to another document form is called _knitting_ and [RStudio](https://rstudio.com/) embeds the [knitr](https://yihui.org/knitr/) package which can read R code along with RMarkdown as well as a YAML file specifying metadata to inform the conversion process. In this YAML a user can add a parameter that specifies the template for output writing.  
 
## Disclaimer

The United States Environmental Protection Agency (EPA) GitHub project code is provided on an "as is" basis
 and the user assumes responsibility for its use.  EPA has relinquished control of the information and no longer
  has responsibility to protect the integrity , confidentiality, or availability of the information.  Any
   reference to specific commercial products, processes, or services by service mark, trademark, manufacturer,
    or otherwise, does not constitute or imply their endorsement, recommendation or favoring by EPA.  The EPA seal
     and logo shall not be used in any manner to imply endorsement of any commercial product or activity by EPA or
      the United States Government.