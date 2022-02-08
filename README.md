# Biological-Command-Line-Interpreter
> Biological Command Line Interpreter take commands that apply some biological operations on biological data
# Commands Description
> **gc** 
- *Usage* : `gc seq.`
- *Parameters seq* : `a string represents the sequence.`
- *Description* : `This command takes a seq as a string and returns the gc percentage of it.`
- *Sample run* : `gc AGCAT.`

> **transcribe**
- *Usage* : `transcribe seq.`
- *Options and arguments* : `a string represents the sequence.`
- *Description* : `This command takes a seq as a string and returns its transcription.`
- *Sample run* : `transcribe AGCAT.`

> **revrse_complement**
- *Usage* : `reverse_complement seq.`
- *Options and arguments* : `a string represents the sequence.`
- *Description* : `This command takes a seq as a string and returns its reverse complement.`
- *Sample run* : `reverse_complement AGCAT.`

> **calc_nbases**
- *Usage* : `clac_nbases seq.`
- *Options and arguments* : `a string represents the sequence.`
- *Description* : `This command takes a seq and calculates its nbases.`
- *Sample run* : `calc_nbases AGCAT.`

> **is_valid**
- *Usage* : `is_valid seq type.`
- *Options and arguments* : 

    `Seq: a string represents the sequence.`
    
    `type : a string that represents the type of the sequence. It can be one of these  keywords [protein, dna, rna].`
    
- *Description* : `This command takes a seq and a type (protein, dna, rna) and returns a Boolean value of whether it’s a valid type or not.`
- *Sample run* : `is_valid NGCTN protein.`

> **filter_nbases**
- *Usage* : `filter_nbases seq.`
- *Options and arguments* : `a string represents the sequence.`
- *Description* : `This command takes a seq and returns the Seq after removing n bases.`
- *Sample run* : `filter_nbases NGCTN.`

> **seq_alignment**
- *Usage* : `seq_alignment seq1 seq2 [-o file].`
- *Options and arguments* : 

    `seq1,seq2: strings represents the sequence.`
    
    `-o file : specifies the path of the output file.`
   
- *Description* : `  This command takes 2 sequences as input and get all their alignments along with the score. The -o is an optional parameter if we need the output to be written on a file instead of the screen.`
- *Sample run* : ` seq_alignment AGCCT AGC -o output.txt`

> **seq_alignment_files**
- *Usage* : `seq_alignment_files file1 file2 [-o file3]`
- *Options and arguments* : 

    `file1,file2: specifies the paths of the files to be aligned that contain the sequences.`
    
    `-o file3 : specifies the path of the output file.`
   
- *Description* : ` This command takes 2 fasta files as input, each file contains a single sequence.It reads the 2 sequences from files and get all their alignments along with the score. The -o is an optional parameter if we need the output to be written on a file instead of the screen.`
- *Sample run* : ` seq_alignment s1.fasta s1.fasta -o output.txt`

> **online_alignment**
- *Usage* : `online_align seq [-o file]`
- *Options and arguments* : 

    `seq : a string represents the sequence.`
    
    `-o file : specifies the path of the output file.`
   
- *Description* : ` This command takes a sequence and uses BLAST to search the internet for its alignments. The output should be all the information in the resultant BLAST record. The -o is an optional parameter if we need the output to be written on a file instead of the screen..`
- *Sample run* : `  seq_alignment ACTGCCGTCAAGTCAG -o output.txt`

> **merge_fasta**
- *Usage* : `merge_fasta file1 file2 [file3 …] [-o output_file]`
- *Options and arguments* : 

    `file1,file2: specifies the paths of the files to be merged.`
    
    `-o file3 : specifies the path of the output file.`
   
- *Description* : `  This command takes any number of fasta files (at least two) and merge their contents into one fasta output file. There is an option to write the merge result in a file using -o option, otherwise the merge result will be displayed on the console.`
- *Sample run* : ` merge_fasta f1.fasta f2.fasta f3.fasta f4.fasta`

> **convert_to_fasta**
- *Usage* : `convert_to_fasta file.`
- *Options and arguments* : `: specifies the path of a genbank file.`
- *Description* : `This command converts the input genbank file with multiple records onto a fasta formatted file. The output is to be written in a different output fasta file.`
- *Sample run* : ` convert_to_fasta “ls-orchid.gbk”`
