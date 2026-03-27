# Single_cell_generation
The project aimed to generate synthetic single-cell RNA sequencing data to provide enough training data for building robust classifiers that would be able to identify cancerous cells.
We used a Generative Adversarial Network with a Wasserstein distance-based loss function to generate synthetic data that closely resemble real data and preserved the GRN structure. We added an additional term to the loss function of the Adversarial Network that tracked the distance between the covariance matrices of generated and real data. 
