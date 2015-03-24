Quickstart
==========

Note: If you are currently using a Parsnp version prior to **v1.2** you should update to use the latest release (currently v1.2). The latest release includes a critical fix for FastTree2; see http://darlinglab.org/blog/2015/03/23/not-so-fast-fasttree.html for further details.

Before you run
---------------

   1. MUMi based recruitment is useful for quickly identifying clades of closely related genomes from a genomic DB
   
      * However, it is conservative and can under recruit genomes
      * To force inclusion of all genomes in a given directory, use the `-c` flag.
      
   2. The precompiled binaries are created using Pyinstaller and packaged as a single file:
   
      * The most likely cause for failure is a lack of free space in the /tmp directory. By default, PyInstaller will search a standard list of directories and sets tempdir to the first one which the calling user can create files in. 
      
      * The list of directories where the archive will be extracted:
      
         - The directory named by the TMPDIR environment variable.
         - The directory named by the TEMP environment variable.
         - The directory named by the TMP environment variable.

Download, install & run
-----------------------
Parsnp is distributed as a precompiled binary that should be devoid of external dependencies (all included in dist). The three steps below represent the fastest way to start using the software:

On OSX:
"""""""
  1. wget https://github.com/marbl/parsnp/releases/download/v1.2/parsnp-OSX64-v1.2.tar.gz
  2. tar -xvf parsnp-OSX64-v1.2.tar.gz

On Linux:
"""""""""

  1. wget https://github.com/marbl/parsnp/releases/download/v1.2/parsnp-Linux64-v1.2.tar.gz
  2. tar -xvf parsnp-Linux64-v1.2.tar.gz

Basic usage:
""""""""""""

  From command-line::
  
     parsnp –p <threads> –d <directory of genomes> –r <ref genome>

Advanced usage:
"""""""""""""""

Parsnp quick start for three example scenarios.

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

Command-line parameters:
"""""""""""""""""""""""""

Input/output::

 -c = <flag>: (c)urated genome directory, use all genomes in dir and ignore MUMi? (default = NO)
 -d = <path>: (d)irectory containing genomes/contigs/scaffolds
 -r = <path>: (r)eference genome (set to ! to pick random one from genome dir)
 -g = <string>: Gen(b)ank file(s) (gbk), comma separated list (default = None)
 -o = <string>: output directory? default [./P_CURRDATE_CURRTIME]
 -q = <path>: (optional) specify (assembled) query genome to use, in addition to genomes found in genome dir (default = NONE)

   
MUMi::

 -U = <float>: max MUMi distance value for MUMi distribution 
 -M = <flag>: calculate MUMi and exit? overrides all other choices! (default: NO)
 -i = <float>: max MUM(i) distance (default: autocutoff based on distribution of MUMi values)
  
MUM search::

 -a = <int>: min (a)NCHOR length (default = 1.1*Log(S))
 -C = <int>: maximal cluster D value? (default=100)
 -z = <path>: min LCB si(z)e? (default = 25)
  
LCB alignment::

 -D = <float>: maximal diagonal difference? Either percentage (e.g. 0.2) or bp (e.g. 100bp) (default = 0.12)
 -e = <flag> greedily extend LCBs? experimental! (default = NO)
 -n = <string>: alignment program (default: libMUSCLE)
 -u = <flag>: output unaligned regions? .unaligned (default: NO)
  
Recombination filtration::

 -x = <flag>: enable filtering of SNPs located in PhiPack identified regions of recombination? (default: NO)
  
Misc::

 -h = <flag>: (h)elp: print this message and exit
 -p = <int>: number of threads to use? (default= 1)
 -P = <int>: max partition size? limits memory usage (default= 15000000)
 -v = <flag>: (v)erbose output? (default = NO)
 -V = <flag>: output (V)ersion and exit

Output Files
-------------

#. Newick formatted core genome SNP tree: $outputdir/parsnp.tree
#. SNPs used to infer phylogeny: $outputdir/parsnp.vcf
#. Gingr formatted binary archive: $outputdir/parsnp.ggr
#. XMFA formatted multiple alignment: $outputdir/parsnp.xmfa

Included external software/packages
------------------------

* FastTree2 : http://meta.microbesonline.org/fasttree
* Muscle : http://www.drive5.com/muscle
* PhiPack : http://www.maths.otago.ac.nz/~dbryant/software.html




