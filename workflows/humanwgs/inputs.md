## How to create input JSON
1. Copy template below to a new `.json` file
2. Update `humanwgs.cohort` section (use the template below as a reference)
3. Save `.json` file to Form Bio project

## JSON Template

```
{
  "humanwgs.cohort": {
    "cohort_id": "HG005-trio",
    "samples": [
      {
        "sample_id": "HG005",
        "movie_bams": [
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG005/m64017_200723_190224.hifi_reads.bam",
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG005/m64017_200730_190124.hifi_reads.bam"
        ],
        "sex": "MALE",
        "affected": true,
        "father_id": "HG006",
        "mother_id": "HG007"
      },
      {
        "sample_id": "HG006",
        "movie_bams": [
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG006/m64017_191209_211903.hifi_reads.bam",
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG006/m64017_191211_182504.hifi_reads.bam"
        ],
        "sex": "MALE",
        "affected": false
      },
      {
        "sample_id": "HG007",
        "movie_bams": [
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG007/m64017_191216_194629.hifi_reads.bam",
          "formbio://myOrg/myProj/pacbio/sample/small_tests_chr6p23/HG007/m64017_191218_164535.hifi_reads.bam"
        ],
        "sex": "FEMALE",
        "affected": false
      }
    ],
    "phenotypes": [
      "HP:0000001"
    ]
  },
  "humanwgs.reference": {
    "name": "GRCh38",
    "fasta": {
      "data": "gs://pacbio-wdl/dataset/GRCh38/human_GRCh38_no_alt_analysis_set.fasta",
      "data_index": "gs://pacbio-wdl/dataset/GRCh38/human_GRCh38_no_alt_analysis_set.fasta.fai"
    },
    "chromosomes": [
      "chr1",
      "chr2",
      "chr3",
      "chr4",
      "chr5",
      "chr6",
      "chr7",
      "chr8",
      "chr9",
      "chr10",
      "chr11",
      "chr12",
      "chr13",
      "chr14",
      "chr15",
      "chr16",
      "chr17",
      "chr18",
      "chr19",
      "chr20",
      "chr21",
      "chr22",
      "chrX",
      "chrY",
      "chrM"
    ],
    "chromosome_lengths": "gs://pacbio-wdl/dataset/GRCh38/human_GRCh38_no_alt_analysis_set.chr_lengths.txt",
    "tandem_repeat_bed": "gs://pacbio-wdl/dataset/GRCh38/human_GRCh38_no_alt_analysis_set.trf.bed",
    "trgt_tandem_repeat_bed": "gs://pacbio-wdl/dataset/GRCh38/trgt/human_GRCh38_no_alt_analysis_set.trgt.v0.3.4.bed",
    "hificnv_exclude_bed": {
      "data": "gs://pacbio-wdl/dataset/GRCh38/hificnv/cnv.excluded_regions.common_50.hg38.bed.gz",
      "data_index": "gs://pacbio-wdl/dataset/GRCh38/hificnv/cnv.excluded_regions.common_50.hg38.bed.gz.tbi"
    },
    "hificnv_expected_bed_male": "gs://pacbio-wdl/dataset/GRCh38/hificnv/male_expected_cn.hg38.bed",
    "hificnv_expected_bed_female": "gs://pacbio-wdl/dataset/GRCh38/hificnv/female_expected_cn.hg38.bed",
    "gnomad_af": "gs://pacbio-wdl/dataset/GRCh38/slivar_gnotate/gnomad.hg38.v3.custom.v1.zip",
    "hprc_af": "gs://pacbio-wdl/dataset/GRCh38/slivar_gnotate/hprc.deepvariant.glnexus.hg38.v1.zip",
    "gff": "gs://pacbio-wdl/dataset/GRCh38/ensembl.GRCh38.101.reformatted.gff3.gz",
    "population_vcfs": [
      {
          "data": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/EEE_SV-Pop_1.ALL.sites.20181204.vcf.gz",
          "data_index": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/EEE_SV-Pop_1.ALL.sites.20181204.vcf.gz.tbi"
      },
      {
          "data": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/nstd166.GRCh38.variant_call.vcf.gz",
          "data_index": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/nstd166.GRCh38.variant_call.vcf.gz.tbi"
      },
      {
          "data": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/hprc.GRCh38.pbsv.vcf.gz",
          "data_index": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/hprc.GRCh38.pbsv.vcf.gz.tbi"
      },
      {
          "data": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/ont_sv_high_confidence_SVs.sorted.vcf.gz",
          "data_index": "gs://pacbio-wdl/dataset/GRCh38/sv_pop_vcfs/ont_sv_high_confidence_SVs.sorted.vcf.gz.tbi"
      }
    ]
  },
  "humanwgs.slivar_data": {
    "slivar_js": "gs://pacbio-wdl/dataset/slivar/slivar-functions.v0.2.8.js",
    "hpo_terms": "gs://pacbio-wdl/dataset/hpo/hpoTerms.txt",
    "hpo_dag": "gs://pacbio-wdl/dataset/hpo/hpoDag.txt",
    "hpo_annotations": "gs://pacbio-wdl/dataset/hpo/ensembl.hpoPhenotype.tsv",
    "ensembl_to_hgnc": "gs://pacbio-wdl/dataset/hpo/ensembl.hgncSymbol.tsv",
    "lof_lookup": "gs://pacbio-wdl/dataset/slivar/lof_lookup.v2.1.1.txt",
    "clinvar_lookup": "gs://pacbio-wdl/dataset/slivar/clinvar_gene_desc.20221214T183140.txt"
  },
  "humanwgs.deepvariant_version": "String (optional)",
  "humanwgs.deepvariant_model": "WomCompositeType {\n model -> WomCompositeType {\n data -> File\ndata_index -> File \n}\nmetadata -> File \n}? (optional)",
  "humanwgs.pbsv_call_mem_gb": "Int (optional, default = if N<=3: 64 else 96)",
  "humanwgs.glnexus_mem_gb": "Int (optional, default = 30)",
  "humanwgs.run_tertiary_analysis": "Boolean (optional, default = false)",
  "humanwgs.backend": "GCP",
  "humanwgs.zones": "String",
  "humanwgs.preemptible": "Boolean"
}
```

## PacBio Github Details
Template Reference: https://github.com/PacificBiosciences/wdl-humanwgs/blob/main/README.md

