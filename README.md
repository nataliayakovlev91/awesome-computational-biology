# Awesome Computational Biology [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated collection of databases, software, and papers related to computational biology.

> Computational biology involves the development and application of data-analytical and theoretical methods, mathematical modelling and computational simulation techniques to the study of biological, ecological, behavioural, and social systems. — [Wikipedia](https://en.wikipedia.org/wiki/Computational_biology)

---

## Overview

[![Resource Landscape Overview](docs/overview.png)](https://inoue0426.github.io/awesome-computational-biology/overview.html)

> Interactive version: [Resource Overview page](https://inoue0426.github.io/awesome-computational-biology/overview.html)  
> Regenerate the figure: `python scripts/generate_overview.py`

---

## GitHub Pages UI

Browse and search the resources via the [GitHub Pages UI](https://inoue0426.github.io/awesome-computational-biology/).

For treatment-response work, the [Dataset Explorer](https://inoue0426.github.io/awesome-computational-biology/dataset-explorer.html) compares curated cell-line, patient, and PDX datasets by year, sample type, perturbation metadata, matched pre/post availability, SMILES coverage, and clinical outcomes.

The [Method Explorer](https://inoue0426.github.io/awesome-computational-biology/method-explorer.html) compares drug-response and perturbation methods by task, molecular/context representation, unseen-drug support, dose/time conditioning, and patient transfer.

The [Foundation Model Explorer](https://inoue0426.github.io/awesome-computational-biology/foundation-explorer.html) compares foundation models by fine-grained modality, parameter count, pretraining scale, species, zero-shot support, weights/code availability, perturbation support, and spatial support.

The [Agent Explorer](https://inoue0426.github.io/awesome-computational-biology/agent-explorer.html) compares agentic AI systems by scientific domain, single- vs multi-agent architecture, tool/code execution, literature and web retrieval, omics and wet-lab support, autonomy, and human-in-the-loop design. The Agent Explorer table is sortable and supports domain, architecture, omics, code-execution, and year filters.

All explorer tables support sortable columns and focused filters for quick comparison, including a Recent (≥2025) toggle.

The Pages home screen also summarizes total resources, profiled datasets, methods, foundation models, agents, and the most common foundation-model modalities.

Chemical and genetic perturbation datasets can be filtered separately in the Dataset Explorer. Genetic screens can also be filtered by CRISPRi, CRISPRa, knockout, enhancer-targeting, combinatorial, or mixed perturbation modes, including mixed-resource collections.

The explorer also includes the eight perturbation datasets used in the Bison unseen-compound benchmark.

- Search matches `name`, `description`, `tasks`, `modalities`, and `tags`.
- The **Task**, **Modality**, and **Type** filters map directly to `tasks`, `modalities`, and `type` in `docs/data/resources.json`.
- Clicking badges on cards applies the corresponding filter.

---

## Table of Contents

- [Awesome Computational Biology](#awesome-computational-biology-)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [GitHub Pages UI](#github-pages-ui)
  - [Citation](#citation)
  - [Curation Criteria (Strict)](#curation-criteria-strict)
  - [Update & Link Rot Policy](#update--link-rot-policy)
  - [Data Schema & Contribution Workflow](#data-schema--contribution-workflow)
  - [Databases](#databases)
    - [scRNA](#scrna)
    - [Compound](#compound)
    - [Pathway](#pathway)
    - [Mass Spectra](#mass-spectra)
    - [Protein](#protein)
    - [Genome](#genome)
    - [Disease](#disease)
    - [Interaction](#interaction)
      - [Drug-Gene Interaction](#drug-gene-interaction)
      - [Drug (Cell Line) Response](#drug-cell-line-response)
      - [Chemical-Protein Interaction](#chemical-protein-interaction)
      - [Protein-Protein Interaction](#protein-protein-interaction)
      - [Knowledge Graph](#knowledge-graph)
      - [Gene Regulatory Network](#gene-regulatory-network)
    - [Clinical Trial](#clinical-trial)
  - [Benchmarks & Datasets](#benchmarks--datasets)
  - [API](#api)
  - [Preprocessing Tools](#preprocessing-tools)
  - [Machine Learning Tasks and Models](#machine-learning-tasks-and-models)
    - [Drug Discovery](#drug-discovery)
      - [Drug Response Prediction](#drug-response-prediction)
      - [Drug Perturbation](#drug-perturbation)
      - [Drug Repurposing](#drug-repurposing)
      - [Drug Target Interaction](#drug-target-interaction)
      - [Compound-Protein Interaction](#compound-protein-interaction)
      - [Molecular Generation](#molecular-generation)
    - [Protein Property Prediction](#protein-property-prediction)
    - [LLM for Biology](#llm-for-biology)
    - [Foundation Models](#foundation-models)
      - [Single-cell Foundation Models](#single-cell-foundation-models)
        - [Transcriptomics Foundation Models](#transcriptomics-foundation-models)
        - [Spatial Foundation Models](#spatial-foundation-models)
        - [Multi-Omics Foundation Models](#multi-omics-foundation-models)
        - [Domain Alignment](#domain-alignment)
      - [Compound Foundation Models](#compound-foundation-models)
        - [Compound Embedding](#compound-embedding)
      - [Protein Foundation Models](#protein-foundation-models)
        - [Pre-trained Embedding](#pre-trained-embedding)
        - [Protein Structure Prediction and Design](#protein-structure-prediction-and-design)
      - [Multi-Modal Foundation Models](#multi-modal-foundation-models)
      - [Genomics Foundation Models](#genomics-foundation-models)

---

## Databases

### scRNA

- [CZ CELLxGENE](https://cellxgene.cziscience.com/) — Single-cell dataset repository and interactive explorer from the Chan Zuckerberg Initiative.
- [Gene Expression Omnibus](https://www.ncbi.nlm.nih.gov/geo/) — Public functional genomics database.
- [Human Cell Atlas](https://www.humancellatlas.org/) — Open global atlas of all cells in the human body.
- [Single Cell PORTAL](https://singlecell.broadinstitute.org/single_cell) — Public database for single-cell RNA.
- [Single Cell Expression Atlas](https://www.ebi.ac.uk/gxa/sc/home) — Public database for single-cell RNA.

### Compound

- [PubChem](https://pubchem.ncbi.nlm.nih.gov/) — One of the largest chemical databases (compounds, genes, and proteins).
- [ChEBI](https://www.ebi.ac.uk/chebi/) — Database focused on small chemical compounds.
- [ChEMBL](https://www.ebi.ac.uk/chembl/) — Bioactive molecules with drug-like properties.
- [ChemSpider](http://www.chemspider.com/) — Chemical structure database.
- [DrugTargetCommons](https://drugtargetcommons.fimm.fi/) — Community platform for curating and integrating experimental bioactivity data across drugs and targets.
- [HMDB (Human Metabolome Database)](https://hmdb.ca/) — Comprehensive database of small molecule metabolites found in the human body.
- [KEGG COMPOUND](https://www.genome.jp/kegg/compound/) — Collection of small molecules and biopolymers.
- [LIPID MAPS](https://www.lipidmaps.org/databases/lmsd/overview) — Database of lipids.
- [Rhea](https://www.rhea-db.org/) — Database of chemical reactions.
- [DrugCentral](http://drugcentral.org/) — Online drug compendium with drug mode of action and indication information.
- [Drug Repurposing Hub](https://repo-hub.broadinstitute.org/repurposing#download-data) — Collections of drug repurposing data (drug, MoA, target, etc).
- [Therapeutic Target Database](https://idrblab.net/ttd/full-data-download) — Drug-target, target-disease, and drug-disease datasets.
- [ZINC ligand discovery database](https://zinc.docking.org/) — Free database of commercially-available compounds for virtual screening.

### Pathway

- [PathwayCommons](https://www.pathwaycommons.org/) — Database of pathways and interactions.
- [KEGG PATHWAY](https://www.genome.jp/kegg/pathway.html) — Collection of pathway maps.
- [WikiPathways](https://wikipathways.org/) — Database of biological pathways.
- [Reactome](https://reactome.org/) — Expert-curated, peer-reviewed pathway database with detailed reaction mechanisms.
- [BioCyc](https://biocyc.org/) — Collection of pathway/genome databases across thousands of organisms.
- [OmniPath](https://omnipathdb.org/) — Comprehensive resource integrating protein interactions, signaling pathways, gene regulatory networks, and miRNA targets from over 100 databases.
- [SIGNOR 2.0](https://signor.uniroma2.it/) — Database of causal signaling interactions and pathways, with signed and directed relationships between proteins.
- [MSigDB (Molecular Signatures Database)](https://www.gsea-msigdb.org/gsea/msigdb) — Curated gene sets derived from pathways and biological processes.

### Mass Spectra

- [MassBank](http://www.massbank.jp/) — Open source databases and tools for mass spectrometry reference spectra.
- [MoNA MassBank of North America](https://mona.fiehnlab.ucdavis.edu/) — Meta-database of metabolite mass spectra, metadata, and associated compounds.

### Protein

- [THE HUMAN PROTEIN ATLAS](https://www.proteinatlas.org/) — Comprehensive human protein database (cells, tissues, organs).
- [PROTEIN DATA BANK (PDB)](https://www.rcsb.org/) — 3D structures of proteins, nucleic acids, complexes.
- [UniProt](https://www.uniprot.org/) — Functional information on proteins.
- [AlphaFold Protein Structure Database](https://alphafold.ebi.ac.uk/api-docs) — 3D protein structure predictions.
- [RCSB Protein Data Bank](https://www.rcsb.org/) — Repository for structural data of biological molecules.
- [Critical Assessment of Structure Prediction (CASP)](https://predictioncenter.org/) — Assessing methods for protein structure prediction.
- [Uniclust](https://uniclust.mmseqs.com/) — Clustered protein sequence databases.
- [UniRef](https://www.uniprot.org/uniref/) — Non-redundant sequence database clustering UniProtKB entries at multiple sequence identity thresholds.
- [CATH database](https://www.cathdb.info/) — Hierarchical classification of protein domain structures.
- [SAbDab](https://opig.stats.ox.ac.uk/webapps/sabdab-sabpred/sabdab) — Structural Antibody Database containing all antibody structures in the PDB.
- [OADB (Observed Antibody Space Database)](http://opig.stats.ox.ac.uk/webapps/oas/) — Database of antibody sequences from immune repertoire sequencing.
- [InterPro](https://www.ebi.ac.uk/interpro/) — Protein families, domains, and functional sites database integrating 14 member databases including Pfam and PROSITE.
- [Pfam](https://www.ebi.ac.uk/interpro/entry/pfam/) — Database of protein families described by multiple sequence alignments and hidden Markov models.
- [NeXtProt](https://www.nextprot.org/) — Expert knowledge base on human proteins with deep functional annotation, complementary to UniProt.

### Genome

- [ENCODE](https://www.encodeproject.org/) — Encyclopedia of DNA Elements; regulatory and functional genomic elements across the genome.
- [Ensembl](https://www.ensembl.org/) — Genome browser and annotation database for vertebrate and other eukaryotic genomes.
- [Human Genome Resources at NCBI](https://www.ncbi.nlm.nih.gov/projects/genome/guide/human/index.shtml) — Database for genomics, proteomics, transcriptomics, and systems biology.
- [GenBank](https://www.ncbi.nlm.nih.gov/genbank/) — NCBI's database of genetic sequences.
- [UCSC Genome Browser](https://genome.ucsc.edu/) — UCSC's genome browser.
- [cBioPortal](https://www.cbioportal.org/) — Cancer genomics database; aggregating many patient datasets.
- [OncoKB](https://www.oncokb.org/) — Precision oncology knowledge base of cancer genes, variants, and therapeutic implications.
- [10x Genomics Dataset](https://www.10xgenomics.com/resources/datasets) — Collection of single-cell datasets.
- [The Genotype-Tissue Expression (GTEx)](https://gtexportal.org/home/) — Human gene expression and regulation resource.
- [Dependency Map (DepMap)](https://depmap.org/portal/) — CRISPR-Cas9 screens in cancer cell lines.
- [Catalogue Of Somatic Mutations In Cancer (COSMIC)](https://cancer.sanger.ac.uk/cosmic) — Resource on somatic mutations in cancers.
- [MGnify](https://www.ebi.ac.uk/metagenomics/) — Resource for metagenomic and metatranscriptomic data.
- [JASPAR](http://jaspar.genereg.net/) — Database of transcription factor binding profiles.
- [gnomAD](https://gnomad.broadinstitute.org/) — Genome Aggregation Database; genetic variation from large-scale sequencing projects.
- [Rfam](https://rfam.org/) — Database of RNA families with sequence alignments and consensus structures.
- [ROADMAP Epigenomics](http://www.roadmapepigenomics.org/) — Reference epigenome maps for 111 primary human cell types and tissues, including histone modifications, chromatin accessibility, and DNA methylation.
- [FANTOM5](https://fantom.gsc.riken.jp/5/) — Functional annotation of mammalian genome; comprehensive atlas of active enhancers, promoters, and transcription start sites across human and mouse cell types.

### Disease

- [KEGG DRUG](https://www.genome.jp/kegg/drug/) — Comprehensive, approved drug information.
- [DrugBank](https://go.drugbank.com/) — Database of drugs and targets (University of Alberta).
- [DisGeNET](https://www.disgenet.org/) — Database of gene-disease associations integrating expert-curated and GWAS data.
- [OMIM (Online Mendelian Inheritance in Man)](https://www.omim.org/) — Comprehensive database of human genes and genetic disorders.
- [Open Targets Platform](https://platform.opentargets.org/) — Systematic target identification and prioritization platform integrating genetics, genomics, and drug data for drug discovery.
- [Human Phenotype Ontology (HPO)](https://hpo.jax.org/) — Standardized vocabulary of phenotypic abnormalities in human disease, linking genes, variants, and clinical features.
- [DISEASES](https://diseases.jensenlab.org/) — Gene–disease association database integrating evidence from text mining, curated databases, and experimental data.

### Interaction

#### Drug-Gene Interaction

- [DGIdb](https://www.dgidb.org/) — Drug-gene interactions and the druggable genome.
- [Comparative Toxicogenomics Database](http://ctdbase.org/) — Chemical-gene interactions, chemical-disease and gene-disease associations, chemical-phenotype associations.
- [SNAP](https://snap.stanford.edu/biodata/datasets/10002/10002-ChG-Miner.html) — Dataset of drug-gene interactions.

#### Drug (Cell Line) Response

- [NCI60](https://dtp.cancer.gov/discovery_development/nci-60/) — Focuses on 60 cancer cell lines and many drugs.
- [Genomics of Drug Sensitivity in Cancer (GDSC)](https://www.cancerrxgene.org/) — Drug sensitivity for ~1000 human cancer cell lines and hundreds of compounds.
- [Cancer Cell Line Encyclopedia](https://sites.broadinstitute.org/ccle/) — Database of ~1000 cancer cell lines.
- [CellMiner Cross Database (CellMinerCDB)](https://discover.nci.nih.gov/cellminercdb/) — Integrates multiple cancer cell line databases.

#### Chemical-Protein Interaction

- [STITCH](http://stitch.embl.de/) — Chemical-protein interactions.
- [BindingDB](https://www.bindingdb.org/rwd/bind/index.jsp) — Compounds and target database.
- [Davis kinase inhibitors DB](http://staff.cs.utu.fi/~aijrinas/dti/) — Experimental kinase inhibitor binding affinity dataset for protein–ligand interaction research.
- [Kinase Inhibitor Bioactivity Data (KIBA)](https://janeliascicomp.github.io/KIBA/) — Integrated bioactivity scores for kinase inhibitors combining Ki, Kd, and IC50 measurements.
- [PDBBind](https://www.pdbbind-plus.org.cn/) — Binding affinity data for biomolecular complexes.

#### Protein-Protein Interaction

- [STRING](https://string-db.org/) — PPI networks for multiple organisms.
- [BioGRID](https://thebiogrid.org/) — Protein, genetic, and chemical interactions.
- [HIPPIE](http://cbdm-01.zdv.uni-mainz.de/~mschaefer/hippie/) — Human protein-protein interaction database.
- [IntAct](https://www.ebi.ac.uk/intact/home) — Open-source molecular interaction database and analysis system from EMBL-EBI.

#### Knowledge Graph

- [Drug Mechanism Database (DrugMechDB)](https://github.com/SuLab/DrugMechDB/tree/2.0.1) — Mechanisms of action from drug to disease.
- [DRKG](https://github.com/gnn4dr/DRKG) — Large-scale biological knowledge graph for drug discovery.
- [Hetionet](https://github.com/hetio/hetionet) — Heterogeneous network integrating genes, diseases, drugs, pathways, and more.
- [PrimeKG](https://github.com/mims-harvard/PrimeKG) — Multi-modal precision medicine knowledge graph integrating clinical, genetic, and drug data.

#### Gene Regulatory Network

- [TRRUST v2](https://www.grnpedia.org/trrust/) — Manually curated database of human and mouse transcriptional regulatory interactions between transcription factors and their target genes, expanded with literature-derived evidence.
- [RegNetwork](http://www.regnetworkweb.org/) — Database of gene regulatory networks covering transcription factor–target gene and miRNA–gene interaction data across multiple species.
- [miRBase](https://www.mirbase.org/) — Reference repository for microRNA gene annotations, sequences, and experimentally validated targets.

### Clinical Trial

- [ClinicalTrials.gov](https://clinicaltrials.gov/) — Privately and publicly funded clinical studies.
- [ICD10](https://icd.who.int/browse10/2019/en) — International Classification of Diseases, 10th revision.
- [EU Drug Regulating Authorities Clinical Trials DB (EudraCT)](https://eudract.ema.europa.eu/) — European clinical trial database.
- [MIMIC-IV](https://mimic.mit.edu/) — Freely accessible critical care database.

---

## Benchmarks & Datasets

### Drug Response & Perturbation

- [BEAT AML](https://biodev.github.io/BeatAML2/) — Functional ex vivo drug sensitivity measurements paired with genomics for acute myeloid leukemia.
- [Cancer Therapeutics Response Portal (CTRP)](https://portals.broadinstitute.org/ctrp/) — Drug sensitivity profiles across ~900 cancer cell lines for >400 compounds.
- [Chem-PerturBridge](https://github.com/theislab/Chem-PerturBridge) — Harmonized compendium and processing pipelines for small-molecule perturbation transcriptomics across heterogeneous assays and gene panels.
- [GSE191127 Breast Cancer Pre/Post Chemotherapy](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE191127) — Bulk RNA-seq and genomics from matched pre- and post-neoadjuvant chemotherapy breast tumors with treatment outcomes.
- [Genomics of Drug Sensitivity in Cancer (GDSC)](https://www.cancerrxgene.org/) — Drug sensitivity for ~1000 human cancer cell lines and hundreds of compounds.
- [JUMP Cell Painting Datasets](https://github.com/jump-cellpainting/datasets) — Consortium-scale cell imaging perturbation datasets (chemical and genetic) for phenotypic profiling and drug discovery research.
- [LINCS L1000](https://lincsproject.org/LINCS/tools/workflows/find-the-best-place-to-obtain-the-lincs-l1000-data) — Gene expression profiles (978 landmark genes) for >20,000 chemical and genetic perturbations across cell lines.
- [LINCS L1000 Phase 1](https://github.com/theislab/Chem-PerturBridge) — Phase-1 L1000 benchmark view used by Bison with 692,787 profiles, 9,233 molecules, 70 contexts, and 978 landmark genes.
- [LINCS L1000 Phase 2](https://github.com/theislab/Chem-PerturBridge) — Phase-2 L1000 benchmark view used by Bison with 333,263 profiles, 1,760 molecules, 30 contexts, and 978 landmark genes.
- [MIX-Seq](https://www.nature.com/articles/s41467-020-17440-w) — Multiplexed single-cell transcriptional profiling of chemical and genetic perturbation responses across pools of cancer cell lines.
- [NCI60](https://dtp.cancer.gov/discovery_development/nci-60/) — Drug sensitivity benchmark across 60 diverse human cancer cell lines.
- [Novartis Perturbation Dataset](https://github.com/theislab/Chem-PerturBridge) — Large chemical perturbation transcrip