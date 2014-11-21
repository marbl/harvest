Quickstart
==========

Before you run
---------------

   1. To run Gingr OSX, you will need to right click to open and bypass the unsigned developer notice:
   
      * Future releases will be signed
   
Download, install & run
-----------------------
Parsnp is distributed as a precompiled binary that should be devoid of external dependencies (all included in dist). The three steps below represent the fastest way to start using the software:

On OSX:
"""""""
  1. wget https://github.com/marbl/gingr/releases/download/v1.0.1/gingr-OSX64-v1.0.1.zip
  2. unzip gingr-OSX64.app.zip

On Linux:
"""""""""

  1. wget https://github.com/marbl/gingr/releases/download/v1.0.1/gingr-Linux64-v1.0.1.tar.gz
  2. tar -xvf gingr-Linux64-v1.0.1.tar.gz

Basic usage:
""""""""""""

  1. On OSX simply click on Gingr app (right click to bypass unsigned developer notice)
  2. On Linux, simply run::
      ./gingr
  

Browsing a Gingr file
--------------------
* Download :download:`Gingr input file <parsnp.ggr>`

* Open in Gingr (File->Open)

.. image:: ggr.png

* The phylogeny appears on the left. Hover over a clade to highlight and outline the corresponding tracks to the right.

.. image:: clade.png

* Click to zoom in on the clade

.. image:: zoomed.png

* The multiple alignment appears on the right, shown as a SNP heatmap when zoomed out. To see the full alignment, zoom in with the mouse wheel or by selecting a region in the ruler.

.. image:: bases.png

Importing other files
---------------------
* Create a new workspace (File->New)

.. image:: new.png

* Download the data files

  * Alignment: :download:`xmfa <parsnp.xmfa>`
  * Reference: :download:`fasta <england1.fna>` 
  * Annotations: :download:`genbank <england1.gbk>` 
  * Phylogeny: :download:`newick <parsnp.tree>` 

* Open the XMFA alignment (File->Open). Since XMFA files can be accompanied by reference files, the Open dialog will appear. Choose the Fasta file as the reference in this window.

.. image:: open.png

* The preview panes allow you to ensure that the header for the reference is the same as the first sequence in the XMFA. This allows sequences between LCBs to be shown and allows annotations to be added later.

.. image:: xmfa.png

* The track highlighted in blue ("england.gbk.fna.srt") is the current reference for variants. Select a new reference by right-clicking on a track.

.. image:: reref.png

* Next, import the phylogenetic tree (File->Open)

.. image:: tree.png

* Reroot the tree at the midpoint (Tree->Reroot at midpoint)

.. image:: reroot.png

* The tree will now be balanced at the center of the longest path

.. image:: rerooted.png

* Finally, import the annotations (File->Open)

.. image:: annotated.png

* The workspace can be saved to share or return to later (File->Save)
