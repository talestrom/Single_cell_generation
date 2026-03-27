# Single_cell_generation
The project aimed to generate synthetic single-cell RNA sequencing data to provide enough training data for building robust classifiers that would be able to identify cancerous cells.
We used a Generative Adversarial Network with a Wasserstein distance-based loss function to generate synthetic data that closely resemble real data and preserved the GRN structure. We added an additional term to the loss function of the Adversarial Network that put a penalty on the distance between the covariance matrices of generated and real data. 

The Notebook includes the following steps:
1. Uploading and summarization of the data: single-cell RNA sequences.
2. Data visualization after dimensionality reduction (UMAP).
3. Graphical lasso analysis.
4. Synthetic data generation via Wasserstein-GAN.
5. Comparison of visualization after UMAP reduction and Graphical lasso results between the synthetic and the real data.
6. Training a model that includes an additional term that penalizes difference in Graphical lasso in the loss function - generate synthetic data using this approach.
7. Comparison of visualization after UMAP reduction and Graphical lasso results between two types of synthetic data (with and without the modified loss function) and the real data.

Dataset used is compiled from 4 publicly available datasets under the GEO accessions: GSE90848 (Yang, mouse hair follicle subpopulations), GSE67602 (Joost, mouse epidermal cells), GSE99989 (Ghahramani, in vitro mouse keratinocytes), GSE96772 (Buenrostro, human blood cells), and at the Short Read Archive under accession number SRP073767 (Zheng, human blood monocytes). The datasets were combined and normalized by authors of the paper "Generative adversarial networks simulate gene expression and predict perturbations in single cells" (https://www.biorxiv.org/content/10.1101/262501v2.full). The combined dataset is avilable at https://github.com/luslab/scRNAseq-WGAN-GP/tree/master/data.
