---
layout: page
title: Microbiome-16S-Pipeline
description: Complete workflow from raw reads to taxonomic level
img: assets/img/ChatGPT Image 2. Mai 2026, 10_10_05.jpg
importance: 4
category: work
---

### Goal
Adapted a 16S rRNA amplicon analysis workflow for microbiome profiling across more than 130 samples, with around 1,300 bacterial taxa detected per sample on average. 16S rRNA analysis is a standard method in clinical microbiology, used for bacterial identification and microbiome characterisation. The same approach was applied here to host-associated microbiomes, identifying dominant taxa and candidates with potential beneficial roles for the host.

### Strategy
The wide range of sample types meant that classifier choice and filter settings could not be picked once and reused. The workflow had to handle very different community structures consistently, while keeping the analysis reproducible across dozens of samples. NanoClass2, a Snakemake-based meta-classifier, served as the backbone, with downstream analysis built around it in R.

### Pipeline overview

    Input preparation. 
    Demultiplexed reads were concatenated per sample into single fastq.gz files, 
    then registered in a mapping CSV that defined run, sample, and file path for Snakemake.

---

    Quality filtering. 
    Reads were filtered with Chopper inside NanoClass2, with quality 
    and length thresholds set per sample type.

---

    Classifier selection. 
    A subsampled run with all eleven NanoClass2 classifiers was used to 
    compare performance on a representative subset before scaling up. Minimap2 and Kraken2 were 
    chosen for the full dataset.

---

    Classification at scale. 
    The full dataset was processed against the SILVA 138.1 SSU reference, 
    producing OTU and taxonomy tables per sample and classifier.

---

    Downstream analysis. OTU tables were imported into MicrobiomeAnalyst and R for diversity metrics, 
    statistical comparisons, and visualization of taxa that differed significantly between host groups.

To run Nanoclass2

    snakemake --cores 16 \
    -s <NanoClass2>/Snakefile \
    --configfile config.yaml \
    --use-conda --rerun-incomplete

### Tech stack
Snakemake · Bash · R · executed on an HPC environment


### Key takeaways
The benefit of a Snakemake-based workflow became obvious once the sample count grew: reproducibility, parallel execution, and clean separation between data and code. The harder part was the downstream side, deciding which differences between communities were biologically meaningful and which were artefacts of read depth or classifier choice. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Bildschirmfoto 2026-05-03 um 12.04.54.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
