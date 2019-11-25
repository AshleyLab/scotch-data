# scotch-data-grch37

GRCh37 region feature data for [Scotch indel caller](https://github.com/AshleyLab/scotch). (GRCh38 features available [here](https://github.com/AshleyLab/scotch-data-grch38).)

## Data

Columns
1. *chromosome*
2. *position*
3. *nistHC*
  * whether the position is in NIST-high-confidence regions
  * `ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/release/NA12878_HG001/NISTv3.3.2/GRCh37/HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_nosomaticdel.bed`
4. *repMasker*
  * whether the position is in RepeatMakser-masked regions
  * UCSC Genome Browser Table Browser --> Genome: Human, Group: All Tables, Table: rmsk
5. *segDups*
  * whether the position lies in segmental duplications
  * `ftp://ftp-trace.ncbi.nih.gov/giab/ftp/data/NA12878/analysis/NIST_union_callsets_06172013/superdupsmerged_all_sort.bed.gz`
6. *LCR*
  * whether the position lies in low-complexity regions
  * hs37d5-LCRs.bed.gz, available at `https://figshare.com/articles/Low_complexity_regions_in_hs37d5/969685`
7. *gc50*
  * GC content within a 50-bp window
  * calculated with `bedtools nuc`
8. *gc1000*
  * GC content within a 1000-bp window
  * calculated with `bedtools nuc`
9. *map100*
  * mappability score
  * UCSC Genome Browser Table Browser --> Genome: Human, Group: All Tables, Table: wgEncodeCrgMapabilityAlign100mer
10. *uniq35*
  * uniqueness score within 35 bp
  * UCSC Genome Browser Table Browser --> Genome: Human, Group: All Tables, Table: wgEncodeDukeMapabilityUniqueness35bp
