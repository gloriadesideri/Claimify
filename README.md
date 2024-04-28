# Claimify
This repository contains the code for the Claimify project. The goal fo the project is perform an analysis of the
AVeriTec dataset, collecting claims and their veridicity. <br>
The link to the dataset can be found [here](https://fever.ai/dataset/averitec.html). 
The link to the original paper can be found [here](https://arxiv.org/abs/2305.13117).
## Installation
In order to properly run this project, you need to build a conda environment with the following packages:
```bash
conda create --name name python=3.11.5
conda activate name
```
Then, install the dependencies with the following command:
```bash
pip install -r requirements.txt
```
## Data Preprocessing
> ❗️<span style="color:red">**Important**</span>:
> for any data manypulation never use `reset_index=True`

## Dataset Preparation
Two datasets are extracted from the original one: the first one contains the claims and their veridicity, the second one contains the questions and the answers used to verify the veridicity. The datasets are stored in the `data\postprocessed` folder.
## Exploratory Analysis
Some plots are generated to get some insights about the data:
- The percentage of rejected claims per state.
- The number of rejected claim per speaker.
- The number of rejected claims per date.
- The number of rejected claims per date and state.
- The number of rejected claims per date and speaker.
## Clustering
Clustering analysis using LDA (Linear Dirichlet Allocation) is performed on the claims. The goal is to find the topics that are present in the claims.
An ANOVA analysis is performed to study whether the class assigned by the clustering to the claims is statistically significant.
The p-value of the ANOVA shows that the topics assigned to the claims influence the distribution of the data.
## Embeddings
Warning: to make gensim work an outdated version of scipy is necessary (1.10.1) refer to this issue: https://github.com/piskvorky/gensim/issues/3525
