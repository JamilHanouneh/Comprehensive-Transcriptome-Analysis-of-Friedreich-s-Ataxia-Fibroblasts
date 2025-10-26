# Comprehensive Transcriptome Analysis of Friedreich's Ataxia Fibroblasts

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8+-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![FAU](https://img.shields.io/badge/FAU-Erlangen--Nürnberg-003366.svg)
![RNA-seq](https://img.shields.io/badge/RNA--seq-Transcriptomics-red.svg)
![FRDA](https://img.shields.io/badge/Disease-Friedreich's%20Ataxia-purple.svg)
![Bioinformatics](https://img.shields.io/badge/Field-Bioinformatics-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

A comprehensive differential gene expression analysis of Friedreich's Ataxia (FRDA) patient fibroblasts versus control samples using RNA-seq data. This project identifies significantly dysregulated genes and molecular pathways involved in FRDA pathogenesis.

## Overview

Friedreich's ataxia (FRDA) is an autosomal recessive neurodegenerative disease caused by GAA repeat expansions in intron 1 of the frataxin (FXN) gene, resulting in reduced frataxin expression. This analysis performs differential gene expression (DGE) profiling on fibroblast samples from 18 FRDA patients and 17 unaffected controls to identify molecular hallmarks and potential biomarkers.

## Key Features

- Differential expression analysis between FRDA and control fibroblasts
- Statistical testing with multiple comparison correction
- Volcano plot visualization of differentially expressed genes
- Gene signature identification and functional pathway analysis
- Comprehensive output tables with statistical metrics

## Dataset

The analysis uses RNA-seq data from GEO accession **GSE104288**:

**Title:** Comprehensive Analysis of Gene Expression Patterns in Friedreich's Ataxia Fibroblasts by RNA Sequencing Reveals Altered Levels of Protein Synthesis Factors and Solute Carriers

**Source:** [NCBI GEO GSE104288](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE104288)

**Organism:** Homo sapiens

**Samples:** 18 FRDA patients, 17 unaffected controls

**Platform:** Illumina HiSeq 2000

**Reference:**
Napierala JS, Li Y, Lu Y, Lin K, et al. Comprehensive analysis of gene expression patterns in Friedreich's ataxia fibroblasts by RNA sequencing reveals altered levels of protein synthesis factors and solute carriers. *Dis Model Mech* 2017 Nov 1;10(11):1353-1369. PMID: 29125828

### Downloading the Dataset

1. Visit the [GEO dataset page](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE104288)
2. Download the required data files (raw counts or processed expression matrix)
3. Create a `dataset/` directory in the project root
4. Place the downloaded files in the `dataset/` directory

```
mkdir dataset
# Place your downloaded GSE104288 files here
```

## Repository Structure

```
.
├── FRDA_DGE_Analysis.ipynb    # Main analysis notebook
├── dataset/                    # Dataset directory (user must download)
├── results/                    # Analysis outputs
│   ├── DE_results_FRDA_vs_CTRL.tsv
│   ├── Signature_shifts.tsv
│   └── Volcano Plot Differential Expression in FRDA vs. CTRL.pdf
├── requirements.txt            # Python dependencies
├── LICENSE                     # MIT License
└── README.md                   # This file
```

## Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Setup

1. Clone the repository:
```
git clone https://github.com/JamilHanouneh/Friedreich-Ataxia-Transcriptome-Analysis.git
cd Friedreich-Ataxia-Transcriptome-Analysis
```

2. Create a virtual environment (recommended):
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```
pip install -r requirements.txt
```

4. Download the dataset (see Dataset section above)

## Usage

1. Ensure the dataset is placed in the `dataset/` directory
2. Launch Jupyter Notebook:
```
jupyter notebook
```
3. Open `FRDA_DGE_Analysis.ipynb`
4. Run all cells sequentially

The notebook will generate analysis results in the `results/` directory.

## Results

The analysis produces three main outputs:

### DE_results_FRDA_vs_CTRL.tsv
Complete table of differentially expressed genes with:
- Gene identifiers
- Log2 fold changes
- Statistical significance values (p-values, adjusted p-values)
- Mean expression levels

### Signature_shifts.tsv
Gene signature analysis showing coordinated expression changes across functional gene sets

### Volcano Plot Differential Expression in FRDA vs. CTRL.pdf
Publication-quality visualization displaying:
- Log2 fold change (x-axis)
- Statistical significance (y-axis)
- Highlighted significantly differentially expressed genes

## Key Findings

The analysis reveals significantly altered expression of genes involved in:

- **Upregulated:** Plasma membrane solute carrier proteins (consistent with published findings)
- **Downregulated:** Protein synthesis factors (cytoplasmic and mitochondrial)
- **Downregulated:** Antioxidant defense genes

These findings align with known FRDA pathophysiology and provide insights into molecular mechanisms of disease progression.

## Citation

If you use this analysis in your research, please cite:

```
@software{Hanouneh_FRDA_Transcriptome_2025,
  author = {Hanouneh, Jamil},
  title = {Comprehensive Transcriptome Analysis of Friedreich's Ataxia Fibroblasts},
  year = {2025},
  url = {https://github.com/JamilHanouneh/Friedreich-Ataxia-Transcriptome-Analysis}
}
```

Please also cite the original dataset:

```
@article{Napierala2017,
  author = {Napierala, Jill S. and Li, Yanbin and Lu, Yanjie and Lin, Kevin and others},
  title = {Comprehensive analysis of gene expression patterns in Friedreich's ataxia fibroblasts by RNA sequencing reveals altered levels of protein synthesis factors and solute carriers},
  journal = {Disease Models \& Mechanisms},
  volume = {10},
  number = {11},
  pages = {1353--1369},
  year = {2017},
  doi = {10.1242/dmm.030536},
  pmid = {29125828}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Jamil Hanouneh**

Computational imaging and vision researcher | Medical engineer

Friedrich-Alexander-Universität Erlangen-Nürnberg

- GitHub: [@JamilHanouneh](https://github.com/JamilHanouneh)
- LinkedIn: [jamil-hanouneh](https://www.linkedin.com/in/jamil-hanouneh-39922b1b2)
- Email: jamil.hanouneh1997@gmail.com

## Acknowledgments

- Original dataset contributors: Napierala Lab, University of Alabama at Birmingham
- RNA-seq data deposited in NCBI GEO: GSE104288
- Supported by NIH grant R01 NS081366

## Related Publications

1. Napierala JS, Li Y, Lu Y, Lin K, et al. (2017) Comprehensive analysis of gene expression patterns in Friedreich's ataxia fibroblasts by RNA sequencing. *Dis Model Mech* 10(11):1353-1369.

2. McMackin MZ, Durbin-Johnson B, Napierala M, et al. (2019) Potential biomarker identification for Friedreich's ataxia using overlapping gene expression patterns. *PLoS One* 14(10):e0223209.

3. Misiorek JO, Schreiber AM, Urbanek-Trzeciak MO, et al. (2020) A Comprehensive Transcriptome Analysis Identifies FXN and BDNF as Novel Targets of miRNAs in Friedreich's Ataxia Patients. *Mol Neurobiol* 57(6):2639-2653.
```
