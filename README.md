# Quantifying-attribute-information-gains-from-geospatial-metadata-enrichment-201-paired-metadata
This repository package contains the final, matched JSON metadata records used for the analysis of the study titled: Quantifying attribute information gains from geospatial metadata enrichment.
## Folder structure

- `pre-enrichment.7z`: 201 original metadata JSON records, before enrichment.
- `post-enrichment.7z`: the corresponding 201 JSON records after enrichment.

The two folders contain **exactly the same 201 filenames**. Match records by filename; for example, `pre-enrichment/Addresses_of_buildings_2016_Shape.json` pairs with `post-enrichment/Addresses_of_buildings_2016_Shape.json`. The original metadata fields and values are preserved in the corresponding post-enrichment JSON; the post-enrichment version additionally contains an `enrichment` field with the information produced by the Data-aware metedata enrichment (DaME) workflow.

## How to use

1. Download and extract this archive.
2. Compare identically named JSON files across `pre-enrichment/` and `post-enrichment/`.
3. Inspect the `enrichment` arrays in post-enrichment records for extracted dataset-level, spatial-index, and attribute-profile information.
4. When calculating counts, state the unit of analysis: metadata record, spatial enrichment block, field summary, or statistical cell. Multiple tiles/layers can produce multiple summaries for one field name.

## Important interpretation notes

- These are metadata JSON exports, not copies of the underlying geospatial source datasets.
- If interested in reproducing the enrichment,download the source datasets on the download links provided in the respective metadata and enrich the pre-enriched metadata with the DaME plugin provided here: git@github.com:Blessingk-code/DaME.git
- A post-enrichment profile documents what the enrichment workflow extracted, not necessarily every field available in the underlying source dataset.
- Some records contain spatial index information rather than thematic feature attributes; both may be useful but should be distinguished analytically.
- The folder contains only the 201 pairs included in the study; excluded records are omitted and can be found on the original source, on Paituli.

## Package verification

At packaging time, the 201 filenames matched exactly between the two folders; all files were parseable JSON; and every original JSON key/value was preserved in its paired post-enrichment JSON. Each post-enrichment JSON contained an `enrichment` field. The package is not a replacement for the separate analysis code and methodological documentation needed to reproduce every manuscript statistic.

### Citation 

The  citattion of the 
