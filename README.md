# metagenome
how to annotate

suggested metagenome steps, lines, notes
1. Quality filtering/trimming raw reads using fastp 0.19.4 
2. removal of host DNA, Fasta reference required using BBMap 38.90
bbduk.sh ref=T.molitor_genome_GCA_014282415.1_130x_Sep201.fna(file) k=43(kmer length) threads=28 ordered=t in=(SAMPLENAME_R1_trimmed.fastq.gz in2=SAMPELNAME_R2_trimmed.fastq.gz out=SAMPLENAME_R1_bbduk.fq) out2=(SAMPLENAME_R2_bbduk.fq)
specificity is the K mer, the k=43 to make it strict. if i wanted to allow for more mismatches I would make the K=21
max threads 28
output is the file created, the sequences that didn't match to the reference genome. 
bbduk.sh -> gives options.

first download host genome from NCBI (through assembly)

notes

example destination path  /home/UwU7/(directory)/(directory)/file/* /
databases. from kaiju website. 

basic commands to remember because I'm a fucking pretty ass princess not a fucking coder
ls -lh  lists all in sizes
