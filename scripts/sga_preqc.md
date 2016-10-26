#### 0. Run SGA Preqc to estimate genome size


```
sga preprocess --pe-mode 1 R1.fastq R2.fastq > info.fastq
sga index -a ropebwt --no-reverse -t 8 info.fastq
sga preqc -t 8 info.fastq > name.preqc
/opt/sga/src/bin/sga-preqc-report.py tode_a3.preqc /opt/sga/src/examples/preqc/*.preqc
```