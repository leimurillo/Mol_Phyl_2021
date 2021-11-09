# **Dataset Manipulation**

## **Introduction**

In this section we will learn to download genetic sequence information from online databases (i.e. Genbank) and generate a dataset. Later on, by following tutorials, you will align this dataset file and convert it to different alignment file formats. We will also learn here how to convert between different formats used in phylogenetic programs and the main differences between these formats.

## **Download the data**

Using a web browser, you need to navigate to the NCBI’s Genbank. Even if the [link]( https://www.ncbi.nlm.nih.gov/genbank/) is not easy to remember, googling basically any keyword combination containing Genbank will bring you to the NCBI quite easily. In Genbank each sequence entry has a unique identification code called ***accession number***. For this exercise, you need to download the sequences from few genes of the following accession numbers which correspond to mitochondrial genome entries.

| # | Accession Number | Organism name | 
|---|---|---|
| 1 | KP202271 | Acinonyx jubatus |
| 2 | KP202272 | Caracal caracal |
| 3 | KX265095 | Catopuma badia | 
| 4 | KX265096 | Catopuma badia |
| 5 | KP271500 | Catopuma temminckii |
| 6 | FCU20753 | Felis catus | 
| 7 | NC_028307 | Felis chaus |
| 8 | KR132580 | Felis margarita | 
| 9 | KP202277 | Felis nigripes | 
| 10 | KP202273 | Felis silvestris bietis |
| 11 | KP202275 | Felis silvestris lybica |
| 12 | KP202282 | Leopardus colocolo | 
| 13 | KP202292 | Leopardus geoffroyi | 
| 14 | KP202293 |  Leopardus guigna | 
| 15 | KP202294 | Leopardus jacobita |
| 16 | KP202284 | Leopardus pardalis |
| 17 | KP202287 | Leopardus tigrinus | 
| 18 | KP202288 | Leopardus tigrinus | 
| 19 | KP202289 | Leopardus	wiedii |
| 20 | KP202286 | Leptailurus	serval | 
| 21 | KR132581 | Lynx	lynx |
| 22 | KX911367 | Lynx	pardinus |
| 23 | KP202285 | Lynx	rufus | 
| 24 | DQ257669 | Neofelis	nebulosa | 
| 25 | KP202291 | Neofelis	nebulosa | 
| 26 | KP202295 | Otocolobus	manul  | 
| 27 | KC834784 | Panthera	leo persica |
| 28 | KU234271 | Panthera	leo persica | 
| 29 | KX258451 | Panthera	leo spelaea |
| 30 | KX258452 | Panthera	leo spelaea |
| 31 | KP001494 | Panthera	leo | 
| 32 | KP001495 | Panthera	leo | 
| 33 | KF483864 | Panthera	onca | 
| 34 | KM236783 | Panthera	onca |
| 35 | KKJ866876 | Panthera	pardus japonensis |
| 36 | KP001507 | Panthera	pardus | 
| 37 | MH124079 | Panthera	tigris altaica |
| 38 | JF357972 | Panthera	tigris corbetti |
| 39 | JF357970 | Panthera	tigris sumatrae |
| 40 | KJ508413 | Panthera	tigris |
| 41 | EF551004 | Panthera	uncia | 
| 42 | KP202269 | Panthera	uncia |
| 43 | KP202263 | Pardofelis	marmorata | 
| 44 | KT288227 | Pardofelis	marmorata | 
| 45 | HM185183 | Prionailurus	bengalensisa | 
| 46 | KR135743 | Prionailurus	planiceps |
| 47 | KR135744 | Prionailurus	rubiginosus | 
| 48 | KR135742 | Prionailurus	viverrinus | 
| 49 | KP202261 | Puma	concolor | 
| 50 | KP202279 | Puma	yagouaroundi |

Pictures of the species used to generate the sequences above.
<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Cats.png" alt="Cats" width="800"></p>




Opening the [link]( https://www.ncbi.nlm.nih.gov/genbank/) provided earlier you can see the following (slight differences may exist due to different web browsers and operating systems and the position of the planets and …).


<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank1.png" alt="Genbank1" width="800"></p>


In the red rectangle you see a list option which should be on ***Nucleotide***. Clicking on the list you can see other repositories offered by NCBI website. Here we are going to create a dataset of nucleotide sequences of three protein coding genes, so we chose the ***Nucleotide*** option. Remember that these two markers being protein coding genes, allow us to create also ***Amino Acid*** datasets. *Do you know why we stay with nucleotides in this case? Wich option allows you to create an amino acid dataset?*

Now pick an accession number from the list and hit search. You should see something similar to this picture:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank2.png" alt="Genbank2" width="800"></p>

Take a look at it. Try to decipher different parts of it. Now look at the 2 red rectangles on top of the picture. The one on the left where you can read ***GenBank*** is the format of the information. And the other rectangle ***Send to:*** create a downloadable file. Click on it. Choose ***Complete Record***, ***File*** under *Choose Destination* and finally in *format:* choose ***FASTA***. 

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank3.png" alt="Genbank3" width="800"></p>

Now ***Create File***! And *Voila!* Congratulations, now you have downloaded your first Fasta file.

Now download all sequences for each gene separately. ***IMPORTANT TIP*** Do not download each accession number separately! Go to this link ([www.ncbi.nlm.nih.gov/sites/batchentrez](https://www.ncbi.nlm.nih.gov/sites/batchentrez)) and follow the instructions for a batch download ;) Also remember to change the name of your files to the name of their genes. Now you should have these 4 files:

```
ATP6.fasta
COI.fasta
Cytb.fasta
ND5.fasta
```

---------

Now lets take a look at the *FASTA* files we have created. Open any of them in your (prefered) text editor. (Here I have used TextWrangler!)

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/FastaFile.png" alt="FastaFile" width="800"></p>

As you can see, each entry is something similar to this:

```
>AF412762.1 Araschnia levana voucher NW39-2 wingless (wg) gene, partial cds
TCCTGCACCGTTAAAACTTGTTGGATGAGGCTGCCCAGTTTTCGCTCCGTAGGTGATGCGCTAAAAGATC
GCTTCGATGGAGCGTCGCGGGTCATGATGCCCAATACTGAAATCGAAGCACCCGCACAGCGAAATGACGC
ATCGCCTCATCGAGTTCCAAGACGAGATCGGTACAGATTCCAGCTTCGACCGCACAATCCCGATCATAAA
ACACCGATTGCAAAAGACCTAGTCTACCTTGAATCATCACCAGGTTTTTGTGAGAAAAACCCGAGGCTGG
GCATTCCCGGCACACACAACGATACGAGCATCGGCGTCGACGGTTGCGATCTTATGTGTTGTGGTCGTGG
TTACCGTACTGAAACAATGCTTGTTGTGG

```

The line starting with `>` in a fasta file is a header for the sequence. Practically all programs will have problems with how Genbank have created these fasta files. So in your text editor go and modify the name of each sequence to keep only the organism name. Remember that an empty space is not allowed in the name! Replace it with an underscore `_`. You should have exactly the same header as bellow now.


```
>Araschnia_levana
TCCTGCACCGTTAAAACTTGTTGGATGAGGCTGCCCAGTTTTCGCTCCGTAGGTGATGCGCTAAAAGATC
GCTTCGATGGAGCGTCGCGGGTCATGATGCCCAATACTGAAATCGAAGCACCCGCACAGCGAAATGACGC
ATCGCCTCATCGAGTTCCAAGACGAGATCGGTACAGATTCCAGCTTCGACCGCACAATCCCGATCATAAA
ACACCGATTGCAAAAGACCTAGTCTACCTTGAATCATCACCAGGTTTTTGTGAGAAAAACCCGAGGCTGG
GCATTCCCGGCACACACAACGATACGAGCATCGGCGTCGACGGTTGCGATCTTATGTGTTGTGGTCGTGG
TTACCGTACTGAAACAATGCTTGTTGTGG

```

Now save the files adding `2` after the name of the genes. You should have the following files now:


```
ATP6.fasta
COI.fasta
Cytb.fasta
ND5.fasta
```

Now we can proceed to the next tutorial to learn about Alignment Methods. But before lets take a look at our sequence files in a graphical interface specifically designed to visualize sequences and alignments, ***Aliview***.

Open the program, click on file, Open File and find any of the last fasta files you have created, for example `Wingless2.fasta`. You should see something like this.

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021//blob/main/Tutorials/1.DatasetManipulation/Aliview.png" alt="Aliview" width="800"></p>

Before moving on, consider what this file looks like. Very few sites look  ***aligned***, right? This a quite small dataset of relatively conserved sequences, so you can easily find patterns within the file and you should be able to align it by hand given enough time with no major problems. We will check our alignment once we obtain it in this program again.

Now if you click again on `File` you will see something like this:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021//blob/main/Tutorials/1.DatasetManipulation/Aliview2.png" alt="Aliview2" width="500"></p>

As you can see this program allow us to convert/save a sequence file in many different formats which can be used in different programs. Remember this for when we are going to convert the alignment to other file formats than fasta.

