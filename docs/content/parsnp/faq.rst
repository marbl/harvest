FAQs
====

Q. **What is Parsnp ?**

 A. Parsnp takes both draft and finished genomes of closely related strains as input, performs conservative core genome alignment and as output returns multi-alignments (XMFA), variants (VCF), core genome phylogeny (Newick) and Gingr input format (GGR).  

Q. **Why should I use Parsnp?**

 A. The main advantages of Parsnp over alternative approaches is robust filtration of variant (SNP) calls, multiple alignments as output and superior speed. Parsnp can align 200-300 bacterial strains in <30 minutes on a 16-core server and ~1000 in a couple of hours.

Q. **Why should I *not* use Parsnp?**

 A. If you are interested in pan genome/whole genome alignment, existing tools for the job that perform well include Mauve, Mugsy, among others. In addition, Parsnp is tailored for intraspecific genome analysis (outbreak analysis of a pathogen, etc). One main limitation of Parsnp is that it cannot handle subsets (core genome only) and is not as sensitive as existing methods.

Q. **How can I visualize the results?**

 A. Gingr (http://github.com/marbl/gingr) can open Parsnp output and provide an interactive display of multi-alignments, variants and the phylogenetic tree estimated from the core genome alignment.

Q. **What % of genome X is aligned? What is the core genome alignment size?**

 A. Within the log output, there are coverage values listed that individually indicate the percentage of a given genome that is included in the core genome alignment. Note, this includes the Muscle aligned-regions plus the maximal unique matches (MUMs). The core genome alignment size can then be calculated by multiplying the coverage value, for a given genome, by its length.

Q. **Only a small percentage (<40%) of the reference genome covered by the alignments, huh?**

 A. Parsnp is a conservative core genome alignment method that necessarily requires that all genomes are present in each aligned regions. The focus is on aligning 1000s of closely related bacterial strains quickly while maintaining sensitivity comparable to existing WGA methods. In additon, the core genome has been shown to contain as few as 30-40% of the gene content (even in very closely-related clades) due to reductive genome evolution and/or a large accessory genome (with plenty of IS/phage elements). However, for increased sensitivity w.r.t aligned regions, and alignments containing subsets, both Mugsy and Mauve are terrific tools for the job.

Q. **I am not sure which reference genome to choose, help!**

 A. Since the core necessarily includes all genomes, the choice of reference does not matter (with a couple important exceptions, continue reading). Feel free to use the parameter ‘-r !’ to randomly select a reference if you are feeling indecisive or if all of the genomes contained in the genome directory are of similar quality. Typically, finished/closed genomes are used a the reference strain to ensure they are high-quality and do not contain assembly artifacts or contaminant.

Q. **How are the genomes selected from the input directory? Not all of the genomes I wanted included are in the tree!**

 A. By default, parsnp calculates the MUMi distance between the reference and each of the genomes in the genome directory. All genomes with MUMi distance <= 0.01 are included, all others are discarded. To force all genomes present in the genome dir to be included simply include '-c' as a command-line parameter.

Q. **Parsnp fails to report a SNP position output by method X, why is this?**

 A. The goal of parsnp is to capture all informative signals found in the core genome of the specified clade of interest. Any SNPs in regions not shared by all genomes will not reported. Additionally, any SNP found in a likely poorly aligned region would also be discarded. Finally, parsnp does not perform LCB extension and therefore may miss SNPs appearing at the end of locally conserved blocks or clusters. 
