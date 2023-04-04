# NanoDengue
NanoDengue is a Bash script designed to generate a consensus FASTA file from Nanopore sequencing fastq data. The script is user-friendly and uses popular command-line tools to streamline the analysis process. This tool can be a valuable resource for researchers and bioinformaticians who work with Nanopore sequencing data and need a fast and efficient way to analyze it.

# Script Overview
This Bash script takes in a folder containing fastq.gz files, unzips them, aligns them to a reference genome using minimap2, and generates a consensus fasta file from the aligned BAM files using samtools.

# Script Steps
1. Set the path for the reference genome file.
2. Loop through all the fastq.gz files in the folder and gunzip them.
3.Loop through all the fastq files in the folder.
4.Generate the output SAM file name based on the input fastq file name.
5.Run minimap2 to align the fastq file to the reference genome and output a SAM file.
6.Generate the output BAM file name based on the input SAM file name.
7.Sort the SAM file and output it as a BAM file.
8.Generate an index file for the BAM file.
9.Generate the output consensus fasta file name based on the input BAM file name.
10.Generate the consensus fasta file from the BAM file.

#Required Dependencies
This script requires minimap2 and samtools to be installed.

# Usage
Save the script in a file with a .sh extension.
Place the script in the folder containing the fastq.gz files.
Open a terminal window and navigate to the folder.
Run the script using the following command:
bash scriptname.sh

The script will execute and generate the output SAM, BAM, and consensus fasta files in the same folder.

# Example Output
If the input fastq file name is "sample.fastq", the output files generated by the script will be:

"sample_minimap2.sam"
"sample_minimap2_sorted.bam"
"sample_minimap2_sorted.bam.bai"
"sample_minimap2_sorted.consensus.fasta"
