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


#Quality Control 

<img width="688" height="443" alt="image" src="https://github.com/user-attachments/assets/78d6aeeb-e45b-4a89-9ddd-4fa1a1d22b16" />

#Trimming

<img width="1281" height="584" alt="image" src="https://github.com/user-attachments/assets/46e8a8a3-bd44-4a31-adfc-88652ac1d117" />



