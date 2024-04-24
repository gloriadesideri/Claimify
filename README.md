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

