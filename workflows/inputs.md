## JSON Template

```
{
  "humanwgs.cohort": {
    "cohort_id": "String",
    "samples": [
      {
        "sample_id": "String",
        "movie_bams": "Array[File]",
        "sex": "String?",
        "affected": "Boolean",
        "father_id": "String?",
        "mother_id": "String?"
      }
    ],
    "phenotypes": "Array[String]"
  },
  "humanwgs.reference": {
    "name": "String",
    "fasta": {
      "data": "File",
      "data_index": "File"
    },
    "chromosomes": "Array[String]",
    "chromosome_lengths": "File",
    "tandem_repeat_bed": "File",
    "trgt_tandem_repeat_bed": "File",
    "hificnv_exclude_bed": {
        "data": "File",
        "data_index": "File"
      },
    "hificnv_expected_bed_male": "File",
    "hificnv_expected_bed_female": "File",
    "gnomad_af": "File",
    "hprc_af": "File",
    "gff": "File",
    "population_vcfs": [
      {
        "data": "File",
        "data_index": "File"
      }
    ]
  },
  "humanwgs.slivar_data": {
    "slivar_js": "File",
    "hpo_terms": "File",
    "hpo_dag": "File",
    "hpo_annotations": "File",
    "ensembl_to_hgnc": "File",
    "lof_lookup": "File",
    "clinvar_lookup": "File"
  },
  "humanwgs.deepvariant_version": "String (optional)",
  "humanwgs.deepvariant_model": "WomCompositeType {\n model -> WomCompositeType {\n data -> File\ndata_index -> File \n}\nmetadata -> File \n}? (optional)",
  "humanwgs.pbsv_call_mem_gb": "Int (optional)",
  "humanwgs.glnexus_mem_gb": "Int (optional)",
  "humanwgs.run_tertiary_analysis": "Boolean (optional, default = false)",
  "humanwgs.backend": "String ['GCP', 'Azure', 'AWS', or 'HPC']",
  "humanwgs.zones": "String? (optional); required if backend is set to 'GCP' or 'AWS'",
  "humanwgs.aws_spot_queue_arn": "String? (optional); required if backend is set to 'AWS'",
  "humanwgs.aws_on_demand_queue_arn": "String? (optional); required if backend is set to 'AWS'",
  "humanwgs.preemptible": "Boolean"
}
```

## PacBio Github Details
https://github.com/PacificBiosciences/wdl-humanwgs/blob/main/README.md
