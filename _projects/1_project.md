---
layout: page
title: wet lab WGS
description: From Sample Extraction to Sequencing
img: assets/img/Labor_1.jpg
importance: 1
category: work
related_publications: false
---

### Goal 
Built a workflow from sample preparation to sequencing for a non-model organism, where no validated protocol existed in the group. The workflow transfers directly to other non-model species and is documented so colleagues without a background in long-read sequencing can apply it independently.
The chosen organism, Caulerpa, produces bioactive compounds studied in cancer research, which makes reference genomes for this genus relevant beyond evolutionary genetics. 

### Wet lab
Maintained live cultures under controlled temperature and light conditions, and processed silica-preserved samples from collaborators where only minimal tissue was available. DNA was extracted using a CTAB protocol that I adapted for this tissue type, chosen over commercial kits because CTAB reliably removes polysaccharides and secondary metabolites and yields the high-molecular-weight DNA that long-read sequencing requires.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Bildschirmfoto 2026-05-02 um 13.25.12.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Bildschirmfoto 2026-05-02 um 13.25.23.jpg
" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Bildschirmfoto 2026-05-02 um 13.27.06.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Wet-lab workflow: tissue homogenization, CTAB-based DNA extraction adapted for Caulerpa, followed by quality control via gel electrophoresis (fragment integrity) and Nanodrop (concentration and 260/280, 260/230 purity ratios) to ensure clean, high-molecular-weight DNA for downstream Nanopore library preparation.
</div>

### Sequencing
Library preparation and barcoding followed the Oxford Nanopore protocol; whole-genome sequencing was performed on the MinION using flow cells. Based on expected genome size, I calculated the optimal sample number per flow cell and scaled multiplexing from 3 to 24 barcodes per run with no loss in data quality, significantly reducing per-sample sequencing cost.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_0193.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_7640.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Whole-genome sequencing run on the Oxford Nanopore MinION: 10 µl of multiplexed library loaded onto a flow cell, monitored in real time via MinKNOW for pore activity, read-length distribution, and total yield over the 48-hour run.
</div>


### Outcome
A reproducible workflow from sample preparation to sequencing. Sequence analysis is covered in a separate project.


### Stack
Oxford Nanopore (MinION) · CTAB DNA extraction · multiplexed library preparation · controlled algal culturing.
