https://resources.qiagenbioinformatics.com/manuals/clcgenomicsworkbench/1000/index.php?manual=TMM_Normalization.html

TMM Normalization
Since the sequencing depth might differ between samples, a per-sample library size normalization must be performed before samples can be compared. In the case of the tools included in the RNA-Seq folder, this normalization is automatically applied by the tools.

All of the tools in the RNA-Seq folder use the TMM (trimmed mean of M values) normalization method [Robinson and Oshlack, 2010] to calculate effective libraries sizes, which are then used as part of the per-sample normalization. TMM normalization is the normalization used in EdgeR [Robinson et al., 2010].

TMM normalization adjusts library sizes based on the assumption that most genes are not differentially expressed. Therefore, it is important not to make subsets of the count data before doing statistical analysis or visualization, as this can lead to differences being normalized away.

For the expression visualization tools (Create Heat Map and PCA for RNA-Seq) additional filtering and normalization are performed:

'log CPM' (Counts per Million) values are calculated for each gene. The CPM calculation uses the effective library sizes as calculated by the TMM normalization.
After this first normalization, a second one is performed across samples for each gene: the counts for each gene are mean centered, and scaled to unit variance.
Genes or transcripts with zero expression across all samples or invalid values (NaN or +/- Infinity) are removed.
