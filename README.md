<div align="center">
<a name="logo"/>
<img src="./inst/TFregulomeR_logo.png" alt="TFregulomeR Logo" ></img>
</a>
</div>



TFregulomeR-dev

Version @ master: v1.2.2 (human only) [<img src="https://www.ymcachicago.org/page/-/kroehler/blog/icon-new-9.jpg" alt="new" width="30"></img>](./inst/update_notes/functionality_update.md)

Version @ with_mouse_version: v1.99.2 (human and mouse) [<img src="https://www.ymcachicago.org/page/-/kroehler/blog/icon-new-9.jpg" alt="new" width="30"></img>](./inst/update_notes/functionality_update.md)

[![Build Status](https://travis-ci.com/linquynus/TFregulomeR-dev.svg?branch=master)](https://travis-ci.com/linquynus/TFregulomeR-dev)

# Introduction
*TFregulomeR* comprises of a comprehensive compendium of transcription factor binding sites (TFBSs) derived from the MethMotif and GTRD, as well as the ready-to-use functionality in R language facilitating data access, integration and analysis. The binding motifs predicted in-silico from MethMotif and GTRD describe cell specific transcription factor (TF) binding propensities, while the DNA methylation profiles from MethMotif portray a second epigenetic dimension in TF binding events. The whole toolbox allows a better understanding of the TF binding propensities in a cell-specific manner.

-------

## Release notes

#### This repository is for TFregulomeR development release

#### Current TFregulomeR development version: 1.2.2 (Updated on 10 January 2020).

#### For stable release, please visit [TFregulomeR](https://github.com/benoukraflab/TFregulomeR)

-------

## Documentation
You can check detailed package instructions in [Vignettes](https://bioinfo-csi.nus.edu.sg/methmotif/API_TFregulomeR/TFregulomeR-Vignettes.html)

-------

## Current Functionalities v1.2.2
### Click [here](./inst/update_notes/functionality_update.md) for functionality update notes 
Note: new function is highlighted in bold font.

1) Browse the TFregulomeR data warehouse (dataBrowser)
2) Load TF peaks (loadPeaks)
3) Search motif matrix and DNA methylation score matrix (searchMotif)
4) Plot motif or MethMotif logo (plotLogo)
5) Export motif matrix and DNA methylation score matrix (exportMMPFM)
6) Get context-independent peaks along with DNA methylation profiles (commonPeaks & commonPeakResult)
7) Get context-dependent peaks along with DNA methylation profiles (exclusivePeaks & exclusivePeakResult)
8) Form a intersected matrix between two lists of peak sets along with DNA methylation profiles, read enrichments and **users' input external signals**, for interactome and co-binding partner studies (intersectPeakMatrix & intersectPeakMatrixResult). **- NEW Feature**
9) Automatically generate a PDF report for TF co-factors along with motif sequences, DNA methylation (within motif and in 200bp regions) and read enrichments (cofactorReport).
10) **Automatically produce a dynamic three-dimensional interface showing TF interactome coupled with DNA methylation and/or users’ input external signal values (interactome3D). - NEW Function**
11) Plot the TFBS distribution in a given list of peak sets (motifDistrib & plotDistrib).
12) Annotate peak genomic locations (genomeAnnotate).
13) Annotate ontologies of target genes by a peak set (greatAnnotate).
14) Convert a motif matrix to a PFMatrix calss object for *TFBSTools* package (toTFBSTools).

-------

## Current TFBSs in TFregulomeR compendium

 ### Click [here](./inst/update_notes/compendium_update.md) for TFregulomeR compendium update notes

TFregulomeR data compendium version: 1.2.0

