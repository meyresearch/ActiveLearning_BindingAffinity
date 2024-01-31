# Benchmarking active learning protocols for ligand binding affinity prediction

This repository contains datasets used in our study.

## Project Abstract

Active learning (AL) has become a powerful tool in computational drug discovery, enabling the identification of top binders from vast molecular libraries with reduced costs for relative binding free energy calculations and experiments. To design a robust AL protocol, it is important to understand the influence of AL parameters, as well as the features of the datasets on the outcomes. We use four affinity datasets for different targets (TYK2, USP7, D2R, Mpro) to systematically evaluate the performance of machine learning models (Gaussian Process model, Chemprop), sample selection protocols, as well as the batch size based on metrics describing the overall predictive power of the model (R2, Spearman rank, RMSE) as well as the accurate identification of top 2% / 5% binders (Recall, F1 score). Both models have a comparable Recall of top binders on large datasets, but the GP models surpass Chemprop when training data is sparse. A larger initial batch size, especially on diverse datasets, increased the Recall of both models as well as overall correlation metrics. However, for subsequent cycles, smaller batch sizes of 20 or 30 compounds proved to be desirable. Furthermore, the presence of Gaussian noise to the data, up to a certain threshold, still allowed the model to identify clusters with top-scoring compounds. However, excessive noise (<1σ) did impact the model’s predictive and exploitative capabilities.

### Dataset files

We use four binding affinity datasets, each dataset corresponds to a different protein target- Tyrosine Kinase 2 (TYK2), Dopamine Receptor D2 (D2R), Ubiquitin-Specific Protease 7 (USP7), and SARS-CoV-2 Main Protease (Mpro). The datasets are provided in CSV format, featuring columns for SMILES (chemical structure representation), affinity (binding scores in pKi for TYK2/D2R and pIC50 for USP7/Mpro), target protein, and indicators for top 2% and top 5% binders.
