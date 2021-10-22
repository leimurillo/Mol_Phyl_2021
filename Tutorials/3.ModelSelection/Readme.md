# **Model Selection**


In the first two tutorials you have learned to download various gene sequences from Genbank and align and concatenate them to create the dataset we want to work on for the rest of the course. You also heard about differences between file formats and saw how to create the needed formats. For the next tutorial, we are going to use *ModelFinder* to find the best partitioning scheme for our dataset and also the best models for each partition.

First remember that our final dataset, `COI_EF1a_Wingless.fasta` was saved as a fasta format (If you did not manage to generate this file, go to ***Molecular-systematics-course/Data/*** and download `2_COI_EF1a_Wingless.fasta`). Now open *Aliview* and open this file. You should have something similar to this:

<p align="center"><img src="https://github.com/niklas-w/Molecular-systematics-course/blob/master/Tutorials/3.ModelSelection/Aliview3.png" alt="Aliview3" width="800"></p>

Now I want you to save a \*.phy and a \.nex alignment file with the name **Dataset**. Use the options "***Save as Nexus***" and "***Save as Phylip (full names & padded)***" as seen in the next picture (both options marked with a red rectangle):

<p align="center"><img src="https://github.com/niklas-w/Molecular-systematics-course/blob/master/Tutorials/3.ModelSelection/Aliview5.png" alt="Aliview5" width="800"></p>

You should have these two files now:

```
Dataset.phy
Dataset.nex
```

For this tutorial we are going to use the `Dataset.phy` and a command file that we are going to create together. 







