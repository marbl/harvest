Tutorial
========

To further demonstrate the functionality of Parsnp we have prepared two small tutorial datasets. The first dataset is a MERS coronavirus outbreak dataset involving 42 isolates.
The second dataset is a selected set of 31 Streptococcus pneumoniae genomes. Both of these datasets should run on modestly equipped laptops in a few minutes.

   1) 42 MERS Coronavirus genomes
   
      * Download genomes: 
      
         * :download:`gzipped tarball <mers42.tar.gz>` 
    
      * Run parsnp ::
      
         ./parsnp -r ./mers42/England-Qatar_2012.fna -d ./mers42 -p <num threads>
         
      * Command-line output ::
      
      .. image:: runm1.png

      * Visualize with Gingr::
      
      .. image:: runm1.gingr.png

      * Inspect Output::
      
      XMFA multiple alignment: 
      
      >1:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >2:16-26502 + cluster2 s1:p16
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >3:8-26494 + cluster2 s1:p8
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >4:16-26502 + cluster2 s1:p16
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >5:52-26538 + cluster2 s1:p52
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >6:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >7:48-26534 + cluster2 s1:p48
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >8:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >9:15-26501 + cluster2 s1:p15
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >10:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >11:52-26538 + cluster2 s1:p52
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >12:8-26494 + cluster2 s1:p8
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >13:21-26507 + cluster2 s1:p21
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >14:11-26497 + cluster2 s1:p11
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTCgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >15:21-26507 + cluster2 s1:p21
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >16:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatCGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >17:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaCtaatttgcct
      
      >18:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >19:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >20:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >21:52-26538 + cluster2 s1:p52
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >22:51-26537 + cluster2 s1:p51
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >23:45-26531 + cluster2 s1:p45
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >24:45-26531 + cluster2 s1:p45
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >25:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >26:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >27:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >28:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >29:57-26543 + cluster2 s1:p57
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >30:56-26542 + cluster2 s1:p56
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >31:39-26525 + cluster2 s1:p39
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >32:43-26529 + cluster2 s1:p43
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >33:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaCtaatttgcct
      
      >34:17-26503 + cluster2 s1:p17
      ttttaacgaacttaaatTaaagccctgttgtttagcgtatTGTCgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >35:21-26507 + cluster2 s1:p21
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >36:16-26502 + cluster2 s1:p16
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >37:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >38:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >39:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >40:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct
      
      >41:6-26492 + cluster2 s1:p6
      ttttaacgaacttaaatAaaagccctgttgtttagcgtatTGTTgcacttgtctggtgggattgtggcaTtaatttgcct

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
