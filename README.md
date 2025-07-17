# Fastqc_quality_control_bash
RNA-Seq Verisi Kalite Kontrolü ve Opsiyonel Trimming (Single-End). 


sequencing_sample.fastq.txt: Tek uçlu (Single-End) RNA-Seq okuma dosyası :  
# https://drive.google.com/file/d/1HLIbV7Y_J_m8zccwnVB0DufmZkCR97SW/view

sequencing_sample_fastqc.html	Ham verinin FastQC raporu


sequencing_sample.trimmed.fastq	Trimmomatic sonrası kırpılmış dosya


sequencing_sample.trimmed_fastqc.html	Kırpılmış verinin FastQC raporu


trimmomatic-0.39.jar	Trimmomatic trimming aracı

Eğer yalnızca ifade düzeyi analizi (differential expression) yapılacaksa trimming zorunlu değildir. Ancak trimming, hizalama sonrası kaliteyi artırabilir ve mapping oranını iyileştirebilir.
Motif analizi, splice site, SNP analizi gibi işlemler yapılacaksa trimming kesinlikle önerilir.

>>>>>>>>>>>Ubuntu_bash.txt dosyasında bash komutları ve açıklamalar ayrıca verilmiştir.



<img width="755" height="541" alt="image" src="https://github.com/user-attachments/assets/263e0b19-4ca2-47a2-8148-449162a08293" />

(base) amsung@DESKTOP-VBIAG6E:~$ cd RNA-seq
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ fastqc sequencing_sample.fastq.txt
text/plain
Started analysis of sequencing_sample.fastq.txt
Approx 5% complete for sequencing_sample.fastq.txt
Approx 10% complete for sequencing_sample.fastq.txt
Approx 15% complete for sequencing_sample.fastq.txt
Approx 20% complete for sequencing_sample.fastq.txt
Approx 25% complete for sequencing_sample.fastq.txt
Approx 30% complete for sequencing_sample.fastq.txt
Approx 35% complete for sequencing_sample.fastq.txt
Approx 40% complete for sequencing_sample.fastq.txt
Approx 45% complete for sequencing_sample.fastq.txt
Approx 50% complete for sequencing_sample.fastq.txt
Approx 55% complete for sequencing_sample.fastq.txt
Approx 60% complete for sequencing_sample.fastq.txt
Approx 65% complete for sequencing_sample.fastq.txt
Approx 70% complete for sequencing_sample.fastq.txt
Approx 75% complete for sequencing_sample.fastq.txt
Approx 80% complete for sequencing_sample.fastq.txt
Approx 85% complete for sequencing_sample.fastq.txt
Approx 90% complete for sequencing_sample.fastq.txt
Approx 95% complete for sequencing_sample.fastq.txt
Analysis complete for sequencing_sample.fastq.txt
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ ls
bash.txt                     sequencing_sample_fastqc.html  trimmomatic-0.39.jar
sequencing_sample.fastq.txt  sequencing_sample_fastqc.zip
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ java -jar trimmomatic-0.39.jar SE -phred33 sequencing_sample.fastq.txt sequencing_sample.trimmed.fastq HEADCROP:10
TrimmomaticSE: Started with arguments:
 -phred33 sequencing_sample.fastq.txt sequencing_sample.trimmed.fastq HEADCROP:10
Automatically using 4 threads
Input Reads: 657474 Surviving: 657474 (100.00%) Dropped: 0 (0.00%)
TrimmomaticSE: Completed successfully
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ fastqc sequencing_sample.trimmed.fastq
null
Started analysis of sequencing_sample.trimmed.fastq
Approx 5% complete for sequencing_sample.trimmed.fastq
Approx 10% complete for sequencing_sample.trimmed.fastq
Approx 15% complete for sequencing_sample.trimmed.fastq
Approx 20% complete for sequencing_sample.trimmed.fastq
Approx 25% complete for sequencing_sample.trimmed.fastq
Approx 30% complete for sequencing_sample.trimmed.fastq
Approx 35% complete for sequencing_sample.trimmed.fastq
Approx 40% complete for sequencing_sample.trimmed.fastq
Approx 45% complete for sequencing_sample.trimmed.fastq
Approx 50% complete for sequencing_sample.trimmed.fastq
Approx 55% complete for sequencing_sample.trimmed.fastq
Approx 60% complete for sequencing_sample.trimmed.fastq
Approx 65% complete for sequencing_sample.trimmed.fastq
Approx 70% complete for sequencing_sample.trimmed.fastq
Approx 75% complete for sequencing_sample.trimmed.fastq
Approx 80% complete for sequencing_sample.trimmed.fastq
Approx 85% complete for sequencing_sample.trimmed.fastq
Approx 90% complete for sequencing_sample.trimmed.fastq
Approx 95% complete for sequencing_sample.trimmed.fastq
Analysis complete for sequencing_sample.trimmed.fastq
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ ls
bash.txt                         sequencing_sample.trimmed_fastqc.html  sequencing_sample_fastqc.zip
sequencing_sample.fastq.txt      sequencing_sample.trimmed_fastqc.zip   trimmomatic-0.39.jar
sequencing_sample.trimmed.fastq  sequencing_sample_fastqc.html
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$  gzip sequencing_sample.fastq.txt
(base) amsung@DESKTOP-VBIAG6E:~/RNA-seq$ ls
Ubuntu_bash.txt                  sequencing_sample.trimmed_fastqc.html  sequencing_sample_fastqc.zip
sequencing_sample.fastq.txt.gz   sequencing_sample.trimmed_fastqc.zip   trimmomatic-0.39.jar
sequencing_sample.trimmed.fastq  sequencing_sample_fastqc.html


