Tutorial
========

To further demonstrate the functionality of Parsnp we have prepared two small tutorial datasets. The first dataset is a MERS coronavirus outbreak dataset involving 47 isolates.
The second dataset is a selected set of 31 Streptococcus pneumoniae genomes. Both of these datasets should run on modestly equipped laptops in a few minutes.

   1) 47 MERS Coronavirus genomes
   
      * Step 1: Download genomes: 
      
         * :download:`gzipped tarball <mers47.tar.gz>` 
    
      * Step 2: Run parsnp ::
      
         ./parsnp -r ! -d ./mers47 -p <num threads>
         
      * Step 2: example output ::
      
      .. image:: runm1.png

      * Step 3: Inspect Output::
      
         * XMFA output
         * VCF output
         * Newick output

      * Step 4: Visualize with Gingr::
      
         * GGR file
         * Download Gingr from : 
         * Include image
         * for more details on using Gingr see http:

      * Step 5: Adjusting parameters::
      
         * D parameter, C parameter
         * Explain with image
         * etc

   2) 31 Streptococcus pneumoniae genomes

      * Step 1: Download genomes: 
      
         * :download:`gzipped tarball <strep31.tar.gz>` 
    
      * Step 2: Run parsnp ::
      
         ./parsnp -r ! -d ./strep31 -p <num threads>
         
      * Step 2: example output
      
          .. image:: run1.png
          

      
      * Step 3: Inspect Output::
      
         * XMFA output
         * VCF output
         * Newick output

      * Step 5: Visualize with Gingr

      * Step 6: Retrieve XMFA via harvest-tools 

      * Step 7: Selecting a list of SNPs common to a pair of genomes
