# WGS_Bacterial_flow
Bacterial genome assembly and quality assessment pipeline using Bactopia, SPAdes, MeDuSa, QUAST, and Sourmash for de novo assembly, reference-guided scaffolding, assembly evaluation, and taxonomic screening.

**Paired-end FASTQ → Quality Control → De novo Assembly → Scaffolding → Assembly Assessment → Taxonomic Screening → Final Metrics**

### Workflow

1. **Input**

   * Paired-end FASTQ files

2. **Read Quality Control**

   * Bactopia (Petit & Read, 2020)
   * FastQC v0.12.1
   * Low-quality base trimming and read preprocessing

3. **De novo Genome Assembly**

   * SPAdes (Bankevich et al., 2012)
   * Default isolate parameters

4. **Contig Ordering and Scaffolding**

   * MeDuSa (Bosi et al., 2015)
   * Reference-guided contig ordering using species-specific reference genomes

5. **Assembly Quality Assessment**

   * QUAST v5.3.0 (Gurevich et al., 2013)
   * N50
   * Number of contigs
   * Total assembled genome size
   * Genome coverage
   * Mean sequencing depth
   * Number of reads per sample
   * Sequencing success rate

6. **Taxonomic Identification and Contaminant Screening**

   * Sourmash (Pierce et al., 2019)
   * GTDB database

### Reference Genomes

| Species                      | Reference genome(s)           |
| ---------------------------- | ----------------------------- |
| *Escherichia coli*           | CP163852.1                    |
| *Klebsiella pneumoniae*      | NZ_CP027036.1; NZ_CP093465.1  |
| *Klebsiella quasipneumoniae* | CP034129.1; NZ_VDFT01000001.1 |

### Computational Environment

The workflow was executed on the **IAM Carlos Chagas computational cluster (Fiocruz PE)** running **Ubuntu Server 20.04.6 LTS**.

<img width="1774" height="887" alt="ChatGPT Image 24 de set  de 2026, 13_54_04" src="https://github.com/user-attachments/assets/27614347-00d0-4a24-98f1-c37e4ec19215" />


