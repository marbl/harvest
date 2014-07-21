Tutorial
========

To further demonstrate the functionality of Parsnp we have prepared two small tutorial datasets. The first dataset is a MERS coronavirus outbreak dataset involving 42 isolates.
The second dataset is a selected set of 31 Streptococcus pneumoniae genomes. Both of these datasets should run on modestly equipped laptops in a few minutes.

   1) 42 MERS Coronavirus genomes
   
      * Download genomes: 
      
         * :download:`gzipped tarball <mers42.tar.gz>` 
    
      * Run parsnp ::
      
         ./parsnp -r ./mers42/England-Qatar_2012.fna -d ./mers42
         
      * Command-line output ::
      
      .. image:: runm1.png

      * Visualize with Gingr::
      
      .. image:: runm1.gingr.png

      * Inspect Output:
      
         * Multiple alignment: :download:`XMFA <runm1.xmfa>` 
         * SNPs: :download:`VCF <runm1.vcf>`
         * Phylogeny: :download:`Newick <runm1.tree>`
 
   2) 31 Streptococcus pneumoniae genomes

      * Download genomes: 
      
         * :download:`gzipped tarball <strep31.tar.gz>` 
    
      * Run parsnp ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads>
         
      * Example output:
      
          .. image:: run1.png
      
      * Force inclusion of all genomes (-c) ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads> -c
      
     * Command-line output:
      
          .. image:: run2.png

      * Visualize with Gingr
      
          .. image:: run1.gingr.png

      * Enable recombination detection/filter (-x) ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads> -c -x

      * Re-visualize with Gingr
      
          .. image:: run2.gingr.png
