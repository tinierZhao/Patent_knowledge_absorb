# Highly Cited Prior Patents and Focal Patent Diffusion

This repository contains the code and documentation for the study **"Highly Cited Prior Patents and Focal Patent Diffusion: The Moderating Role of Disruptiveness."**

## Overview

The study examines whether focal patents that build on highly cited prior patents achieve stronger subsequent diffusion, and whether this relationship depends on the disruptiveness of the cited prior patent. It combines patent-citation data with text-based semantic similarity measures to distinguish recognized, consolidating knowledge sources from recognized but disruptive ones.

## Data and study design

The analysis uses **7,955,822 USPTO utility patents** granted between **1980 and 2024**.

- **Focal patents:** patents whose subsequent diffusion is assessed.
- **Closest cited prior patent:** for each focal patent, the cited patent with the highest cosine similarity based on PatentSBERTa embeddings of patent titles and abstracts.
- **Highly cited prior patent:** a cited prior patent ranked in the top 5% of five-year forward citations within the same grant year and WIPO technology field.
- **Disruptiveness:** the disruption index, following Wu, Wang, and Evans (2019), which captures whether a patent redirects later technological development away from, or reinforces, prior technological trajectories.
- **Subsequent diffusion:** measured using five-year forward citations to focal patents.

The empirical analysis estimates the association between highly cited prior patents and focal-patent diffusion, with prior-patent disruptiveness as a moderator. Models include patent-level controls and grant-year and technology-field fixed effects.

## Data availability

The underlying patent records are publicly available from the United States Patent and Trademark Office (USPTO). Raw patent data and derived intermediate files are not distributed in this repository because of their size. Users should download the relevant source data independently and place them in a local data directory before running the replication code.

Please do not upload raw data, temporary files, or files containing restricted information to a public fork.

## Suggested repository structure

```text
code/       data preparation, variable construction, and estimation scripts
data/       USPTO
output/     
docs/       supplementary documentation
```

## Reproducibility

To reproduce the analysis after the code is uploaded:

1. Download the required USPTO patent records and store them locally.
2. construct citation links, patent-text embeddings, and analytical variables.
3. Run the estimation scripts to reproduce the descriptive analyses, regression tables, and figures.

Specific software requirements and the execution order will be documented with the released scripts.

## Citation

If you use this repository, please cite the associated paper:

> 

## Contact


