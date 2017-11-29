

1. Using python write a tool which generates a random subsampling tool
for sequences. Given a FASTA sequence database file, which has 100,000
sequences, generate a new file which is a random subset these
sequences selecting only 10% of them. Make this 10% an option in the
program so it is easy to change to 20%, etc.

See the script 'rand_shuffle_seqs.py' in the homework template
 
2. Run RNAseq analysis to compute the gene expression for two experiments.
We will use data from this paper on light induction in bacterium Prochlorococcus

See this paper:

* Thompson et al. PLoS One 2016; 11(10): e0165375 doi: [10.1371/journal.pone.0165375](http://dx.doi.org/10.1371/journal.pone.0165375)

* Here is a view of the sequencing data. All data are on cluster in this folder
`/bigdata/gen220/shared/projects/HW4/hw4_template`

Also you can get it from the web directly yourself.
[https://www.ebi.ac.uk/ena/data/view/PRJNA315575](https://www.ebi.ac.uk/ena/data/view/PRJNA315575)

The data for one timepoint: [0hrs light](https://www.ebi.ac.uk/ena/data/view/SRR3234519&display=html)

Go and get the fastq files to process - see the [download script](https://github.com/biodataprog/hw4_hyphaltip_template/blob/master/download_bacteria_light_fastq.sh)

Light 0hr

* [0hr_1.fastq.gz](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR323/009/SRR3234519/SRR3234519_1.fastq.gz)
* [0hr_2.fastq.gz](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR323/009/SRR3234519/SRR3234519_2.fastq.gz)

The data for another timepoints: [4hrs light](https://www.ebi.ac.uk/ena/data/view/SRR3234522&display=html)

The fastq files to process

* [4hr_1.fastq.gz](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR323/002/SRR3234522/SRR3234522_1.fastq.gz)
* [4hr_2.fastq.gz](ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR323/002/SRR3234522/SRR3234522_2.fastq.gz)

Here is the Prochlorococcus marinus subsp. pastoris str. CCMP1986 genome: [GCF_000011465.1](https://www.ncbi.nlm.nih.gov/assembly/GCF_000011465.1). The RefSeq for this genome is at that link.

Can be obtained from this [link](ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/011/465/GCF_000011465.1_ASM1146v1/GCF_000011465.1_ASM1146v1_genomic.fna.gz)

And the [GFF](ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/011/465/GCF_000011465.1_ASM1146v1/GCF_000011465.1_ASM1146v1_genomic.gff.gz)

* Use Hisat2, samtools, and stringtie to generate a table of expression for these two experiments
* Write a python script that will generate a report with 5 columns of data.
Gene Name, Chromosome, Start, End, Strand, Gene Length, FPKM exp1, FPKM exp 2
* Using R or other tools, make these plots
    * Plot gene expression from exp1 vs gene expression of exp 2
    * Plot gene length vs expr1 expression (FPKM). Is there a relationship?
    * Plot gene location vs expr2 (FPKM). Is there any relationship?
* print a list of genes which are > 2 fold higher in the 4hr time point?



