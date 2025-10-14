# 🧬 Metagenome-Assembled Genomes from Chicken Housing Environments
### Bioinformatics Analysis Pipeline

This repository contains the complete bioinformatics workflow used for the reconstruction, quality assessment, taxonomic classification, and functional characterization of metagenome-assembled genomes (MAGs) derived from the layer chicken housing environment.

The pipeline integrates assembly, binning, genome quality evaluation, taxonomic assignment, functional and antimicrobial-resistance (AMR) annotation, and data visualization. It enables a detailed understanding of the ecological and functional roles of microbial communities, focusing on antimicrobial resistance, nutrient cycling, and microbial interactions within poultry barn ecosystems.

---

## 🧩 Pipeline Overview

```mermaid
flowchart TD
    A[Raw shotgun reads] --> B[Quality Control<br/>FastQC]
    B --> C[De novo Assembly<br/>MEGAHIT]
    C --> D[Assembly Quality Check<br/>QUAST]
    D --> E[Binning<br/>MetaBAT2]
    E --> F[Quality Assessment<br/>CheckM]
    F --> G[Taxonomic Classification<br/>GTDB-Tk]
    G --> H[Functional Annotation<br/>EggNOG-mapper]
    H --> I[ARG Detection<br/>AMRFinderPlus]
    I --> J[Plasmid & Mobility Analysis<br/>MOB-suite]
    J --> K[Correlation & Network Analysis<br/>R igraph and ggraph]
    K --> L[Visualization & Integration<br/>R ggplot2 and pheatmap]
    L --> M[Final Results<br/>MAG taxonomy, functions, ARGs, pathways]

