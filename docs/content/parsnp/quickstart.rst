Quickstart
==========

Download, install & run
-----------------------

Parsnp is distributed as a precompiled binary that should be devoid of external dependencies (all included in dist). The four steps below represent the fastest way to start using the software:

1. wget ftp://ftp.cbcb.umd.edu/pub/software/harvest/parsnp-[OSX64/Linux64].tar.gz
2. tar -xvf parsnp-[OSX64/Linux64].tar.gz
3. cd parsnp-[OSX64/Linux64]
4. python INSTALL.py 

Then, on the command-line, run::

./parsnp –p <threads> –d <directory of genomes> –r <ref genome>

Note: This should take anywhere from a few seconds to a few hours complete, from genomes/draft assemblies to newick-formatted tree. 

Output Files
-------------

1. Newick formatted core genome SNP tree: <outputdir>/parsnp.tree
2. SNPs used to infer phylogeny: <outputdir>/parsnp.vcf
4. Gingr formatted binary archive: <outputdir>/parsnp.ggr

External software/packages
------------------------
* FastTree2 (included in distribution)
* Muscle 3.8 (included in distribution)
* Python 2.6+ 
* PhiPack (included in distribution)
* harvest-tools (included in distribution)



