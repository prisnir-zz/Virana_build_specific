# Virana_build_specific
Minor manipulation to the existing Virana source code https://github.com/schelhorn/virana/ . Provides option to custom build DBs based on human genome build. I have only customised it to include builds GrCh37 and 38.

The original usage and documentation is based on the source code provided by the developers [ avaialble here: https://github.com/schelhorn/virana/]

=
The only change is reflected in the following scripts:
=
python vref.py fasta -r Homo_sapiens -g 37 -o my_genome_GrCh37_db.fa --debug

python vref.py fasta -r Homo_sapiens_cDNA -g 38 -o my_transcriptome_db.fa --debug

python vref.py fasta -r Homo_sapiens_cDNA -g 37 -o my_transcriptome_db.fa --debug

=
For more help::
=
python virana/vref.py fasta -h
vref fasta 1.0.0

Obtains NCBI RefSeq and Ensembl reference genomes and transcriptomes.

\nUsage:
    \n\tvref fasta [SWITCHES] 

\nMeta-switches
    \t-h, --help                                                    Prints this help message and quits
    \t--help-all                                                    Print help messages of all subcommands and quit
    \t-v, --version                                                 Prints the program's version and quits

\nSwitches
    \t-d, --debug                                                   Enable debug messages
    \t-g, --genome_build VALUE:str                                  Provisions records based on the genome build provided please provide 37 or 38; default is set to GrCh38;
                                                                  the default is '38'\n
    \t-o, --output_file VALUE:str                                   Sets the fasta output file. Note that all downloaded fasta records are stored within a single fasta file.;
                                                                  required
    \n\t-r, --reference VALUE:{'UniVec', 'rRNA', 'Homo_sapiens', 'Fungi', 'Plasmids', 'Protozoa', 'Viruses', 'Homo_sapiens_cDNA', 'Fungi_DRAFT', 'Bacteria', 'Bacteria_DRAFT'}
                                                                  Sets the kind of references to obtain; microbial ('Fungi', 'Fungi_DRAFT', 'Bacteria', 'Bacteria_DRAFT',
                                                                  'Protozoa', 'Viruses'), 'Plasmids'), human ('Homo_sapiens', 'Homo_sapiens_cDNA'), as well as taxonomically
                                                                  mixed ('rRNA' (from SILVA), 'UniVec') references are available.; the default is ['Fungi', 'Fungi_DRAFT',
                                                                  'Bacteria', 'Bacteria_DRAFT', 'Homo_sapiens', 'Viruses', 'UniVec', 'Plasmids', 'Protozoa', 'rRNA',
                                                                  'Homo_sapiens_cDNA']; may be given multiple times
    \n\t-z, --zipped                                                  Write gzipped output\n


