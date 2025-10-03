# Quant-Bio-Project-2025

People: Ryleigh Griffin and Rishi Soni

Project Title:

Description:
16S sequencing used V3-V4 region (atypical, will affect analysis down the line?)

Example figures: 

Dataset - 16s rRNA and metagenomic sequencing data for the chicken aecal microbiome
From the SRA database - SRX26561860: Faecal Microbiome 53
[Bioproject link] (https://www.ncbi.nlm.nih.gov/bioproject/1180228)
Note: we are reaching out to the researcher who published this work to access the full dataset and the metadata to trace reads back to IDs
If they don't respond, we may need to pivot to a different dataset
We have backup data options and we believe these methods will work for all of them

Methods
Approach based on these two papers
- ["Comparison between 16S rRNA and shotgun sequencing data for the taxonomic characterization of the gut microbiota"] (https://www.nature.com/articles/s41598-021-82726-y)
- ["Profiling the diversity of the village chicken faecal microbiota using 16S rRNA gene and metagenomic sequencing data to reveal patterns of gut microbiome signatures"] (https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1487595/full)
Metagenomic analysis detailed in this paper: ["A practical guide to amplicon and metagenomic analysis of microbiome data"] (https://academic.oup.com/proteincell/article/12/5/315/6724529)
Chicken gut metagenome: ["The chicken gut metagenome and the modulatory effects of plant-derived benzylisoquinoline alkaloids"] (https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-018-0590-5)

Pipeline
- 16S: Data2 standard analysis
- Metagenomic (assembly-based method): 
- Reproducing the Nature paper's MAG-based method is a reach goal

Software
- 16S: Data2 and PhyloSeq
- Metagenomic: Trimmomatic, Bowtie2, Kraken 2, assembler (metaSPAdes/MEGAHIT)
- 

Goals/Timeline
<10 hr goal - Reproduce 16S analysis using Data2 and Phyloseq pipeline
Reach goal: MAG assembly (p


Reach goals: MAG alignment
