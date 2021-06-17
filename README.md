# Synthetic Lethality Cloud (SL-Cloud)

This project provides a cloud-based data access platform coupled with software and well documented computational notebooks that re-implement published synthetic lethality (SL) inference algorithms to facilitate novel investigation into synthetic lethality. In addition  we provide general purpose functions that support these prediction workflows e.g. saving data in bigquery tables as well as functions that implement common bioinformatic analyses such as  survival analysis, pathway enrichment etc. using this cloud-based framework. We anticipate that computationally savvy users can leverage the resources provided in this project to conduct highly customizable analysis based on their cancer type of interest and particular context. 

## Resource Overview
![Resource Overview. Structure of the SL-Hub resource that shows the integration of various cancer genomics datasets and Jupyter notebooks into a cloud-based SL inference resource. ](https://github.com/bhrtrcn/SyntheticLethality/blob/master/figures/slhub_overview.png)

***
### Scripts
- [SL library](https://github.com/IlyaLab/SL-Cloud/tree/main/scripts/)
***

### Notebooks
We provide representative synthetic lethal inference workflow based on highly cited published workflows

#### Sythetic Lethality Inference Workflows 

- [DAISY Pipeline](https://github.com/IlyaLab/SL-Cloud/blob/main/DAISY_pipeline/DAISY_from_library.ipynb) 
- [Mutation-based Conditional Dependence](https://github.com/bhrtrcn/SyntheticLethality/blob/c7bf444b2eece46777dd545b52f18cd4150d0153/Notebooks/mutation_based_conditional_dependence_pipeline/SL-mut-crispr.ipynb)
- [Conservation-based Inference from Yeast Genetic Interactions](https://github.com/bhrtrcn/SyntheticLethality/blob/c7bf444b2eece46777dd545b52f18cd4150d0153/Notebooks/leveraging_conservation_pipeline/YeastOrtholog_SL_pairs.ipynb)

#### Integrative Analysis
- The SL pairs found by different inference approaches for a given gene 
- The SL pairs with highest evidence from different inference approaches
- The SL pairs for a list of genes

#### Data Wrangling and Cleaning Associated Procedures 
- Dataset Creation
- Table Creation
- Writing into Excel File
- Gene conversion among gene symbol, EntrezID and alias 

#### Downstream Analysis Routines

- Survival analysis given SL partners are both mutant or both under-expressed
- Mutation frequency in cancer using TCGA data
- Tissue specific evidence for SL partners from CRISPR and shRNA datasets
- Gene set enrichment analysis of SL partners of a given gene
- Over-expression analysis of SL candidate given gene of interest is active/inactive 


#### Additional Pipelines 

***

### Synthetic-Lethality Inference Data Resources
This resource provides access to publicly available cancer genomics datasets relevant for SL inference. These data have been pre-processed, cleaned and stored in cloud-based query-able tables leveraging [Google BigQuery](https://cloud.google.com/bigquery)  technology. In addition we leverage relevant datasets available through the Institute for Systems Biology Cancer Genomics Cloud ([ISB-CGC](https://isb-cgc.appspot.com/)) to make inferences of potential synthetic lethal interactions. 
The following represent project-specific datasets with relevance for SL inference:

- **DEPMAP**: DEPMAP shRNA (DEMETER2 V6) and CRISPR (DepMap Public 20Q3) gene expression, sample information, mutation and copy number alterations and gene dependency scores for shRNA and gene effect scores for CRISPR experiments.

- **CellMap**: Yeast interaction dataset based on fitness scores after single and double knockouts from SGA experiements

- **Gene Information**: Tables with relevant gene annotation information such as yeast and human ortholog information, gene-alias-Entrez ID mapping, gene Ensembl-id mapping, gene-Refseq mapping and  cancer driver genes.

## Getting Started

### Account Creation
To be able to use our platform, researchers first need to have a Google registered email, a Google Cloud account and have created a Google Project. They can connect the ISB-CGC to their project to be able to use the tables available in our database. How to use ISB-CGC are explained in detail by videos and notebooks on  [https://isb-cgc.appspot.com]([https://isb-cgc.appspot.com).


### Accessing SL Resource

We should explain how they can access our tables from their resources. 
Shall we add figures here or give link to the documentation file?