| Item     | Count |
| :---------:|:------:|
| PWM     | 1468   |
| ChIP-seq experiments    | 3891   |
| Unique TF     | 415   |
| PWM with DNA methylation records    | 655   |
| Species     | human (hg38)  |
| Organ   | stem_cell, blood_and_lymph, connective_tissue, colorectum, brain, bone, stomach, prostate, breast, pancreas, skin, kidney, lung, eye, esophagus, heart, muscle, uterus, spleen, cervix, testis, liver, adrenal_gland, neck_and_mouth, pleura, ovary, thymus, fallopian, vagina   |
| Sample type | primary_cells, cell_line, tissue
| Cell or tissue | 414 |
| Disease state | normal, tumor, Simpson_Golabi_Behmel_syndrome, progeria, metaplasia, unknown, immortalized, premetastatic|
| Source | GTRD, MethMotif | 

-------

## Citation

Quy Xiao Xuan Lin, Denis Thieffry, Sudhakar Jha, Touati Benoukraf. (2019) **TFregulomeR reveals transcription factors’ context-specific features and functions.** _Nucleic Acids Res._, 10.1093/nar/gkz1088. [[Manuscript](https://doi.org/10.1093/nar/gkz1088)]

-------

## Case studies

The scripts of case studies used in our manuscript are available as below.

1. [Case study of CEBPB](./inst/case_study/case_study_of_CEBPB.R)
2. [Case study of MAFF](./inst/case_study/case_study_of_MAFF.R)
3. [Case study of ATF3](./inst/case_study/case_study_of_ATF3.R)

-------


## Installation

#### Prerequisite pakcages

1) Required packages: the packages below are the basic prerequisite packages for *TFregulomeR* functionalities

    - [jsonlite](https://cran.r-project.org/web/packages/jsonlite/index.html) (>= 1.5)
    - [ggplot2](https://cran.r-project.org/web/packages/ggplot2/index.html) (>= 3.0.0)
    - [ggseqlogo](https://cran.r-project.org/web/packages/ggseqlogo/index.html) (>= 0.1)
    - [gridExtra](https://cran.r-project.org/web/packages/gridExtra/index.html) (>= 2.3)
    - [GenomicRanges](https://bioconductor.org/packages/release/bioc/html/GenomicRanges.html) (>= 1.32.7)
    - [curl](https://cran.r-project.org/web/packages/curl/index.html) (>= 3.2)
    - [gplots](https://cran.r-project.org/web/packages/gplots/index.html) (>= 3.0.1.1)


2) Optional packages: the packages below are optional since they are required only in some functions or some options in a function

    - [rGREAT](https://bioconductor.org/packages/release/bioc/html/rGREAT.html) (>= 1.16.1): only requried in `greatAnnotate()`
    - [rbokeh](https://cran.r-project.org/web/packages/rbokeh/index.html) (>= 0.5.0): only required when users opt to export an intuitive HTML report in `greatAnnotate()`
    - [TxDb.Hsapiens.UCSC.hg38.knownGene](https://bioconductor.org/packages/release/data/annotation/html/TxDb.Hsapiens.UCSC.hg38.knownGene.html) (>= 3.4.0): only required when users opt to annotate hg38 peak locations in `genomeAnnotate()`
    - [TxDb.Hsapiens.UCSC.hg19.knownGene](https://bioconductor.org/packages/release/data/annotation/html/TxDb.Hsapiens.UCSC.hg19.knownGene.html) (>= 3.2.2): only required when users opt to annotate hg19 peak locations in `genomeAnnotate()`
    - [TFBSTools](http://bioconductor.org/packages/release/bioc/html/TFBSTools.html) (>= 1.20.0): only required in `toTFBSTools()`

#### Install

In R console,

```r
# if you have not installed "devtools" package
install.packages("devtools")
# install development version 1.2.2 linking to human data only
devtools::install_github("linquynus/TFregulomeR-dev", ref="master")
# install development version 1.99.2 linking to human and mouse data
devtools::install_github("linquynus/TFregulomeR-dev", ref="with_mouse_version")
```
The step above will automatically install the required packages. However, you still need to install optional packages if you opt to use the functions such as `greatAnnotate()`, `genomeAnnotate()` and `toTFBSTools()`.

-------

## License

GNU General Public License v3.0