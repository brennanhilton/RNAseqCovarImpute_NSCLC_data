RNAseqCovarImpute with the NSCLC dataset
================
2024-05-07

This repo includes code examining the differential expression analysis
performance of complete case, single imputation, and RNAseqCovarImpute
methods at dealing with missing covariate data in the NSCLC dataset.

The non-small cell lung cancer (NSCLC) dataset was downloaded from the
European Molecular Biology Laboratory - European Bioinformatics
Institute [EMBL-EBI:
E-GEOD-81089](https://www.ebi.ac.uk/gxa/experiments/E-GEOD-81089/Downloads).
If you download this repo from GitHub and want to run the code, you will
need to download the counts indicated on the EMBL-EBI page indicated as
“All raw counts for the experiment.” I renamed the experiment-design.tsv
file as “covariates.tsv”.

First run the “RNAseqCovarImpute with NSCLC data.Rmd” file. It includes
code for differential expression analysis using the full data,
simulating missing data points under MCAR, MAR, and MNAR mechanisms, and
then conducting differential expression analysis using the complete
case, single imputation, and RNAseqCovarImpute methods to handle missing
data. We additionally compare three different versions of
RNAseqCovarImpute, the MI Gene Bin, MI PCA 80%, and MI PCA Horn methods.

Then run the “RNAseqCovarImpute with NSCLC data plot.Rmd” file. It
includes code for plotting the results in terms of true positive rate
(TPR), false positive rate (FPR), and mean absolute percentage error
(MAPE).

[The RNAseqCovarImpute package is available on
Bioconductor](https://bioconductor.org/packages/release/bioc/html/RNAseqCovarImpute.html)
