## Use Case

- Workflow for analyzing human PacBio whole genome sequencing (WGS) data

## Summary

The human WGS workflow performs read alignment, variant calling and phasing. Joint-calling of small variants and structural variants for cohorts and optional variant filtering and annotation is also available. The workflow can run using Azure, AWS, GCP, and HPC backends

## Workflow Diagram
<img src="https://raw.githubusercontent.com/PacificBiosciences/HiFi-human-WGS-WDL/main/workflows/main.graphviz.svg" width="480"/>

## Tips and Tricks
**Mandatory Inputs**: JSON specifying the cohort information.

**Sample JSON**: [Template](workflows/input_template.json)

## PacBio Github Details

https://github.com/PacificBiosciences/wdl-humanwgs/blob/main/README.md
