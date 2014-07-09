Quickstart
==========

Download, install & run
-----------------------
Parsnp is distributed as a precompiled binary that should be devoid of external dependencies (all included in dist). The three steps below represent the fastest way to start using the software:

1. wget ftp://ftp.cbcb.umd.edu/pub/software/harvest/parsnp-[OSX64/Linux64].tar.gz
2. tar -xvf parsnp-[OSX64/Linux64].tar.gz
3. cd parsnp-[OSX64/Linux64]

Then, on the command-line, run::

./parsnp –p <threads> –d <directory of genomes> –r <ref genome>

Note: This should take anywhere from a few seconds to a few hours complete, from genomes/draft assemblies to newick-formatted tree. 

Output Files
-------------
#. Newick formatted core genome SNP tree: $outputdir/parsnp.tree
#. SNPs used to infer phylogeny: $outputdir/parsnp.vcf
#. Gingr formatted binary archive: $outputdir/parsnp.ggr

Included external software/packages
------------------------
* FastTree2 : http://meta.microbesonline.org/fasttree
* Muscle : http://www.drive5.com/muscle
* PhiPack : http://www.maths.otago.ac.nz/~dbryant/software.html




