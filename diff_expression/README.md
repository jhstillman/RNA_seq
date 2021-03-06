_*.R scripts meant for differential gene expression analysis using files generated by _/blacklight_pipeline_ scripts*_

--

**get_express_data.R**

Gets eXpress expression estimate data, generated by blacklight pipelinescripts, for subequent use in R.  Saves an ".RData" object with total counts, fpkm values, and treatment groupings.

--

**get_DEG_list.R**

Generates a list of differentially expressed genes using the R object created by get_express_data.R  

This is meant to be used interactively in an IDE such as R Studio.

--

**GSEA_w_topGO.R**

This takes the topTags*.csv files generated by xprs_2_edgeR.R and performs a gene set enrichment analysis (GSEA) based on the GO terms from a Trinotate annotation file.  It implements the Fisher exact test on the tags found to be significantly differentially expressed in xprs_2_edgeR.R but can be adapted for other tests; see the topGO documentation:
http://www.bioconductor.org/packages/release/bioc/vignettes/topGO/inst/doc/topGO.pdf

This is meant to be used interactively in an IDE such as R Studio.

--

**clustering_and_heatmap.R**

Clusters transcripts based on their expression response and makes a heatmap.

--

**housekeeping_candidates.R**

Finds candidate housekeeping genes based on lowest coefficient of variation (ratio, standard deviation : mean).
