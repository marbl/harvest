File formats
============

The flowchart below describes the various file formats that can be imported or
exported to/from Gingr (or the `harvesttools` command line utility).

.. image:: flowchart.png

* Alignments
	* Core only: The Gingr file format stores core alignments, or alignments that involve all genomes. When alignments are loaded, blocks that are not core will be discarded.
	* Multi-fasta: This format does not store rearrangement information, so the alignment is treated as a single LCB.
* References
	* XMFA files can be accompanied by Fasta reference files to provide sequence between LCBs and to allow Genbank annotations (which must have matching GI numbers) to be loaded later. Genbank files that contain sequence can also be used as references.
	* Multi-fasta alignments will use the first sequence as the reference. Genbank annotations can be loaded later if the GIs match.
* Variants
	* VCF files must be imported with a Fasta reference. Since VCF does not store complete alignment information, any insertions larger than one base will be replaced by an LCB boundary when importing. If a genotype is diploid or polyploid, only the first haplotype is used in the multi-alignment (the others are ignored). Symbolic alleles and breakends are currently unsupported and will also be ignored. Note that any information ignored when importing (which also includes  besides Variants can be output as a simple VCF file that contains haploid genotypes, qualities, and filters, but ignores indels are currently ignored when writing.
	* The multi-fasta SNP output is the same format as multi-fasta alignments, but only contains columns with unfiltered ("PASS") variants (like a Mauve SNP file). This is useful for generating phylogenetic trees, but does not contain positional information or rearrangements.
