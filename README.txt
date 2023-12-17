Project Overview

In this project, I am interested in studying the heterogeneity of Non-Hodgkin B-cell lymphoma. Until recently, the tumor gene expression was achieved with measurement on bulk cells. However, the emergence of resistance to some treatments raised the importance of tumor heterogeneity in the appearance of the resistance mechanism. Tumor heterogeneity refers to the high diversity of cells showing different gene expression levels.
Single-cell analysis techniques have revolutionized the ability to study this heterogeneity by allowing the examination of the characteristics of individual cells rather than averaging them out in bulk assays. 
After running the first model on two samples, I saw some batch effects in between samples. I will focus on correcting the batch effect with machine learning between samples in the project's near future. 
If this gets solved well enough, I will run more analyses on the whole dataset to extract some biological insight.

Dataset

A single-cell dataset containing 11 samples has been made available on Kaggle:
- 3 DLBCL (malignant)
- 3 Follicular Lymphoma (malignant)
- 2 transformed lymphoma (malignant)
- 3 reactive lymph nodes (non-malignant)

To-do list
[X] Initial data exploration
[X] Looping the exploratory data analysis to all the files available in the dataset
[X] Running a first clustering method
[ ] Introducing some metrics to compare different algorithm performance
[ ] Trying out different algorithms
[ ] Implementing a neural network
[ ] Using an already trained neural network (SCALEX)