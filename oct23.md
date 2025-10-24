## New progress since last submission

-   Found a dataset: [Link](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE113701)
-   Paper: ["Altered gut microbial profile is associated with abnormal metabolism activity of Autism Spectrum Disorder"](https://pmc.ncbi.nlm.nih.gov/articles/PMC7524265/)
-   Attempted 16S RNA analysis using [DADA2](https://benjjneb.github.io/dada2/tutorial_1_8.html) pipeline
-   Using subset of data: 10 samples, 5 from control and 5 from autistic and all age matched
-   Uploaded this subset into github
-   Code for this in the markdown file "DADA2_Subset_Attempt1.md"
-   Metadata for 10 sample subset:

| File.Name | GSM.. | Sample.ID | Stage | Gender | Age | 16.RNA.sequencing | Metagenomic.sequencing |
|:--------|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|--------:|
| SRR9666822 | GSM3936619 | A54 | TD | Male | 3 | yes | Yes |
| SRR9666843 | GSM3936640 | A76 | TD | Male | 3 | yes | Yes |
| SRR9666845 | GSM3936642 | A78 | TD | Male | 3 | yes | Yes |
| SRR9666853 | GSM3936650 | A87 | TD | Male | 3 | yes | Yes |
| SRR9666855 | GSM3936652 | A89 | TD | Male | 3 | yes | Yes |
| SRR9666891 | GSM3936688 | B127 | Autism | Male | 3 | yes | Yes |
| SRR9666907 | GSM3936704 | B143 | Autism | Male | 3 | yes | Yes |
| SRR9666916 | GSM3936713 | B152 | Autism | Male | 3 | yes | Yes |
| SRR9666920 | GSM3936717 | B156 | Autism | Male | 3 | yes | Yes |
| SRR9666935 | GSM3936732 | B2 | Autism | Male | 3 | yes | Yes |

-   Stuck at cleaning reads: unsure whether they need barcode sequences removed

-   Uploaded Quality Profile for all ten samples into github (in the folder titled images) ![Quality Profile for all ten samples in subset]('/Users/cmdb/qb25-answers/project/images/Screenshot%202025-10-23%20at%209.52.22%20PM.png' "Quality Profile for all ten samples in subset")

-   BLAST shows 100% sequence alignment with known bacterial rRNA

    -   BLAST data in github as "FNN15U8S014-Alignment.txt"
    -   Indicates that there is no barcode sequence within this read, but we are not sure how to explain the quality control data

## Addressing Feedback

#### Title -- Refine title as you're "comparing" not just "reproducing" and specify what you're comparing (taxonomy profiling?); put title at the very top in place of "Quant-Bio-Project-2025"

New title: Comparing Taxonomic Resolution of 16S and Metagenomic Analysis Pipelines Repository name changed to this

#### Software -- Add links to relevant tutorials like <https://benjjneb.github.io/dada2> (it's DADA2 not data2)

Fixed this in the README file, added links throughout Did not include links for the metagenomics pipeline software because we expect to change these tools (see next response)

#### Goals -- Clarify metagenomic analysis (if Kraken2 is the main tool, it's not necessarily assembly-based)

We are using a different dataset from our original proposal. In the paper for dataset they use something called SOAPdenovo but it is unlikely that we will be able to reproduce this. Right now, we are focusing on the 16S analysis but we are looking for advice on our metagenomic analysis (we expect to build this pipeline from scratch).

#### Markdown -- Format "Description", "Methods", and other section headers using \## for heading 2, \### for heading 3, and so on to display larger, bold text

Fixed markdown format for headers, multiple sizes of headers now in README file
