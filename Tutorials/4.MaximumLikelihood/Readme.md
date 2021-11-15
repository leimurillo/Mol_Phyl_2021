# Maximum-Likelihood Phylogenetic Inference


## **IQTREE2** 

In this tutorial, we will analyse the `15genes.phy` dataset with one of the fastest maximum-likelihood based phylogenetic programs [IQ-TREE2](http://www.iqtree.org) ([Nguyen et al. 2015](https://academic.oup.com/mbe/article/32/1/268/2925592)). IQ-TREE2 for Windows, MacOSX and Linux can be downloaded [here](http://www.iqtree.org/#download), you can install it on your personal computer.


**Command line instructions and Tree inference**

Tree Inference is one of the most frequently used features of IQ-TREE and allows users to carry out phylogenetic analysis on a multiple sequence alignment (MSA). In the most basic case, no more than an MSA file is required to submit the job. Without further input, IQ-TREE will run with the default parameters and auto-detect the sequence type as well as the best-fitting substitution model. Additionally, Ultrafast Bootstrap ([Hoang et al., 2018](https://academic.oup.com/mbe/article/35/2/518/4565479)) and the SH-aLRT branch test ([Guindon et al., 2010](https://academic.oup.com/sysbio/article/59/3/307/1702850)) will be performed.


Go into IQTREE2 folder by entering in the terminal

cd folder/iqtree-2.1.3-MacOSX (assuming you dowloaded iqtree-2.1.3-MacOSX, and only if iqtree executable was not copied into system search path).

**Command reference**

iqtree2 funtion= will call the executable

`-s`: will call the alignment

`-p`: is your patition file, each partition to have its own evolution rate.

`-m MFP+MERGE`: will search for the evolutionary models of your partitions.

`-bb`: will perfom Ultrafast Boostrap.

`-arlt`: will perform the SH-aLRT test.

`-rcluster`: Specify the percentage for the relaxed clustering algorithm (Lanfear et al., 2014) to speed up the computation instead of the default slow greedy algorithm.

`-bnni`: reduce the risk of overestimating branch supports with UFBoot due to severe model violation.


1. Now you can try to run a simple analysis by entering


`iqtree2 -s 15genes.phy` 


IQTREE2 will infer a tree from a sequence alignment (file.phy) with the best-fit model automatically selected by ModelFinder.



2. However, to find best partition scheme by possibly merging partitions, followed by tree inference and branches support run an analysis by entering

`iqtree2 -s 15genes.phy -p 3.Partitions15genes.txt -m MFP+MERGE -B 1000 -arlt 1000 -rcluster 10 -bnni`


You should have something similar to this:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/4.MaximumLikelihood/IQTREEb.png" alt="IQTREEb" width="600"></p>

**Congratulations! now that you have ran the analyses, compare the results.**



**Output Files to check**

   Suffix	     
   
- `.iqtree`	     Full result of the run, this is the main report file.

- `.log`	       Run log.

- `.treefile`	   Maximum likelihood tree in NEWICK format, can be visualized with treeviewer programs.

- `.ufboot`      Bootstrap trees.

- `.best_scheme.nex` best partitioning scheme.




# Tree visualization


Open the file `.treefile` retrieved from IQTREE2 and check the support values. The phylogeny should look more or less as shown in the next screenshot.

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/4.MaximumLikelihood/IQTREEc.png" alt="IQTREEc" width="600"></p>

The tree is rooted by default on the first taxon in your dataset or on the longest branch in the dataset. In our case we should reroot the tree on the branch leading to *Asterocampa* (which is our outgroup). In FigTree, click on the branch leading to *Asterocampa* to select it, and then click on the "Reroot" button in FigTree.



**Questions**

1. *Are the UFBoot2 values higher/lower compared to those recovered from the SH-like in IQTREE?*

2. *How are the nodes/relationships supported?*

3. *Take a look at the best partitioning scheme. What are the merged partitions? Can you see any similarity pattern beween the merged partitions?*


----------

**Tree inference on Website (optional if you have not downloaded IQTREE2)**

You can also to try out the IQ-TREE [web server](http://iqtree.cibiv.univie.ac.at/), where you only need to upload an alignment, choose the options and start the analysis.You can either try out the web server with an example alignment by ticking the corresponding box or upload your own alignment file. By clicking on ‘Browse’ a dialog will open where you can select your MSA; the file formats Phylip, Fasta, Nexus, Clustal and MSF are supported.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut1.png" alt="IQTREE" width="600"></p>

After that you can submit the job. If you provide an email address, a notification will be sent to you once the job is finished. In case you don’t specify an email address, you will receive a link in the next step; you can bookmark this link to retrieve your results after the job is finished.


**Model Selection on Website (optional if you have not downloaded IQTREE2)**

IQ-TREE supports a wide range of substitution models for DNA, protein, codon, binary and morphological alignments. In case you do not know which model is appropriate for your data, IQ-TREE can automatically determine the best-fit model for your alignment. Use the Model Selection tab if you only want to find the best-fit model without doing tree reconstruction.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut2.png" alt="IQTREE" width="600"></p>

Like with Tree Inference, the only obligatory input is a multiple sequence alignment. You can either upload your own alignment file or use the example alignment to try out the web server and then submit the job.


**Analysis of Results from webserver**

In the tab Analysis Results you can monitor your jobs. With our example file, a run will only take a few seconds. The results will depend on the server load. For your own alignments the CPU time limit is 24 hours. If you provided an email address when submitting the job, you will get an email once it is finished.

<p align="center"><img src="http://www.iqtree.org/doc/images/tut3.png" alt="IQTREE" width="600"></p>

Once a job is finished, you can select it by checking the corresponding box and then downloading the selected jobs as a zip file. This zip file will contain the results of your run, including the Run Log and the Full Result which are also accessible in the webserver.

   Suffix	     Output File Explanation
   
- `.iqtree`	     Full result of the run, this is the main report file.

- `.log`	       Run log.

- `.treefile`	   Maximum likelihood tree in NEWICK format, can be visualized with treeviewer programs.

- `.svg`	       Graphical tree representation in SVG format, done with ete view.

- `.pdf`	       Graphical tree representation in PDF format, done with ete view.

- `.contree`	   Consensus tree with assigned branch supports where branch lengths are optimized on the original alignment; printed if Ultrafast Bootstrap is selected.

- `.ckp.gz`	    Checkpoint file; included if a job was stopped because of RAM/CPU limits.

This tutorial was retrieved from the [IQTREE Web-Server](http://www.iqtree.org/doc/Web-Server-Tutorial)







