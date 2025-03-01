[![sihellem - TERmitoGENOMES](https://img.shields.io/static/v1?label=sihellem&message=TERmitoGENOMES&color=red&logo=github)](https://github.com/sihellem/TERmitoGENOMES "Go to GitHub repo")
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

# TERmitoGENOMES
Repository for mitogenome assembly and annotation in termites


## Annotate mitogenomes
_Dependencies_: [MitoFinder](https://github.com/RemiAllio/MitoFinder)
```
## Get current database file to be used by MitoFinder's "--refseq"
wget https://raw.githubusercontent.com/sihellem/TERmitoGENOMES/reference_mitogenomes/v0/references.gb.gz && gzip -d references.gb.gz

### Annotation of mitochondrial scaffolds
MITO_REF=references.gb
ASSEMBLY=sample.fasta
ID=some_id

mitofinder \
  --processors ${SLURM_CPUS_PER_TASK} \
  --seqid $ID \
  --assembly $ASSEMBLY \
  --tRNA-annotation "mitfi" \
  --organism 5 \
  --refseq $MITO_REF
```

## How to cite
Credits: Hellemans Simon.
