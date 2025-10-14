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
