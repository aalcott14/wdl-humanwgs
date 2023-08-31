## Use Case

- Workflow for analyzing human PacBio whole genome sequencing (WGS) data

## Summary

The human WGS workflow performs read alignment, variant calling and phasing. Joint-calling of small variants and structural variants for cohorts and optional variant filtering and annotation is also available. The workflow can run using Azure, AWS, GCP, and HPC backends.

## Workflow Diagram
![Human WGS workflow diagram](workflows/main.graphviz.svg "Human WGS workflow diagram")

## Tips and Tricks
**Mandatory Inputs**: JSON specifying the cohort information.

**Sample JSON**: [Template](workflows/input_template.json)
