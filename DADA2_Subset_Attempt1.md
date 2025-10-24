R Notebook
================

Here I am attempting to use a subset of 16SRNA data samples from our
larger dataset. All of these samples have a paired metagenomic
sequencing file associated with them. We will eventually compare
outputs.

\#Sample IDs:

``` r
metadata <- read.csv("/Users/cmdb/Documents/Subset_metadata.csv")
print(metadata)
```

\#DADA2:

``` r
library(dada2); packageVersion("dada2")
```

    ## [1] '1.34.0'

``` r
path <- "/Users/cmdb/Documents/Subset QB2025 16S Samples/"
list.files(path)
```

    ##  [1] "SRR9666822.fastq" "SRR9666843.fastq" "SRR9666845.fastq" "SRR9666853.fastq" "SRR9666855.fastq" "SRR9666891.fastq"
    ##  [7] "SRR9666907.fastq" "SRR9666916.fastq" "SRR9666920.fastq" "SRR9666935.fastq"

``` r
#I think all of our data is single end reads so I will treat all samples as F reads
fnFs <- sort(list.files(path, full.names = TRUE))
# Extract sample names, assuming filenames have format: SAMPLENAME_XXX.fastq
sample.names <- sapply(strsplit(basename(fnFs), "\\."), `[`, 1)
glimpse(sample.names)
```

    ##  chr [1:10] "SRR9666822" "SRR9666843" "SRR9666845" "SRR9666853" "SRR9666855" "SRR9666891" "SRR9666907" "SRR9666916" ...

``` r
plotQualityProfile(fnFs[1:10])
```

![](DADA2_Subset_Attempt1_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

This indicates to me that maybe the reads are not trimmed.

From the tutorial: “In gray-scale is a heat map of the frequency of each
quality score at each base position. The median quality score at each
position is shown by the green line, and the quartiles of the quality
score distribution by the orange lines. The red line shows the scaled
proportion of reads that extend to at least that position (this is more
useful for other sequencing technologies, as Illumina reads are
typically all the same length, hence the flat red line).”

Here we clearly see that our red line is not at all flat. It drops
steeply at around 250 bp. The proportion of reads that are longer than
250 bp seems very low. I am not sure what these reads are or what to do
with them.
