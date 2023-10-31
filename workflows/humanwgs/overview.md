## Use Case

- Workflow for analyzing human PacBio whole genome sequencing (WGS) data

## Summary

The human WGS workflow performs read alignment, variant calling and phasing. Joint-calling of small variants and structural variants for cohorts and optional variant filtering and annotation is also available. The workflow can run using Azure, AWS, GCP, and HPC backends.

## Workflow Diagram
<img alt="Human WGS workflow diagram" width="480" src="workflows/main.graphviz.svg" />

## Tips and Tricks
**Mandatory Inputs**: JSON specifying the cohort information.

**Sample JSON**: [Template](workflows/input_template.json)

## PacBio Github Details

https://github.com/PacificBiosciences/wdl-humanwgs/blob/main/README.md
