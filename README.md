# Virana_build_specific
Minor manipulation to the existing Virana source code https://github.com/schelhorn/virana/ . Provides option to custom build DBs based on human genome build. I have only customised it to include builds GrCh37 and 38.

The original usage and documentation is based on the source code provided by the developers [ avaialble here: https://github.com/schelhorn/virana/]


The only change is reflected in the following scripts:
=
python vref.py fasta -r Homo_sapiens -g 37 -o my_genome_GrCh37_db.fa --debug

python vref.py fasta -r Homo_sapiens_cDNA -g 38 -o my_transcriptome_db.fa --debug

python vref.py fasta -r Homo_sapiens_cDNA -g 37 -o my_transcriptome_db.fa --debug


For more help::
=
python virana/vref.py fasta -h
