# Urban Appraisal Analysis

This repository contains original analysis code for the Urban Appraisal EEG
dataset. Raw data and upstream analysis code are kept as separately managed
repositories and are not committed here.

## Layout

- `data/ds006850/`: OpenNeuro dataset, managed with DataLad/git-annex
- `external/perception2appraisal_analyses/`: analysis code from the research group
- `src/`: original analysis code for this project
- `results/`: generated outputs (not tracked by Git)
- `environment.yml`: reproducible Conda environment

## Set up the environment

```bash
conda env create -f environment.yml
conda activate urban-appraisal
```

Install `git-annex` separately on Apple Silicon:

```bash
brew install git-annex
```

## Obtain the dataset

```bash
mkdir -p data
git clone https://github.com/OpenNeuroDatasets/ds006850.git data/ds006850
cd data/ds006850
datalad get sub-02 sub-04
cd ../..
```

## Obtain the original analysis code

```bash
mkdir -p external
git clone https://github.com/BeMoBIL/perception2appraisal_analyses.git \
  external/perception2appraisal_analyses
```
