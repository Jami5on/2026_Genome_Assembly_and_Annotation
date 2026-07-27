# 2026_Genome_Assembly_and_Annotation
This repository contains shell scripts used for genome assembly and annotation of tiger beetle PacBio HiFi long-read sequence data


# Overview of workflow:

(also see https://github.com/MHChou-Hsun/Genome_Assembly_and_Annotation_2026)

- read statistics

- adapter removal

- assembly

- decontamination

- annotation with two different protein hint sources

- quality control: completeness, contiguity, and accuracy

# Programs:

1. Read statistics
    - following Steps 1-3 outlined in Kim and Kim (2022; https://doi.org/10.1016/j.xpro.2022.101506)
    - Jellyfish
    - Genomescope (online http://genomescope.org/genomescope2.0/ or HPCC conda)
2. Genome Assembly
   - HiFiAdaptFilt (https://github.com/sheinasim-USDA/HiFiAdapterFilt/blob/master/README.md)
   - Hifiasm
3. Decontamination
   - purge_haplotigs
   - BlobToolKit
   - seqkit
   - BLAST
4. Assembly Statistics
   - BUSCO
   - Quast
   - Referee
5. Genome Annotation
   - RepeatModeler
   - RepeatMasker
   - BRAKER3
6. Supporting utilities
   - Samtools
   - minimap2
   - R
  
# References
- Kim, J., & Kim, C. (2022). A beginner’s guide to assembling a draft genome and analyzing structural variants with long-read sequencing technologies. STAR Protocols, 3(3). https://doi.org/10.1016/j.xpro.2022.101506
- Singh, R. P., Weng, Y. M., Sondhi, Y., Plotkin, D., Frandsen, P. B., & Kawahara, A. Y. (2024). Genome assembly of a nocturnal butterfly (Macrosoma leucophasiata) reveals convergent adaptation of visual genes. Communications Biology, 7(1), 1664. https://doi.org/10.1038/s42003-024-07124-2
- Jérémy Gauthier, Cody Raul Cardenas, Matilde Nari, Conrad P D T Gillett, Emmanuel F A Toussaint, Draft genome of the endemic alpine ground beetle Carabus (Platycarabus) depressus (Coleoptera: Carabidae) from long-read sequencing of a frozen archived specimen, G3 Genes|Genomes|Genetics, Volume 15, Issue 5, May 2025, jkaf027, https://doi.org/10.1093/g3journal/jkaf027
