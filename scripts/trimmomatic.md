2. Trim low quality reads

```
java -jar /opt/Trimmomatic-0.32/trimmomatic-0.32.jar PE -threads 12 \
-baseout tode_a3_trim_phred20 \
/home/mcclintock/ta2007/nematodes/sample_tode_a3/TODE-A3_AGGCAGAA-CTAAGCCT_combined_R1.fastq \
/home/mcclintock/ta2007/nematodes/sample_tode_a3/TODE-A3_AGGCAGAA-CTAAGCCT_combined_R2.fastq \
ILLUMINACLIP:/opt/Trimmomatic-0.32/adapters/NexteraPE-PE.fa:2:30:10 \
LEADING:12 TRAILING:12 SLIDINGWINDOW:5:20 MINLEN:60
```
