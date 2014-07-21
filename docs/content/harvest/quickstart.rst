Quickstart
==========

Download, install & run
-----------------------
harvest-tools is distributed as a precompiled binary. The three steps below represent the fastest way to start using the software:

On OSX:
"""""""
  1. wget ftp://ftp.cbcb.umd.edu/pub/software/harvest/harvesttools-OSX64.gz
  2. tar -xvf harvesttools-OSX64.tar.gz

On Linux:
"""""""""

  1. wget ftp://ftp.cbcb.umd.edu/pub/software/harvest/harvesttools-Linux64.gz
  2. tar -xvf harvesttools-Linux64.tar.gz

Basic usage:
""""""""""""

  From command-line::
  
     harvest-tools –x <input xmfa> -f <input reference fasta> -g <reference genbank formatted annotations> -n <newick formatted tree>

Advanced usage:
"""""""""""""""

harvest-tools quick start for three example scenarios.

With reference & genbank file as input::
   
   harvest-tools -g <reference_genbank_file1,reference_genbank_file2,..> -r <reference fasta file> -x <XMFA file> -o hvt.ggr 

With harvest-tools file as input, XMFA output::
   
   harvest-tools -i input.ggr -X output.xmfa
 
With harvest-tools file as input, fasta formatted SNP file as output::
   
   harvest-tools -i input.ggr -S output.snps

Command-line parameters:
"""""""""""""""""""""""""
   - -b: <bed filter intervals>,<filter name>,"<description>"
   - -B: <output backbone intervals>
   - -f: <reference fasta>
   - -F: <reference fasta out>
   - -g: <reference genbank>
   - -h: (show this help)
   - -i: <harvest input>
   - -m: <multi-fasta alignment input>
   - -n: <Newick tree input>
   - -N: <Newick tree output>
   - --midpoint-reroot
   - -o: <hvt output>
   - -q: (quiet mode)
   - -S: <output for multi-fasta SNPs>
   - -v: <VCF input>
   - -V: <VCF output>
   - -x: <xmfa alignment file>
   - -X: <output xmfa alignment file>

Primary output files
-------------

#. Compressed binary archive (GGR)





