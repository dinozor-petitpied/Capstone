Project Overview

In this project, I am interested in studying the heterogeneity of Non-Hodgkin B-cell lymphoma. Until recently, the tumor gene expression was achieved with measurement on bulk cells. However, the emergence of treatment resistance raised the importance of tumor heterogeneity in the appearance of the resistance mechanism. Tumor heterogeneity refers to the high diversity of cells showing different gene expression levels.
Single-cell analysis techniques have revolutionized the ability to study this heterogeneity by allowing the examination of the characteristics of individual cells rather than averaging them out in bulk assays. 
In this project, I aim to integrate different samples:

A single-cell dataset containing 11 samples has been made available on Kaggle:
- 3 DLBCL (malignant)
- 3 Follicular Lymphoma (malignant)
- 2 transformed lymphoma (malignant)
- 3 reactive lymph nodes (non-malignant)

The 11 samples come from two different batch experiments. My first aim will be to remove this side effect. Secondly, I need a model that effectively separates B-cells and T-cells to understand non-Hodgkin B-cell lymphoma better. Eventually, the final clustering should describe the lymph node function as closely as we know about this organ thus far, ideally identifying different stages of the Germinal center reaction. In this structure, B-cells are trained to produce highly specified antibodies, and Non-Hodgkin B-cell lymphoma originates in the germinal center reaction.
To evaluate the final clustering, I looked at the gene expression within each cluster, identifying B-cell stages based on current knowledge in the field. I also calculated a silhouette score to evaluate the clustering without any ground truth to compare with.
The batch effect was partly addressed after running the first model (PCA, neighbors, Leiden algorithm, UMAP) on two samples (rLN1 and rLN2). However, the separation of B-cells and T-cells was not optimal (based on CD19 expression). 
The Variational AutoEncoder from the scvi library addressed two issues: the batch effect and good B-cell and T-cell separation.
If this gets solved well enough, I will run more analyses on the whole dataset to extract some biological insight.

For sprint three, there are two notebooks: the AnneSophieHoward_capstone_sprint3, which describes three modeling approaches for clustering the dataset, and the SCALEX notebook, which describes the use of the already-trained model SCALEX to correct for batch effect.

To-do list
[X] Initial data exploration
[X] Looping the exploratory data analysis to all the files available in the dataset
[X] Running a first clustering method
[X] Introducing some metrics to compare different algorithm performance
[X] Trying out different algorithms
[X] Implementing a neural network
[X-partly] Using an already trained neural network (SCALEX)