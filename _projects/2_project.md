---
layout: page
title: wet lab 16S rRNA 
description: 16S rRNA Nanopore workflow from sample to sequencing data.
img: assets/img/Gemini_Generated_Image_vxbcq9vxbcq9vxbc Kopie2.jpg
importance: 2
category: work
giscus_comments: false
---

### Goal
Built a wet-lab workflow for 16S rRNA microbiome profiling that scales from environmental samples down to single bacterial colonies. 16S rRNA sequencing is a standard method in clinical microbiology, used for bacterial identification and microbiome analysis.The same approach was applied here to host-associated microbiomes, identifying the bacterial taxa that drive host growth and survival.


### Wet lab
Bead-based homogenisation followed by DNA extraction with the Zymo Quick-DNA kit, selected for time-efficient handling of large sample numbers. 16S amplification (PCR) and barcoding fed directly into Oxford Nanopore library preparation. In parallel, swab samples from selected hosts were used to isolate single bacterial colonies, which were amplified directly from picked colonies and sequenced by Sanger to confirm specific taxa at high resolution.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_4640.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_5873.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_6671.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Working under sterile conditions in the laminar flow hood. Bacterial isolates in liquid media and bacterial colonies on agar plates, ready for picking and single-colony isolation.
</div>

### Sequencing
16S rRNA amplicons were barcoded and prepared following the Oxford Nanopore protocol, then sequenced on the MinION using Flongle flow cells with 12 multiplexed samples per run. Sanger sequencing of single colonies served as a complementary high-confidence reference for individual isolates.

### Outcome
A reproducible workflow from sample preparation to sequencing for microbiome profiling, scaling from bulk samples to single colonies. Downstream bioinformatic analysis is covered in a separate project.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Bildschirmfoto 2023-11-27 um 18.47.37.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/Bildschirmfoto 2026-05-01 um 20.03.49.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    16S rRNA amplicons, multiplexed and sequenced for 24 hours on the Oxford Nanopore MinION with Flongle flow cells (12 samples per run).
</div>

### Stack
Oxford Nanopore (MinION, Flongle) · Sanger sequencing · 16S rRNA amplicon PCR · Zymo Quick-DNA extraction · multiplexed library preparation
