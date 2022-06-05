# Introduction

## Scientific Question:
Can a model organism for melanoma drug treatment be identified via high sequence similarity to TNFα protein in humans?

## Hypothesis:
If an organism’s TNFα protein sequence is <70% similarity to Human TNFα protein sequence, especially near the ligand binding site, then that organism can be potentially used a model organism for drug treatment testing.

# Project Description
In this project, I performed pairwise sequence alignment and multiple sequence alignment to identify similarities in the 10 selected sequences of TNF-alpha protein downloaded from Uniprot. The results were visualized using MSA output in the notebook, heatmap of pairwise alignment score and sequence logo visualization for MSA.

Further I tried to identify residues in binding sites of TNF-alpha protein. The protein was downloaded from rcsb.org and PDB ID is 5VH4. I used bio3d package to find residue number in the binding site of protein and displayed them in my notebook. Further I also used NGLViewer to visualize the protein structure in the notebook.


# File Description

## Input files to reproduce analysis:

* `Balang_Project2C.Rmd`
This is the R notebook file containing all code to reproduce bioinformatics analysis to test above hypothesis. 

* `TNFA_aa_seq.fasta`
This is input FASTA file required in the analysis. It contains 10 TNFα protein sequences of different organism downloaded from [UniProt](https://www.uniprot.org/).

Sequences used with UniProt IDs in the above FASTA file are: 

1. P23383 | TNFA_SHEEP | [https://www.uniprot.org/uniprot/P23383](https://www.uniprot.org/uniprot/P23383)
2. P29553 | TNFA_HORSE | [https://www.uniprot.org/uniprot/P29553](https://www.uniprot.org/uniprot/P29553)
3. P23563 | TNFA_PIG | [https://www.uniprot.org/uniprot/P23563](https://www.uniprot.org/uniprot/P23563)             
4. P16599 | TNFA_RAT | [https://www.uniprot.org/uniprot/P16599](https://www.uniprot.org/uniprot/P16599)      
5. P06804 | TNFA_MOUSE | [https://www.uniprot.org/uniprot/P06804](https://www.uniprot.org/uniprot/P06804)         
6. P13296 | TNFA_CAPHI | [https://www.uniprot.org/uniprot/P13296](https://www.uniprot.org/uniprot/P13296)
7. P04924 | TNFA_RABIT | [https://www.uniprot.org/uniprot/P04924](https://www.uniprot.org/uniprot/P04924)
8. P51742 | TNFA_CANLF | [https://www.uniprot.org/uniprot/P51742](https://www.uniprot.org/uniprot/P51742)
9. Q06599 | TNFA_BOVIN | [https://www.uniprot.org/uniprot/Q06599](https://www.uniprot.org/uniprot/Q06599)
10. P01375 | TNFA_HUMAN | [https://www.uniprot.org/uniprot/P01375](https://www.uniprot.org/uniprot/P01375)


# Output files

* Balang_Project2C.html
This is the knitted HTML file produced by running above R Notebook. For this analysis in MSA, I produced a PDF file as well containing visualization which is required to display in this HTML.

* msa_output.pdf
This is the Multiple Sequence Alignment visualization output from my analysis and used futher in knitted HTML to display.   

# R Package Requirements

* R version used: `4.1.1`

### Install CRAN packages using install.packages() and Bioconductor package using BiocManager::install()

* To read the FASTA sequence data and perform pairwise alignment
  `library(Biostrings)`
* To perform multiple sequence alignment 
  `library(msa)`
* To identify residues in protein binding site
  `library(bio3d)`
  `library(gplots)`
* To convert tex format to pdf after MSA results
 `library(tools)`
* To visualize protein structure
  `library(NGLVieweR)`
