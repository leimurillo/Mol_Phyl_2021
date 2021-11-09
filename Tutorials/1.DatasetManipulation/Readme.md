# **Dataset Manipulation**

## **Introduction**

In this section we will learn to download genetic sequence information from online databases (i.e. Genbank) and generate a dataset. Later on, by following tutorials, you will align this dataset file and convert it to different alignment file formats. We will also learn here how to convert between different formats used in phylogenetic programs and the main differences between these formats.

## **Download the data**

Using a web browser, you need to navigate to the NCBI’s Genbank. Even if the [link]( https://www.ncbi.nlm.nih.gov/genbank/) is not easy to remember, googling basically any keyword combination containing Genbank will bring you to the NCBI quite easily. In Genbank each sequence entry has a unique identification code called ***accession number***. For this exercise, you need to download the sequences from few genes of the following accession numbers which correspond to mitochondrial genome entries.

| # | Accession Number | Organism name | 
|---|---|---|
| 1 | KP202271 | *Acinonyx jubatus* |
| 2 | KP202272 | *Caracal caracal* |
| 3 | KX265095 | *Catopuma badia* | 
| 4 | KX265096 | *Catopuma badia* |
| 5 | KP271500 | *Catopuma temminckii* |
| 6 | FCU20753 | *Felis catus* | 
| 7 | NC_028307 | *Felis chaus* |
| 8 | KR132580 | *Felis margarita* | 
| 9 | KP202277 | *Felis nigripes* | 
| 10 | KP202273 | *Felis silvestris bietis* |
| 11 | KP202275 | *Felis silvestris lybica* |
| 12 | KP202282 | *Leopardus colocolo* | 
| 13 | KP202292 | *Leopardus geoffroyi* | 
| 14 | KP202293 | *Leopardus guigna* | 
| 15 | KP202294 | *Leopardus jacobita* |
| 16 | KP202284 | *Leopardus pardalis* |
| 17 | KP202287 | *Leopardus tigrinus* | 
| 18 | KP202288 | *Leopardus tigrinus* | 
| 19 | KP202289 | *Leopardus wiedii* |
| 20 | KP202286 | *Leptailurus serval* | 
| 21 | KR132581 | *Lynx	lynx* |
| 22 | KX911367 | *Lynx	pardinus* |
| 23 | KP202285 | *Lynx	rufus* | 
| 24 | DQ257669 | *Neofelis	nebulosa* | 
| 25 | KP202291 | *Neofelis	nebulosa* | 
| 26 | KP202295 | *Otocolobus	manul*  | 
| 27 | KC834784 | *Panthera	leo persica* |
| 28 | KU234271 | *Panthera	leo persica* | 
| 29 | KX258451 | *Panthera	leo spelaea* |
| 30 | KX258452 | *Panthera	leo spelaea* |
| 31 | KP001494 | *Panthera	leo* | 
| 32 | KP001495 | *Panthera	leo* | 
| 33 | KF483864 | *Panthera	onca* | 
| 34 | KM236783 | *Panthera	onca* |
| 35 | KKJ866876 | *Panthera	pardus japonensis* |
| 36 | KP001507 | *Panthera pardus* | 
| 37 | MH124079 | *Panthera tigris altaica* |
| 38 | JF357972 | *Panthera tigris corbetti* |
| 39 | JF357970 | *Panthera tigris sumatrae* |
| 40 | KJ508413 | *Panthera tigris* |
| 41 | EF551004 | *Panthera uncia* | 
| 42 | KP202269 | *Panthera uncia* |
| 43 | KP202263 | *Pardofelis marmorata* | 
| 44 | KT288227 | *Pardofelis marmorata* | 
| 45 | HM185183 | *Prionailurus bengalensisa* | 
| 46 | KR135743 | *Prionailurus planiceps* |
| 47 | KR135744 | *Prionailurus rubiginosus* | 
| 48 | KR135742 | *Prionailurus viverrinus* | 
| 49 | KP202261 | *Puma concolor* | 
| 50 | KP202279 | *Puma yagouaroundi* |

Pictures of the species used to generate the sequences above.
<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Cats.png" alt="Cats" width="800"></p>




Opening the [link]( https://www.ncbi.nlm.nih.gov/genbank/) provided earlier you can see the following (slight differences may exist due to different web browsers and operating systems and the position of the planets and …).


<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank1.png" alt="Genbank1" width="800"></p>


In the red rectangle you see a list option which should be on ***Nucleotide***. Clicking on the list you can see other repositories offered by NCBI website. Here we are going to create a dataset of nucleotide sequences of protein coding genes, so we chose the ***Nucleotide*** option. Remember that these markers being protein coding genes, allow us to create also ***Amino Acid*** datasets. *Do you know why we stay with nucleotides in this case? Wich option allows you to create an amino acid dataset?*

Now pick an accession number from the list and hit search. If you like cheetahs (and you choose the first accession number in the list) you should see something similar to this picture:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank2.png" alt="Genbank2" width="800"></p>

Take a look at it. Try to decipher different parts of it. As you see first you read the accession number, the lenght of the sequence and some information about the entry. in the following lines there is more information about the organism, the authors of the sequence, if it is published in any scientific publication, their authors and so on. in this case in the comments you can even see some information on how this genome has been sequenced (Illumina) and how it has been assembled (SOAPdenovo). After this, you can find the information on the annotation of the sequence. Here is where you look to find a gene of interest for example.

Now look at the 2 red rectangles on top of the picture. The one on the left where you can read ***GenBank*** is the format of the information. And the other rectangle "***Send to:***" create a downloadable file. Click on it. Choose ***Complete Record***, ***File*** under *Choose Destination* and finally in *format:* choose ***FASTA***. 

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank3.png" alt="Genbank3" width="800"></p>

Now ***Create File***! And *Voila!* Congratulations! Now you have downloaded your first Fasta file. This fasta file is the sequence information of the whole mitochondrial genome of our nice cheetah sample (in the case you chose the first accession number). What we want to generate here is the alignment for only one gene of the mitochondrial genome, hte ***COI*** gene. Scroll down on the page to find the ***COI*** gene. Remember that some genes could have different names. It should look like this:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank4.png" alt="Genbank4" width="800"></p>

As you can see in the red rectangle, the gene is marked as ***COX1*** and its position on the sequence is given (6060-7604). In the **CDS** section, which stands for **Coding Sequences**, you will see extra information about the gene. Try to decipher different parts of it. *Is there anything you dont understan? Ask! Why the tRNAs before and after does not have a **CDS** section?*

Now we need to download the ***COI*** (or ***COX1***) gene from the mitochondrial whole genome entry. For this clisk on ***gene*** or ***CDS***. It should bring you to the end of the document and highlight the corresponding sequence on the whole genome sequence. You should see this:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank5.png" alt="Genbank5" width="800"></p>

Then you should click on the "**FASTA**" (marked in the red rectangle in the picture above). If you do so you will see the fasta file of the marker we are interested in. You should see the following now:

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank6.png" alt="Genbank6" width="800"></p>

This is the sequence we are interested in. *Do you remember how to download the sequence?* you have a reminder in the next picture...

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/Genbank7.png" alt="Genbank7" width="800"></p>

Now you need to download the ***COI*** sequence for every entry in the list. You could go on and download each of them in a separate file, but I suggest you to have a text file open in any text editor of your choice (no microsoft word though! Try something like TextWrangler for mac or Notepad++ for windows), Copy and paste each fasta into it. Save this file as:


```
COI.fasta
```

---------

Now lets take a look at the *FASTA* files we have created. Open any of them in your (prefered) text editor. (Here I have used TextWrangler!)

<p align="center"><img src="https://github.com/leimurillo/Mol_Phyl_2021/blob/main/Tutorials/1.DatasetManipulation/FastaFile.png" alt="FastaFile" width="800"></p>

As you can see, each entry is something similar to this:

```
>KP202271.1:3460-4415 Acinonyx jubatus isolate AJU mitochondrion, complete genome
ATGTTTATAATTAATATCCTCTCACTAATTATCCCTATTCTCCTCGCCGTGGCTTTCCTAACCCTAGTTG
AACGAAAAGTACTAGGCTACATACAACTTCGTAAAGGACCAAATGTCGTAGGACCATATGGCCTACTCCA
ACCTATTGCAGACGCCGTAAAACTCTTTACCAAAGAACCTCTCCGACCTCTCACATCCTCCATATTCATA
TTTATTATAGCACCAATTCTAGCCCTCACACTAGCACTAACTATGTGAATCCCACTACCCATGCCATATC
CACTCATCAATATGAACCTAGGAGTACTATTCATACTAGCCATATCAAGCCTAGCCGTTTACTCTATCCT
ATGATCAGGATGGGCTTCAAACTCAAAATATGCTCTAATCGGAGCCTTACGAGCCGTAGCCCAAACAATC
TCATATGAAGTCACACTAGCCATCATCCTTTTATCAGTATTACTAATAAATGGGTCCTTCACACTAGCCA
CACTAATTACCACCCAAGAACACACATGGCTAATTATCCCTGCATGACCCCTAGCCATGATATGATTTAT
CTCAACACTAGCAGAAACTAACCGAGCCCCATTCGACCTAACAGAAGGGGAATCAGAATTAGTCTCCGGA
TTTAATGTAGAATACGCAGCAGGCCCCTTCGCCCTATTCTTTCTAGCAGAATACGCCAACATCATCATAA
TAAATATCCTTACAACAATCCTATTTTTCGGAGCATTCCATAATCCTTATATACCAGAACTATATATTGT
CAACTTTACAGTAAAAACCCTGTTTTTAACAACCACTTTCCTATGAATCCGAGCATCATATCCACGATTC
CGATATGATCAATTAATACACCTTTTATGAAAAAATTTTCTCCCTCTTACCCTAGCTTTATGCATATGAC
ACGTATCAATGCCTATTATCACAGCAAGCATCCCACCTCAAACATA
```

The line starting with `>` in a fasta file is a header for the sequence. Practically all programs will have problems with how Genbank have created these fasta files. So in your text editor go and modify the name of each sequence to keep only the organism name. Remember that an empty space is not allowed in the name! Replace it with an underscore `_`. You should have exactly the same header as bellow now.


```
>KP202271_Acinonyx_jubatus
ATGTTTATAATTAATATCCTCTCACTAATTATCCCTATTCTCCTCGCCGTGGCTTTCCTAACCCTAGTTG
AACGAAAAGTACTAGGCTACATACAACTTCGTAAAGGACCAAATGTCGTAGGACCATATGGCCTACTCCA
ACCTATTGCAGACGCCGTAAAACTCTTTACCAAAGAACCTCTCCGACCTCTCACATCCTCCATATTCATA
TTTATTATAGCACCAATTCTAGCCCTCACACTAGCACTAACTATGTGAATCCCACTACCCATGCCATATC
CACTCATCAATATGAACCTAGGAGTACTATTCATACTAGCCATATCAAGCCTAGCCGTTTACTCTATCCT
ATGATCAGGATGGGCTTCAAACTCAAAATATGCTCTAATCGGAGCCTTACGAGCCGTAGCCCAAACAATC
TCATATGAAGTCACACTAGCCATCATCCTTTTATCAGTATTACTAATAAATGGGTCCTTCACACTAGCCA
CACTAATTACCACCCAAGAACACACATGGCTAATTATCCCTGCATGACCCCTAGCCATGATATGATTTAT
CTCAACACTAGCAGAAACTAACCGAGCCCCATTCGACCTAACAGAAGGGGAATCAGAATTAGTCTCCGGA
TTTAATGTAGAATACGCAGCAGGCCCCTTCGCCCTATTCTTTCTAGCAGAATACGCCAACATCATCATAA
TAAATATCCTTACAACAATCCTATTTTTCGGAGCATTCCATAATCCTTATATACCAGAACTATATATTGT
CAACTTTACAGTAAAAACCCTGTTTTTAACAACCACTTTCCTATGAATCCGAGCATCATATCCACGATTC
CGATATGATCAATTAATACACCTTTTATGAAAAAATTTTCTCCCTCTTACCCTAGCTTTATGCATATGAC
ACGTATCAATGCCTATTATCACAGCAAGCATCCCACCTCAAACATA

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

