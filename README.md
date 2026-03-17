# Bacterial-Genome-Analysis-using-BioPython-
Python pipeline for ORF detection, protein translation, and BLASTp homology search across the complete genome of *Clostridium botulinum* A str. ATCC 3502.

Developed as a part of coursework @ Carnegie Mellon University.

## 🧬 Project Overview
This project implements an end-to-end genome analysis pipeline using BioPython to extract and characterize protein-coding regions from a bacterial genome obtained from the [NCBI RefSeq database](https://www.ncbi.nlm.nih.gov/refseq/).

The workflow includes:
* ORF detection on forward and reverse DNA strands.
* Translation of nucleotide sequences to proteins.
* Protein molecular weight calculation.
* BLASTp similarity search against the NCBI nr database.

Detailed analysis, methods and code are available in the Jupyter Notebook.

## 📁 Files in this Repository
* Final Project PCB - 03701.ipynb - Complete Jupyter Notebook with pipeline, code, and analysis
* Final Project Report PCB - 03701.pdf - Detailed report with methodology, results, and discussion
* data/ - Genome FASTA file (GCF_000063585.1_ASM6358v1_genomic.fna)
* outputs/ - CSV files containing ORFs (all_orfs.csv) and protein sequences (all_proteins.csv)
*Note*: BLASTp results are included and summarized in the Jupyter Notebook

## 🧫 Organism and Data

| Field           | Details                                  |
| --------------- | ---------------------------------------- |
| Organism        | *Clostridium botulinum* A str. ATCC 3502 |
| RefSeq Assembly | GCF_000063585.1                          |
| Source          | NCBI RefSeq                              |

## ⬇️ Downlaod Genome
#### create data directory if it doesn't exist
mkdir -p data

#### download genome FASTA file
curl https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/063/585/GCF_000063585.1_ASM6358v1/GCF_000063585.1_ASM6358v1_genomic.fna.gz \
  -o data/GCF_000063585.1_ASM6358v1_genomic.fna.gz

#### unzip the genome file
gunzip data/GCF_000063585.1_ASM6358v1_genomic.fna.gz

## ▶️ Reproducing the Analysis

#### 1. Clone the repository

git clone https://github.com/yourusername/bacterial-genome-analysis.git
cd bacterial-genome-analysis

#### 2. Ensure the genome file is in the data/ folder (see steps above).

#### 3. Run the notebook

jupyter notebook "Final Project PCB - 03701.ipynb"

## 🔄 Pipeline Overview

```
Genome (FASTA)
      ↓
ORF Detection
      ↓
Protein Translation
      ↓
Protein Feature Analysis
      ↓
BLASTp Homology Search
      ↓
CSV Output Files
```

## 📊 Key Results
* Identified 26,970 ORFs across forward and reverse strands.
* Computed molecular weights for all translated proteins.
* Selected 5 proteins (<1000 AA) for BLASTp analysis.
* BLASTp searches returned top 3 hits per protein.
* All selected proteins showed high similarity to known bacterial proteins.

## 🗂️ Repository Structure
```
Bacterial-Genome-Analysis-using-BioPython-/
├── Final Project PCB - 03701.ipynb
├── Final Project Report PCB - 03701.pdf
├── data/
│   └── GCF_000063585.1_ASM6358v1_genomic.fna
├── outputs/
│   ├── all_orfs.csv
│   └── all_proteins.csv
└── README.md
```

## 🛠️ Tools & Libraries
* Python
* Biopython (SeqIO, Seq, ProtParam, BLAST modules)
* Jupyter Notebook
* NCBI BLASTp

## 👩‍💻 Author
Mrunmayee Wankhede \
MS-QBB @ CMU
