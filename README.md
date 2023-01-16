
# Differential Expression RNA-Seq Workflow

This snakemake workflow runs differential expression analysis from RNA-Seq raw reads through to the plotting of differentially expressed genes. This includes:

- Initial read quality assessment
- Read quality trimming
- Followup quality assessment
- Read alignment to reference
- Generation of count data
- Saturation Curves + PCA plots
- Handles high and low abundance counts
- Volcano plots
- Means to further investigate genes of interest

## Requirements

### Software
- A Snakemake installation of version ? or higher
- Conda installation

### Data
- Compressed Reference genome (fasta file with extension .fna.gz or .fa.gz)
- Associated annotation file (.gff or .gtf extension)
- Compressed paired end illumina reads (extension fastq.gz or fq.gz)

## Setup

### Get your reads/fastq data

Copy or place all of your fastq data into the `0_data/fastq/` directory.
Data can be moved from one location to another using the `mv` command (example below moves a file called file.fq.gz from its current location to a folder called /newspot)

```
mv file.fq.gz newspot/
```

### Populate the config file


