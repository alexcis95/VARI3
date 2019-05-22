# Package epiasocgenes

To use the epiasocgenes function you must have Plink and ANNOVAR installed. 
Therefore, before explaining the operation of the function we will give the basic details for the installation of the tools.

## Plink

To download Plink we can do it from the link: https://www.cog-genomics.org/plink2  

We download the version for our operating system, in our case Linux 64-bit and decompress
the plink file in the directory where we want to leave it.

## ANNOVAR  

To download ANNOVAR we can do it from the link: http://annovar.openbioinformatics.org/en/latest/user-guide/download/#-for-gene-based-annotation  

First, we have to sign in, then we receive an email in which we have the following link: http://www.openbioinformatics.org/annovar/download/0wgxR2rIVP/annovar.latest.tar.gz  
Once we have downloaded ANNOVAR we unzip the file. You will see that you have a folder called annovar where there are several Perl 
files with the suffix pl. (Note that if you have already added the ANNOVATE path to the executable path from  
your system, then typing annotate_variation.pl would be valid instead of typing perl annotate_variation.pl). 
First, we need to download the appropriate database files using annotate_variation.pl, we must execute in the terminal 
the following commands:    

annotate_variation.pl -buildver hg19 -downdb -webfrom annovar refGene humandb/  

annotate_variation.pl -buildver hg19 -downdb cytoBand humandb/  

annotate_variation.pl -buildver hg19 -downdb -webfrom annovar exac03 humandb/   

annotate_variation.pl -buildver hg19 -downdb -webfrom annovar avsnp147 humandb/   

annotate_variation.pl -buildver hg19 -downdb -webfrom annovar dbnsfp30a humandb/  

