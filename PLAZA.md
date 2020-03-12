---


---

<h2 id="plaza">PLAZA</h2>
<h3 id="introduction">Introduction</h3>
<blockquote>
<p>PLAZA is an access point for plant comparative genomics centralizing genomic data produced by different genome sequencing initiatives. It integrates plant sequence data and comparative genomics methods and provides an online platform to perform evolutionary analyses and data mining within the green plant lineage (<em>Viridiplantae</em>).</p>
</blockquote>
<p>PlAZA是一个针对植物比较基因组学研究的在线平台。<br>
基本流程如下图，后续版本又增加了对其它物种的支持。<br>
<img src="http://www.plantcell.org/content/plantcell/21/12/3718/F1.large.jpg" alt="PLAZA"><br>
很多功能是针对单基因做基因家族和Domian分析<br>
<img src="https://i.bmp.ovh/imgs/2020/03/a1f3a885ee76faf3.png" alt="enter image description here"></p>
<h3 id="materials-and-methods">Materials and Methods</h3>
<p>根据一篇Cell的文献，查到了相关评估方法：<br>
<img src="https://i.bmp.ovh/imgs/2020/03/38e247d90ffc1057.png" alt="enter image description here"><br>
<img src="https://i.bmp.ovh/imgs/2020/03/a1af051f5125d4fb.png" alt="enter image description here"></p>
<h4 id="下载相关文件">下载相关文件</h4>
<pre><code>@ wget ftp://ftp.psb.ugent.be/pub/plaza/plaza_public_02_5/coreGF/coreGF_plaza2.5_geneset.py
@ python3 coreGF_plaza2.5_geneset.py -h

usage: CoreGF_Plaza2.5_geneset.py [-h] coreGFs_table blast_output &gt; results.txt
Calculate the CoreGF score using the PLAZA 2.5 core gene families.
positional arguments:
  coreGFs_table  Tab-delimited file containing the coreGFs of Plaza 2.5
  blast_output   Tab-delimited blast output of the annotated gene space
                 (protein or transcript sequences) against the Plaza 2.5
                 proteome.
@ vim coreGF_plaza2.5_monocots.txt
</code></pre>
<p><img src="https://i.bmp.ovh/imgs/2020/03/d1a9afab9ef1fee1.png" alt="enter image description here"><br>
这个是最终的输出结果</p>
<pre><code> @ vim example_coreGFscore_ath_rosids.txt 
</code></pre>
<p><img src="https://i.bmp.ovh/imgs/2020/03/6ace593d37230c67.png" alt="enter image description here"><br>
这个是coreGFs_table</p>
<p>README文件</p>
<pre><code>The coreGF score can be calculated in two steps. 

1) BLAST search

Perform a BLAST search of the annotated protein sequences (BLASTp) or transcript sequences (BLASTx) against the Plaza 2.5 proteome database. 
A preformatted BLAST database has been made available in the ftp coreGF folder (PLAZA_2.5_proteome).
The output should be tab-delimited, with the target locus in the second column. 
All significant BLAST hits should be given as input to the python script.

2) Calculate coreGF score using python script (coreGF_plaza2.5_geneset.py)

Three sets of coreGFs have been defined for different plant lineages (green plants, rosids and monocots) by means of Plaza 2.5.
A table with the selected gene families and their representatives can be found in the supplementals of Van Bel et al., 2012 and are available as text files in the ftp coreGF folder (coreGF_plaza2.5_greenplants.txt, coreGF_plaza2.5_rosids.txt and coreGF_plaza2.5_monocots.txt).
        
This python (v3) script reads the coreGF table and parses the tab delimited blastoutput. 
All BLAST hits are taken into account in search for a hit with the representative sequence of a coreGF.
As each coreGF has a its own weight, the coreGF score is calculated as the sum of weights of the represented coreGFs divided by the total weigth of all coreGFs.
The coreGF score, the number and list of missing coreGFs are written to STDOUT.

Show help: python3 coreGF_plaza2.5_geneset.py -h
Example: python3 coreGF_plaza2.5_geneset.py coreGF_plaza2.5_rosids.txt example_BLASTp_ath_plaza2.5_proteome.txt &gt; example_coreGFscore_ath_rosids.txt
</code></pre>
<h3 id="discussion">Discussion</h3>
<p>总体感觉与BUSCO类似，基于BLAST，前期BLAST的参数选择十分重要。需要手动下载PLAZA的数据库，然后进行Local Blast.<br>
数据库网址：<a href="ftp://ftp.psb.ugent.be/pub/plaza/plaza_public_02_5/coreGF/">ftp://ftp.psb.ugent.be/pub/plaza/plaza_public_02_5/coreGF/</a></p>
<p>Ref:<br>
Veeckman E ,  Ruttink T ,  Vandepoele K . Are We There Yet? Reliably Estimating the Completeness of Plant Genome Sequences[J]. The Plant Cell, 2016, 28(8):tpc.00349.2016.<br>
Proost S ,  Bel M V ,  Sterck L , et al. PLAZA: A Comparative Genomics Resource to Study Gene and Genome Evolution in Plants[J]. Plant Cell, 2009, 21(12):3718-3731.</p>

