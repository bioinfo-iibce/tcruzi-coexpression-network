# Gene Co-Expression Network Analysis in *Trypanosoma cruzi*

This repository contains the code and data used to construct and analyze gene coexpression networks in *Trypanosoma cruzi* as part of our manuscript:

**Exploring a gene co-expression network throughout the *Trypanosoma cruzi* life cycle**  
Lucas Inchausti, Álvaro Martín, Leticia Pérez-Díaz, Beatriz Garat, María Ana Duhagon, José Sotelo-Silveira, Javier G. De Gaudenzi*, Pablo Smircich*
[2025]

We performed gene co-expression network (GCN) analysis using transcriptomic data spanning all life-cycle stages of *Trypanosoma cruzi*, offering insights into the coordinated expression patterns of functionally linked gene groups. We examined the global network properties, identifying overrepresented functional pathways and highly connected hub genes. Additionally, we explored potential regulatory mechanisms within each module, focusing on conserved motifs in the 3’ untranslated regions (3’UTRs) of co-expressed genes.

🔹 Note: This repository contains only the code and data used for the construction and exploration of the gene coexpression network.


---

## 📁 Repository Structure

```text
.
├── data/                         # Input data (expression matrices, traits)
│   ├── perfiles_expresion_rlog.csv
│   ├── perfiles_expresion_rlog_centrada.csv
│   └── traits.csv
├── scripts/                      # All analysis R scripts
├── results/
│   ├── dissTOM.csv               # Dissimilarity matrix (TOM)
│   ├── all_modules_trait_relationships.png
│   ├── submodules_trait_relationships.png
│   ├── plots_profiles_segmented/
│   ├── plots_profiles_correlation/
│   ├── genes_by_module_correlation/
│   ├── resultados_GO_ab/        # GO enrichment per module and correlation sign
│   ├── grafo_genes.png          # Hub gene network
│   ├── subgrafo_*               # Subnetworks around selected genes
│   └── vecinos_por_gen/         # Tables with neighbors of hub genes
├── top650_hubgenes.txt          # List of hub genes used in network visualization
├── gene2go_df.rds               # GO annotation (TERM2GENE)
├── go_names_df.rds              # GO term names (TERM2NAME)
└── README.md

```

## 📦 Required R packages

```text
install.packages(c("ggplot2", "dplyr", "tidyr", "tibble", "purrr", "igraph", "ggraph", "viridis"))
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(c("CEMiTool", "WGCNA", "clusterProfiler", "enrichplot", "rtracklayer", "ontologyIndex"))
```


## 📂 Input Files
```text
- perfiles_expresion_rlog.csv -> RLOG-normalized expression matrix

- perfiles_expresion_rlog_centrada.csv -> Centered matrix for profile plots

- traits.csv -> Metadata for samples (used for correlation)

- top650_hubgenes.txt -> List of hub genes for subnetworks visualization
```

## 📈 Output Highlights
```text
- Module-trait heatmaps: correlations between module eigengenes and traits.

- Profile plots: expression dynamics across conditions.

- GO enrichment: functional annotation per module and correlation sign.

- Gene networks: submodule graphs of hub gene interactions.

- Neighbor tables: CSVs with top coexpressed neighbors.
```

## 📣 Citation

If you use this code, please cite:

*Exploring a gene co-expression network throughout the Trypanosoma cruzi life cycle* 
Lucas Inchausti, Álvaro Martín, Leticia Pérez-Díaz, Beatriz Garat, María Ana Duhagon, José Sotelo-Silveira, Javier G. De Gaudenzi*, Pablo Smircich*
[2025]
DOI: [Coming soon]
