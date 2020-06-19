# Proposal for Creating a Markdown-compatible PDF template for the EPA ORD Report

md = Markdown
Rmd = RMarkdown

## Background

See the main [Background](README.md#Background) first.

Since generating the PDF is via LaTeX, the intermediate LaTeX file must contain the information to pass data from md or Rmd into the PDF. 

## Option 1 

Steps:
1. Following the recommendations to [Use a custom Pandoc LaTeX template from bookdown](https://bookdown.org/yihui/rmarkdown-cookbook/latex-template.html), start with the [default.latex](https://github.com/jgm/pandoc/blob/master/data/templates/default.latex) template used with pandoc.

2. We need to get EPA styles and formatting from LaTeX as well to add/modify the starter template. To do this, convert the current Word docx Report template to LaTeX (EPAreport.latex) with a tool like [Writer2LaTeX](http://writer2latex.sourceforge.net/)

3. Modify the default.latex with data from the converted EPAreport.latex on the styles and images.

4. Create the custom YAML metadata in a .yaml file, [described here](https://bookdown.org/yihui/rmarkdown-cookbook/latex-template.html).

5. Text writing out to PDF first using pandoc commands to write using the custom template, and iterate with changes to the template.









