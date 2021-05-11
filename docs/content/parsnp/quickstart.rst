Quickstart
==========


Basic usage:
""""""""""""

  From command-line::
  
     parsnp –p <threads> –d <directory of genomes> –r <ref genome>

Advanced usage:
"""""""""""""""

Parsnp quick start for three example scenarios. Note that the argument to `-d` can also be a list of fasta files, for example `-d genome_dir/*.fasta`.

With reference & genbank file::
   
   parsnp -g <reference_replicon1,reference_replicon2,..> -d <genome_dir> -p <threads> 
   
NOTE: 

    1. Genbank files are currently expected to have GI numbers for indexing. This means custom Genbank files (not downloaded from NCBI) will not have annotations appear in Gingr, though the alignment should still work. The dependency on GIs is expected to change in future versions.
    2. GenBank files can only be specific for the reference genome
    3. -g and -r are mutually exclusive; you can either provide a fasta file for your reference genome, or GenBank file, but not both.
    4. All non-reference genomes are captured with the -d parameter. These genomes *must* be in fasta format and located within the specified directory.

With reference but without genbank file::
   
   parsnp -r <reference_genome> -d <genome_dir> -p <threads> 
   
Autorecruit reference to a draft assembly::
   
   parsnp -q <draft_assembly> -d <genome_db> -p <threads> 

Output Files
-------------

#. Newick formatted core genome SNP tree: $outputdir/parsnp.tree
#. SNPs used to infer phylogeny (with the `--vcf` flag: $outputdir/parsnp.vcf
#. Gingr formatted binary archive: $outputdir/parsnp.ggr
#. XMFA formatted multiple alignment: $outputdir/parsnp.xmfa

