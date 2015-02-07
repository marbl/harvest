Quickstart
==========

Before you run
--------------
   1. harvest-tools VCF outputs indels in non standard format:
   
      * currently column based, not row based. excluding indel rows (default behavior) converts file into valid VCF format.
      * this will be updated in future version
       
   2. Genbank annotation input:
   
      * Multiple Genbank files must be specified with multiple `-g` parameters
      * In addition, genome identifier (gi) must match the header of the reference fasta file
       
Download, install & run
-----------------------
harvest-tools is distributed as a precompiled binary. The three steps below represent the fastest way to start using the software:

On OSX:
"""""""
  1. wget https://github.com/marbl/harvest-tools/releases/download/v1.2/harvesttools-OSX64-v1.2.zip
  2. tar -xvf harvesttools-OSX64-v1.2.tar.gz

On Linux:
"""""""""

  1. wget https://github.com/marbl/harvest-tools/releases/download/v1.2/harvesttools-Linux64-v1.2.tar.gz
  2. tar -xvf harvesttools-Linux64-v1.2.tar.gz

Basic usage:
""""""""""""

  From command-line::
  
     harvesttools –x <input xmfa> -f <input reference fasta> -g <reference genbank formatted annotations> -n <newick formatted tree>

Advanced usage:
"""""""""""""""

harvest-tools quick start for three example scenarios.

With reference & genbank file as input::
   
   harvesttools -g <reference_genbank_file1> -r <reference fasta file> -x <XMFA file> -o hvt.ggr 

With harvest-tools file as input, XMFA output::
   
   harvesttools -i input.ggr -X output.xmfa
 
With harvest-tools file as input, fasta formatted SNP file as output::
   
   harvesttools -i input.ggr -S output.snps

Command-line parameters:
"""""""""""""""""""""""""
   - -i <Gingr input>
   - -b <bed filter intervals>,<filter name>,"<description>"
   - -B <output backbone intervals>
   - -f <reference fasta>
   - -F <reference fasta out>
   - -g <reference genbank>
   - -a <MAF alignment input>
   - -m <multi-fasta alignment input>
   - -M <multi-fasta alignment output (concatenated LCBs)>
   - -n <Newick tree input>
   - -N <Newick tree output>
   - --midpoint-reroot (reroot the tree at its midpoint after loading)
   - -o <Gingr output>
   - -S <output for multi-fasta SNPs>
   - -u 0/1 (update the branch values to reflect genome length)
   - -v <VCF input>
   - -V <VCF output>
   - -x <xmfa alignment file>
   - -X <output xmfa alignment file>
   - -h (show this help)
   - -q (quiet mode)

Primary output files
-------------

#. Compressed binary archive (GGR)





