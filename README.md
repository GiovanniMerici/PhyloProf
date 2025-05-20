# Phylogenetic Profiling and Visualization of Gene Presence/Absence

This Colab-based tool automates the process of identifying the phylogenetic distribution of one or more genes across a user-defined set of genomes. It generates a presence/absence matrix and visualizes it alongside a taxonomic tree as a heatmap.

## 🚀 What it does

- 🧬 Accepts a set of protein sequences
- 🌍 Accepts a list of target organisms (or a short default list is available) 
- ⬇️ Automatically downloads reference genomes from NCBI
- 🧪 Runs `BLASTP` searches to detect gene presence
- 📊 Builds a presence/absence matrix
- 🌳 Constructs a taxonomic tree from NCBI
- 🎨 Plots a heatmap aligned to the tree

All of this is performed entirely in Google Colab — no local installation required.

---

## 📥 Input Files

You need to upload two files to the Colab environment before running the notebook:

### 1. `query_genes.txt` — Gene input file (FASTA or UniProt IDs)

This file can be provided in either of the following formats:

#### Option A – Protein FASTA file

A standard FASTA file containing one or more amino acid sequences. Each entry should have:
- A header line beginning with `>gene_name`
- The sequence on one or more lines

#### Option B – List of UniProt IDs

A plain text file with one UniProt ID per line. The notebook will automatically download the corresponding protein sequences.

### 2. `organism_list.txt` — Target species list

A plain text file with one organism name per line. These should be recognized species from NCBI.

📦 Don't have a list?  
If no file is uploaded, the notebook will fall back to a default list of representative organisms, which includes a few common model species across different branches of life.



## 📓 How to use it

👉 Open the notebook in Colab

Steps:

1. Upload `query_genes.txt` and `organism_list.txt`
2. Run the notebook cells
3. Collect outputs:
   - CSV matrix: `profile.csv`
   - Heatmap figure: `tree_and_heatmap.png`
