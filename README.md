<!-- badges: start -->
[![DOI](https://zenodo.org/badge/306182457.svg)](https://zenodo.org/badge/latestdoi/306182457)
[![.github/workflows/basic_checks.yaml](https://github.com/mblue9/RNAseq-R-tidyverse/workflows/.github/workflows/basic_checks.yaml/badge.svg)](https://github.com/mblue9/RNAseq-R-tidyverse/actions) [![Docker](https://github.com/Bioconductor/BioC2020/raw/master/docs/images/docker_icon.png)](https://hub.docker.com/repository/docker/mblue9/RNAseq-R-tidyverse) 	
<!-- badges: end -->

# RNAseq-R-tidyverse 
<p float="left">
<img height="100" alt="tidybulk" src="https://github.com/Bioconductor/BiocStickers/blob/master/tidybulk/tidybulk.png?raw=true"/>
</p>

## Author names and contact information

* Maria Doyle <Maria.Doyle at petermac.org>  
* Stefano Mangiola <mangiola.s at wehi.edu.au>

## Syllabus

Material [web page](https://mblue9.github.io/RNAseq-R-tidyverse/articles/tidytranscriptomics.html).

## Package installation 

This is necessary in order to reproduce the code shown in the training material. The material is designed for R `4.0` and can be installed using one of the two ways below.

### Via Docker image

If you're familiar with [Docker](https://docs.docker.com/get-docker/) you could use the Docker image which has all the software pre-configured to the correct versions.

```
docker run -e PASSWORD=abc -p 8787:8787 mblue9/RNAseq-R-tidyverse:latest
```

Once running, navigate to <http://localhost:8787/> and then login with
`Username:rstudio` and `Password:abc`.

You should see the Rmarkdown file with the training material code which you can run.

### Via GitHub

Alternatively, you could install the training material using the commands below in R `4.0`.

```
# Install training material package
remotes::install_github("mblue9/RNAseq-R-tidyverse", build_vignettes = TRUE)

# To view vignettes
library(RNAseqRtidyverse)
vignette("RNAseqRtidyverse")
```

To run the code, you could then copy and paste the code from the workshop vignette or [R markdown file](https://raw.githubusercontent.com/stemangiola/ABACBS2020_tidytranscriptomics/master/vignettes/tidytranscriptomics.Rmd) into a new R Markdown file on your computer.

## Material Description

This training material presents how to perform analysis of RNA sequencing data following the tidy data paradigm. The tidy data paradigm provides a standard way to organise data values within a dataset, where each variable is a column, each observation is a row, and data is manipulated using an easy-to-understand vocabulary. Most importantly, the data structure remains consistent across manipulation and analysis functions.

This can be achieved for RNA sequencing data with the [tidybulk](https://stemangiola.github.io/tidybulk/),   [tidyHeatmap](https://stemangiola.github.io/tidyHeatmap/) and [tidyverse](https://www.tidyverse.org/) packages. The tidybulk package provides a tidy data structure and a modular framework for bulk transcriptional analyses and tidyHeatmap provides a tidy implementation of ComplexHeatmap. These packages are part of the tidytranscriptomics suite that introduces a tidy approach to RNA sequencing data.

### Pre-requisites

* Basic knowledge of RStudio
* Some familiarity with tidyverse syntax

Recommended Background Reading
[Introduction to R for Biologists](https://melbournebioinformatics.github.io/r-intro-biologists/intro_r_biologists.html)

### _R_ / _Bioconductor_ packages used

* tidyverse
* tidybulk
* tidyHeatmap
* tidygate
* limma
* edgeR
* DESeq2
* org.Mm.eg.db
* dittoSeq
* ggrepel
* GGally
* plotly

### Material goals and objectives

In exploring and analysing RNA sequencing data, there are a number of key concepts, such as filtering, scaling, dimensionality reduction, hypothesis testing, clustering and visualisation, that need to be understood. These concepts can be intuitively explained to new users, however, (i) the use of a heterogeneous vocabulary and jargon by methodologies/algorithms/packages, (ii) the complexity of data wrangling, and (iii) the coding burden, impede effective learning of the statistics and biology underlying an informed RNA sequencing analysis.

The tidytranscriptomics approach to RNA sequencing data analysis abstracts out the coding-related complexity and provides tools that use an intuitive and jargon-free vocabulary, enabling focus on the statistical and biological challenges.

#### Learning goals

* To understand the key concepts and steps of RNA sequencing data analysis
* To approach data representation and analysis though a tidy data paradigm, integrating tidyverse with tidybulk and tidyHeatmap.

#### Learning objectives

* Recall the key concepts of RNA sequencing data analysis
* Apply the concepts to publicly available data
* Create plots that summarise the information content of the data and analysis results
