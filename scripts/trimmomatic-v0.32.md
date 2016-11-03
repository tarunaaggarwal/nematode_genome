2. Trim low quality reads using default parameters

```
java -jar /opt/Trimmomatic-0.32/trimmomatic-0.32.jar PE -threads 12 \
-baseout prefix-phred \
R1.fastq \
R2.fastq \
ILLUMINACLIP:/opt/Trimmomatic-0.32/adapters/NexteraPE-PE.fa:2:30:10 \
LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
```
