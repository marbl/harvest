Tutorial
========

`Parsnp download instructions <http://harvest.readthedocs.org/en/latest/content/parsnp/quickstart.html>`_

To further demonstrate the functionality of Parsnp we have prepared two small tutorial datasets. The first dataset is a MERS coronavirus outbreak dataset involving 49 isolates.
The second dataset is a selected set of 31 Streptococcus pneumoniae genomes. Both of these datasets should run on modestly equipped laptops in a few minutes.

   1) 49 MERS Coronavirus genomes
   
      * Download genomes: 
      
         * :download:`gzipped tarball <mers_examples.tar.gz>` 
    
      * Run parsnp with default parameters ::
      
         ./parsnp -g ./ref/EMC_2012.gbk -d ./mers49 -c
         
      * Command-line output
      
      .. image:: run_mers.cmd1.png

      * Visualize with Gingr :download:`GGR <run_mers.gingr1.ggr>`
      
      .. image:: run_mers.gingr1.png
          :target: https://raw.githubusercontent.com/marbl/harvest/master/docs/content/parsnp/run_mers.gingr1.png

      * Configure parameters
      
         - 95% of the reference is covered by the alignment. This is <100% mainly due to a 1kbp unaligned region from 26kbp to 27kbp.
         - To force alignment across large collinear regions, use the `-C` maximum distance between two collinear MUMs::
         
            ./parsnp -g ./ref/EMC_2012.gbk -d ./mers49 -C 1000 -c
            
      * Visualize again with Gingr :download:`GGR <run_mers.gingr2.ggr>`
      
         - By adjusting the `-C` parameter, this region is no longer unaligned, boosting the reference coverage to 97%.
         
         .. image:: run_mers.gingr2.png
            :target: https://raw.githubusercontent.com/marbl/harvest/master/docs/content/parsnp/run_mers.gingr2.png
        
      * Zoom in with Gingr for nucleotide view of region
      
         - On closer inspection, a large stretch of N's in Jeddah isolate C7569 was the culprit
         
         .. image:: run_mers.gingr3.png
            :target: https://raw.githubusercontent.com/marbl/harvest/master/docs/content/parsnp/run_mers.gingr3.png
         
      * Inspect Output:
      
         * Multiple alignment: :download:`XMFA <runm1.xmfa>` 
         * SNPs: :download:`VCF <runm1.vcf>`
         * Phylogeny: :download:`Newick <runm1.tree>`
 
   2) 31 Streptococcus pneumoniae genomes

      * Download genomes: 
      
         * :download:`gzipped tarball <strep31.tar.gz>` 
    
      * Run parsnp ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads>
         
      * Command-line output:
      
          .. image:: run1.png

      * Force inclusion of all genomes (-c) ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads> -c
      
     * Command-line output:
      
          .. image:: run2.png

      * Visualize with Gingr :download:`GGR <run_strep.gingr1.ggr>`
      
          .. image:: run1.gingr.png
             :target: https://raw.githubusercontent.com/marbl/harvest/master/docs/content/parsnp/run1.gingr.png

      * Enable recombination detection/filter (-x) ::
      
         ./parsnp -r ./strep31/NC_011900.fna -d ./strep31 -p <num threads> -c -x

      * Re-visualize with Gingr :download:`GGR <run_strep.gingr1.ggr>`
      
         * Bootstrap values have improved after running recombination filter; columns with filtered SNPs are displayed in image:
          .. image:: run2.gingr.png
             :target: https://raw.githubusercontent.com/marbl/harvest/master/docs/content/parsnp/run2.gingr.png

      * Inspect Output:
      
         * Multiple alignment: :download:`XMFA <runs1.xmfa>` 
         * SNPs: :download:`VCF <runs1.vcf>`
         * Phylogeny: :download:`Newick <runs1.tree>`
