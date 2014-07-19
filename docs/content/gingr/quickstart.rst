Quickstart
==========

Browsing a Gingr file
--------------------
* Download [parsnp.ggr]
* Open in Gingr (File->Open)
* [ggr.png]
* The phylogeny appears on the left. Hover over a clade to highlight and outline the corresponding tracks to the right.
* [clade.png]
* Click to zoom in on the clade
* [zoomed.png]
* The multiple alignment appears on the right, shown as a SNP heatmap when zoomed out. To see the full alignment, zoom in with the mouse wheel or by selecting a region in the ruler.
* [bases.png]

Importing other files
---------------------
* Create a new workspace (File->New)
* [new.png]
* Download the data files
  * Alignment: [parsnp.xmfa]
  * Reference: [england1.fna]
  * Annotations: [england1.gbk]
  * Tree: [parsnp.tree]
* Import the alignment with the refrence (File->Import Alignment (XMFA & Fasta))
* [xmfa.png]
* The track highlighted in blue ("england.gbk.fna.srt") is the current reference for variants. Select a new reference by right-clicking on a track.
* [reref.png]
* Next, import the phylogenetic tree (File->Import tree (Newick))
* [tree.png]
* Reroot the tree at the midpoint (Tree->Reroot at midpoint)
* [reroot.png]
* The tree will now be balanced at the center of the longest path
* [rerooted.png]
* Finally, import the annotations (File->Import annotations (Genbank))
* [annotated.png]
* The workspace can be saved to share or return to later (File->Save)
