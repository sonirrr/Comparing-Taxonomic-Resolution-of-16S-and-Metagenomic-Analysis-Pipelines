# Quant-Bio-Project-2025

People: Ryleigh Griffin and Rishi Soni

Project Title: Reproducing 16S and Metagenomic Analyses for Method Comparison

Description
- When analyzing microbial communities, there are two main methods: 
-  16S rRNA sequencing sequences only the 16S rRNA genome sequences within a mixed community of bacteria. This approach yields data that is simple to analyze but is limited in its taxonomic resolution.
-  Metagenomic (shotgun) sequencing sequences the entire genome of bacteria within a community, requiring a more complicated and resource intensive analysis, but with higher taxonomic resolution.
- We will compare these two methods in a dataset that contains 16S and metagenomic reads for the same samples. 
- If time permits, we would like to reproduce a third method (MAG-based assembly) and conduct additional statistical analyses.


Example figures
- Stacked bar plots of community relative abundance
- PcoA plots for beta diversity
- Figure comparing the number of genera detectable by either/both 16S and shotgun (taken from Durazzi et. al)
- <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/60a99fde-384d-4de5-bb98-49484804d489" />


Dataset - 16s rRNA and metagenomic sequencing data for the chicken aecal microbiome
- From the SRA database - SRX26561860: Faecal Microbiome 53
- [Bioproject link] (https://www.ncbi.nlm.nih.gov/bioproject/1180228)
- Note: we are reaching out to the researcher who published this work to access the full dataset and the metadata to trace reads back to IDs
   - If they don't respond, we may need to pivot to a different dataset
   - We have backup data options and we believe these methods will work for all of them

Methods

Approach based on these two papers
- ["Comparison between 16S rRNA and shotgun sequencing data for the taxonomic characterization of the gut microbiota"] (https://www.nature.com/articles/s41598-021-82726-y)
- ["Profiling the diversity of the village chicken faecal microbiota using 16S rRNA gene and metagenomic sequencing data to reveal patterns of gut microbiome signatures"] (https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1487595/full)
- Metagenomic analysis detailed in this paper: ["A practical guide to amplicon and metagenomic analysis of microbiome data"] (https://academic.oup.com/proteincell/article/12/5/315/6724529)
- Chicken gut metagenome: ["The chicken gut metagenome and the modulatory effects of plant-derived benzylisoquinoline alkaloids"] (https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-018-0590-5)

Pipeline
- 16S: Data2 standard analysis
- Metagenomic (assembly-based method): as described in Liu et al.
- Reproducing the paper's MAG-based method is a reach goal

Software
- 16S: Data2 and PhyloSeq
- Metagenomic: Trimmomatic, Bowtie2, Kraken 2, assembler (metaSPAdes/MEGAHIT)
- Metagenomic (MAG-based): requires same tools as metagenomic analysis and MaxBin2, MetaBAT, CheckM
    - RAST/GTDB-TK for classifying and annotating MAGs

Goals

<10 hr goal 
- Reproduce 16S analysis using Data2 and Phyloseq pipeline
- Assembly-based metagenomic analysis
- Deliverable: stacked bar plot of microbial community relative abundance to be compared qualitatively between methods

Stretch goal #1
- MAG assembly
- Deliverable: additional stacked bar plot to be compared qualitatively between all three methods

Stretch goal #2
- Statistical analysis between methods as described in Durazzi et. al 


