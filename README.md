# humanReadsRemovalBatch

## What it does
This tool remove the human reads from paired end fastq files and report in an output folder
the purged reads and a statistics summary with the number of reads and bases for the 
purged reads

## How it works
The syntax of the tool is the following

  -h, --help            show this help message and exit
  -i INPUTFILE, --inputFile INPUTFILE
                        Input file with list of paired end file name
  -t THREADS, --threads THREADS
                        Number of threads to use
  -o OUTPUT_FOLDER, --output_folder OUTPUT_FOLDER
                        Output folder
  -c CONDA_DIRECTORY, --conda_directory CONDA_DIRECTORY
                        The conda environment path
  -b BOWTIE2_INDEX, --bowtie2_index BOWTIE2_INDEX
                        The human bowtie2 index file ending with .1.bt2
                        
                        

The input file must be formatted with the path to the reads that one wants to filter, one 
line for each read:

path/read1_1.fastq
path/read1_2.fastq
path/read2_1.fastq
path/read2_2.fastq
......
......

The bowtie2 index is the file with suffix _1.bt2 for the human reference index
The conda directory is the complete path the (mini)conda environment 
