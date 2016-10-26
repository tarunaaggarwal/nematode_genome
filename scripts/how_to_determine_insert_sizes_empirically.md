## How to determine insert sizes empirically  

### A. Index the genome assembly

```
bwa index scaffolds.fa  

```

### B. Map paired-end reads to the indexed genome 

```
bwa mem scaffolds.fa \
R1.fastq R1.fastq > name.sam 
```

### C. Sort PE sam file

```
samtools sort name.sam name.sorted
```

### D. Find mapping metrics
```
samtools flagstat name.sorted.bam
```
### E. Find insert size metrics

```
picard-tools CollectInsertSizeMetrics \
     I=name.sorted.bam \
     O=name_insert_size_metrics.txt \
     H=name_insert_size_histogram.pdf \
     M=0.5
```