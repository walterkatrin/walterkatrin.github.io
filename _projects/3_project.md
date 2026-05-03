---
layout: page
title: WGS-Analysis-Pipeline
description: End-to-end WGS pipeline from raw reads to variant detection.
img: assets/img/ChatGPT Image 2. Mai 2026, 10_04_27.jpg
importance: 3
category: work
---

### Project context
Whole genome sequencing of green algae (Chlorophyta), with the goal of expanding a sparse reference database and identifying polymorphisms and heteroplasmy. The dataset combined Nanopore long reads with Illumina short reads, allowing a hybrid approach. Detailed code and results are kept private until publication.

### Strategy
Working with a non-model organism and limited reference material meant that standard pipelines did not apply out of the box. Each step required testing tools, comparing outputs, and adapting the workflow to the specific data type, whether organellar, nuclear, or microbial. The pipeline below reflects the path that worked, after several that did not.

### Pipeline overview

    Quality cotrol. 
    Nanopore reads were filtered with NanoStat and NanoFilt, Illumina reads trimmed with Trimmomatic.
    A k-mer distribution check gave a first sense of genome size and contamination.

---

    Read filtering by component. 
    Organellar, nuclear, and microbial fractions were separated before assembly. 
    Mapping against curated NCBI references with Minimap2 and Samtools formed the backbone, 
    supported by KAT for eukaryotic filtering and the Metagenome-Atlas pipeline for the microbial fraction.

---

    Assembly and polishing. 
    Canu or SPAdes were used depending on the component, with hybrid input where applicable. 
    Nanopore-based assemblies were polished and reviewed in IGV alongside k-mer plots.

---

    Assembly quality assessment. 
    Completeness was checked with BUSCO against the matching lineage dataset before moving on.

---

    Annotation. 
    Features were annotated with GeSeq, BLAST, ARAGORN, tRNAscan-SE, and ORFfinder. 
    OGDraw visualized the organellar genome.

---

    Variant calling. BAM files from Samtools were passed into SNAPE-pooled, a Bayesian caller built for 
    pooled data. Called variants were cross checked in IGV to verify read-level support and rule out 
    mapping artefacts.

### Tech stack
Bash · Python · executed on an HPC environment


### Reflections
The hardest part was not running the tools, but choosing the right one for each step and recognizing when something was not adding up. Each setback pushed me to step back, try alternatives, and document what worked. Looking back, patience and persistence carried this project as much as the tools themselves.



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Bildschirmfoto 2026-05-03 um 11.31.12.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
