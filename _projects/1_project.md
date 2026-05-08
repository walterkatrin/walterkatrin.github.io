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
Generate high-quality whole-genome sequencing data for the green macroalga Caulerpa as the basis for an organellar reference genome database and identification of polymorphisms. Caulerpa is a non-model organism with no established sequencing protocol in our group, so the entire pipeline had to be built end-to-end.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/bafe93bd-96b9-4958-9eea-e72925a05a3a Kopie.JPG" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_4554.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_6622.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
      Caulerpa is a single-celled organism that can grow over a metre in size while remaining one giant cell with multiple nuclei. Despite its unicellular nature, it forms remarkably diverse morphologies (grape-, feather-, and leaf-like) and make it a research target across biomedicine, biotech, and the food industry.
</div>

### Wet lab
Maintained live cultures under controlled temperature and light conditions, and processed silica-preserved samples from collaborators where only minimal tissue was available. DNA was extracted using a CTAB protocol that I adapted specifically for Caulerpa tissue, chosen over commercial extraction kits because CTAB removes polysaccharides and secondary metabolites typical of macroalgae far more reliably and yields the high-molecular-weight DNA that long-read sequencing requires.

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
Library preparation and barcoding followed the Oxford Nanopore protocol; whole-genome sequencing was performed on the MinION using flow cells. Based on expected total genome size, I calculated the optimal number of samples per flow cell and scaled multiplexing from 3 to 24 barcodes per run with no loss in data quality, significantly reducing per-sample sequencing cost.

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
A reproducible end-to-end workflow from culture to sequencing-ready data, expanding a genus for which only 13 complete chloroplast genomes are currently available worldwide. The workflow has the potential to at least double this reference base and is transferable to other non-model marine organisms.


### Stack
Oxford Nanopore (MinION) · CTAB DNA extraction · multiplexed library preparation · controlled algal culturing.
