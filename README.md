# High-throughput-tech

DESEQ2 R Tutorial
https://lashlock.github.io/compbio/R_presentation.html

Count-Based Differential Expression Analysis of RNA-seq Data
http://bioconnector.github.io/bims8382/r-rnaseq-airway.html

Analyzing RNA-seq data with DESeq2
http://bioconductor.org/packages/release/bioc/vignettes/DESeq2/inst/doc/DESeq2.html#pre-filtering

Differential Expression with Limma-Voom
https://ucdavis-bioinformatics-training.github.io/2018-June-RNA-Seq-Workshop/thursday/DE.html

StatQuest: A gentle introduction to ChIP-Seq
https://www.youtube.com/watch?v=nkWGmaYRues

A Comparison of Methods: Normalizing High-Throughput RNA Sequencing Data 
https://www.biorxiv.org/content/10.1101/026062v1.full.pdf

Normalisation methods implemented in edgeR
https://davetang.org/muse/2011/01/24/normalisation-methods-for-dge-data/

A Scaling Normalization Method for Differential Expression Analysis of RNA-seq Data (Robinson)
https://pubmed.ncbi.nlm.nih.gov/20196867/

In Papyro Comparison of TMM (edgeR), RLE (DESeq2), and MRN Normalization Methods for a Simple Two-Conditions-Without-Replicates RNA-Seq Experimental Design
https://www.frontiersin.org/articles/10.3389/fgene.2016.00164/full

Comparison of TMM (edgeR), RLE (DESeq2), and MRN Normalization Methods
https://www.rna-seqblog.com/comparison-of-tmm-edger-rle-deseq2-and-mrn-normalization-methods/

TMM normalized FPKM vs TPM: which metric to use?
https://groups.google.com/forum/#!topic/rsem-users/GRyJfEOK1BQ
    So an even briefer summary is:
    if you want to compare relative abundances: use TPM
    if you want to compare absolute abundances: use normalized read count or normalized FPKM values (where "normalized" = the results of     TMM or a similar method)

getlength: Retrieves Gene length data
"The length of a gene is taken to be the median length of all its mature, mRNA, transcripts. It is always preferable to obtain length information directly for the gene ID used to summarize your count data, rather than converting IDs and then using the supplied databases. Even when two genes have a one-to-one mapping between different identifier conventions (which is often not the case), they frequently refer to slightly different regions of the genome with different lengths. It is therefore recommended that the user perform the full analysis in terms of only one gene ID, or manually obtain their own length data for the identifier used to bin reads by gene."
https://rdrr.io/bioc/goseq/man/getlength.html

Get gene length with R
https://www.biostars.org/p/317962/
