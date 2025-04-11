# 20250331_Vdes_sRNA
## 2025/03/31 Moving Bam file(NN263dedup.mapcolVdes_3.0.bam) to my work space
```bash
cp //project/okamura-lab-hpc/20250310_Varroa_sRNA/N263dedup.mapcolVdes_3.0.bam //work/h-tamaki/20250331_Vdes_sRNA
```

## 2025/04/03 Create ShortStack environment
```bash
conda create -n shortstack -c bioconda shortstack
```

## 2025/04/03 ShortStack Test Run  
Test runs were performed against the N261 and N263 libraries.  
Details of these libraries can be found on the following links.  
https://docs.google.com/spreadsheets/d/1nR3Zh3I6SoTMR8Lx9IYan7XHd-CtLZys/edit?gid=156060293#gid=156060293

```bash
20250403_Vdes_ShortStack_test.run 20250403_Vdes_ShortStack_test.log


ShortStack version 4.1.1

Beginning run
Options:
{   'adapter': None,
    'align_only': False,
    'autotrim': False,
    'autotrim_key': 'TCGGACCAGGCTTCATTCCCC',
    'autotrim_only': False,
    'bamfile': [   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/N261dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/N263dedup.mapcolVdes_3.0.bam'],
    'dicermax': 50,
    'dicermin': 18,
    'dn_mirna': False,
    'genomefile': '/work/h-tamaki/mRNA_UCSC/DIR_fna/GCF_002443255.1_Vdes_3.0_genomic.fa',
    'known_miRNAs': None,
    'locifile': None,
    'locus': None,
    'make_bigwigs': False,
    'mincov': 1,
    'mmap': 'u',
    'nohp': False,
    'outdir': '/work/h-tamaki/20250331_Vdes_sRNA/20250404_Vdes_N263_N261Test',
    'pad': 200,
    'readfile': None,
    'strand_cutoff': 0.8,
    'threads': 1}
Required executable RNAfold : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/RNAfold
Required executable strucVis : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/strucVis
Required executable samtools : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/samtools

Fri 04 Apr 2025 15:00:33 +0900 JST
Defining small RNA clusters de novo
With 9680609 total reads and mincov of 1 reads per million, the min read depth is 10

Fri 04 Apr 2025 15:04:00 +0900 JST
Analyzing cluster properties using 1 threads

Fri 04 Apr 2025 15:05:12 +0900 JST
 Completed

Writing final files

Non-MIRNA loci by DicerCall:
18 395
22 165
20 151
19 150
23 141
24 121
21 84
30 40
28 38
29 32
25 23
27 18
26 17

Fri 04 Apr 2025 15:05:12 +0900 JST
Run Completed!

```
## 2025/04/08 ShortStack All libraries
```bash
20250408_Vdes_ShortStack_AllLibrary.run
20250408_Vdes_ShortStack_AllLibrary.log


ShortStack version 4.1.1

Beginning run
Options:
{   'adapter': None,
    'align_only': False,
    'autotrim': False,
    'autotrim_key': 'TCGGACCAGGCTTCATTCCCC',
    'autotrim_only': False,
    'bamfile': [   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N258dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N259dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N260dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N261dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N262dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N263dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N265dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N266dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N267dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N268dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N269dedup.mapcolVdes_3.0.bam',
                   '/work/h-tamaki/20250331_Vdes_sRNA/BamFile/Test/N270dedup.mapcolVdes_3.0.bam'],
    'dicermax': 50,
    'dicermin': 18,
    'dn_mirna': False,
    'genomefile': '/work/h-tamaki/mRNA_UCSC/DIR_fna/GCF_002443255.1_Vdes_3.0_genomic.fa',
    'known_miRNAs': None,
    'locifile': None,
    'locus': None,
    'make_bigwigs': False,
    'mincov': 1,
    'mmap': 'u',
    'nohp': False,
    'outdir': '/work/h-tamaki/20250331_Vdes_sRNA/20250409_Vdes_AllLibraries',
    'pad': 200,
    'readfile': None,
    'strand_cutoff': 0.8,
    'threads': 1}
Required executable RNAfold : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/RNAfold
Required executable strucVis : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/strucVis
Required executable samtools : /work/h-tamaki/tools/miniforge3/envs/shortstack/bin/samtools

Thu 10 Apr 2025 19:40:51 +0900 JST
Defining small RNA clusters de novo
With 67640305 total reads and mincov of 1 reads per million, the min read depth is 68

Thu 10 Apr 2025 19:44:44 +0900 JST
Analyzing cluster properties using 1 threads

Thu 10 Apr 2025 19:51:42 +0900 JST
 Completed

Writing final files

Non-MIRNA loci by DicerCall:
18 330
20 269
23 211
24 178
22 144
19 134
21 55
28 33
29 32
30 24
25 21
26 14
27 14

Thu 10 Apr 2025 19:51:42 +0900 JST
Run Completed!
```
