# CRISPR/Cas9 Screen for TOP2 Inhibitor Resistance (ETP & ICRF)
Analysis of CRISPR/Cas9-based screen to identify factors conferring resistance to Topoisomerase II (TOP2) inhibitors.

## Project overview

CRISPR/Cas9-based screens were carried out to find factors sensitizing U2OS cells to two mechanistically different TOP2 inhibitors: etoposide (ETP) and ICRF-193 (ICRF). The details on how the screen was performed can be found in https://pubmed.ncbi.nlm.nih.gov/40516529/.
The resulting samples were processed by the sequencing facilites and total read counts were generated through MAGeCK. In this project we will focus in the analysis of these files, highlighting the factors that were followed up in the rest of the study mentioned above.

## Tools

- **Python (v3.10+)**
- **Packages**: Pandas, Matplotlib, NumPy
- **Platform**: Google Colab
- **Analysis algorithm**: [DruZ](https://pubmed.ncbi.nlm.nih.gov/31439014/) (Python implementation)

## Analysis

The MAGeCK-generated `.txt` files (from the CRISPR screen readout) were analyzed using two complementary approaches:

1. **DrugZ-based scoring**  
   A refined method for identifying synthetic lethal interactions using negative selection scores.  
   [Colab notebook →](https://colab.research.google.com/drive/1lwvopBVo3I95uonq1b5zJKm4c4aye6lG#scrollTo=6yOH9YbR4gW4)

2. **Basic Python analysis**  
   Custom Python-based summary statistics, visualizations, and thresholds to identify sensitizing hits.  
   [Colab notebook →](https://colab.research.google.com/drive/199dA122dQar-znkweMBH1Oon_qSPy97b?usp=sharing)

## Results

- A normZ threshold of **< -3** was used to define genes that sensitize cells to TOP2 inhibitors.
- **ZNF451** and **TDP2**, two known repair factors for trapped TOP2 complexes, were among the top sensitizers — validating the screen.
- A limited number of sgRNAs sensitized cells to both ETP and ICRF treatment.
- The previously uncharacterized gene **CRAMP1** scored in both the ETP and ICRF datasets.
- Several **H1 histone isoforms** also showed sensitization effects, consistent with findings in the referenced publication.

