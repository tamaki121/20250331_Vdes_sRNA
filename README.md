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

## 2025/04/16 BamtoFastq and Remapping to Clusters identified by ShortStack
### Reference
Remappingで使用したRefereceは、20250408_Vdes_ShortStack_AllLibrary.runで特定されたClusterをGCF_002443255.1_Vdes_3.0_genomic.faとmergeさせて、
配列を取得した。
```bash
Bedtools getfasta -fi GCF_002443255.1_Vdes_3.0_genomic.fa -bed ShotStack_Reference.bed -fo temp.fa -name
mv temp.fa ShotStack_Reference.fa

>ShotStack_Reference.fa
>Cluster_1::NW_019211454.1:186597-187065
ATGGAGTGTG...

```

### Build index
```bash
bowtie-build ShotStack_Reference.fa ShotStack_Reference
```

### Revert Bam to Fastq and Mapping
```bash
20250416_BamtoFastq_Remapping.run
20250416_BamtoFastq_Remapping.log

[M::bam2fq_mainloop] discarded 0 singletons
[M::bam2fq_mainloop] processed 7440455 reads
Warning: -M was specified w/o --best; automatically enabling --best
# reads processed: 7440455
# reads with at least one reported alignment: 3993972 (53.68%)
# reads that failed to align: 427068 (5.74%)
# reads with alignments sampled due to -M: 3019415 (40.58%)
Reported 3993972 alignments to 1 output stream(s)
```

### Revert each bamfile to fastq and Mapping(2025/04/20)
```bash
20250420_BamtoFastq_parallel.run
20250420_MappingtoShortStack_parallell.run
```

```bash
for i in {58..70}; do
    sbatch ${Script} ${i}
done
```

### Calculate RPM(2025/05/11)
```bash
20250423_CalculateRPM.run
20250510_CalculateRPM_EachTissue.R
```
20250423_caluclateRPM.runで再マッピングしたsamファイルのRPMを計算した。  
その後、20250510_CalculateRPM_EachTissu.Rで組織ごとの平均値を出して、それぞれのTSVのデータを手動でVdes_AllLibrary(N258-N270,exceptN264).xlsxに張り付けた。  
スクリプトで合併しようとすると、値がおかしくなったので手動で張り付けた。  

### Re ShortStack and MajorRNA(2025/05/25, 26)
```bash
ReShortStack
20250525_Vdes_All.log
20250525_Vdes_All.run

MajorRNA Blast
20250526_Blast_miRGeneDB_AllSpecies.run
```



