# mg-sample-data
## Sample data for a metagenomic / metatranscriptomic workflow.

*The dna / rna is mouse cecal matter that contains mouse, mouse chow and microbial nucleotide sequences.* 

[Full data is here.](https://www.ncbi.nlm.nih.gov/sra?linkname=bioproject_sra_all&from_uid=379709)

Centrifuge database of bacteria available here -- ftp://ftp.ccb.jhu.edu/pub/infphilo/centrifuge/data/p_compressed+h+v.tar.gz 

CAUTION: ~5GB file.

## explanation of directories / files

* /dna

  Two samples of 2500 paired (R1,R2) 100bp reads (cancer and control).
  
* /rna

  Two samples of 2500 paired (R1,R2) 100bp reads (matched to dna).
  
* /annotation

  Annotation from Patric in tab-delimited and gff formats.
  
* /genomes

  Two bacterial reference genomes from Patric.
  
* /metadata
 
  Metadata of genomes including their taxonomic lineage.
  
* /scripts

  Sample scripts to run on PBS scheduling system.

* /scripts/workers

  "Worker" scripts that are launched by the jobs running on the HPC/HTC.
  Can be modified to run interactively if needed.

---
### Reads sampled using sample-reads-randomly.py from the khmer package
http://khmer.readthedocs.io/en/latest/citations.html
e.g. sample-reads-randomly.py -N 10000 -S 3 -R 1 --gzip RNA_2_GCCAAT_L008_R1_016.fastq
and  sample-reads-randomly.py -N 10000 -S 3 -R 1 --gzip RNA_2_GCCAAT_L008_R2_016.fastq
