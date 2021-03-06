BlockClust
==========

**What it does**

BlockClust is an efficient approach to detect transcripts with similar
processing patterns. We propose a novel way to encode expression profiles
in compact discrete structures, which can then be processed using
fast graph-kernel techniques. BlockClust allows both clustering and
classification of small non-coding RNAs.

BlockClust runs in three operating modes:

1) Pre-processing - converts given mapped reads (BAM) into BED file of tags

2) Clustering and classification - of given input blockgroups (output of blockbuster tool) as explained in the original paper.

3) Post-processing - plots for overview of predicted clusters.

For a thorough analysis of your data, we suggest you to use complete blockclust workflow, which contains all three modes of operation.

**Inputs**

BlockClust input files are dependent on the mode of operation:

1. Pre-processing mode:
    * Binary Sequence Alignment Map (BAM) file

2. Clustering and classification:
    * A blockgroups file generated by blockbuster tool
    * Select reference genome

3. Post-processing:
    * Output of cmsearch, searched clusters generated by BlockClust against Rfam
    * BED file containing clusters generated by BlockClust
    * Pairwise similarities of blockgroups generated by BlockClust

**Outputs**

1. Pre-processing mode:
    * BED file of tags with expressions

2. Clustering and classification:
    * Hierarchical clustering plot of all input blockgroups by their similarity
    * Pairwise similarities of all input blockgroups
    * BED file containing predicted clusters
    * BED file containing prediction of blockgroups by pre-compiled SVM binary classification model.

3. Post-processing:
    * Plot of distribution of ncRNA families per predicted cluster (overview of cluster precissions). The annotation of ncRNA families are retrieved by searching cluster instances against Rfam database.
    * Hierarchical clustering made out of centroids of each BlockClust predicted cluster


