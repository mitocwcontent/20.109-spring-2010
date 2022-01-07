---
content_type: page
parent_title: Assignments
parent_uid: 5a2e497f-e49c-5201-6e67-a52f578758e7
title: 'Module 1 Assignment: RNA Computational Analysis'
uid: 719527d1-5fa3-3e74-09a6-6598e496c6a1
---

Contents
--------

*   [Assignment Overview](#Assignment_Overview)
*   [Logistics](#Logistics)
*   [Background Information](#Background_Information)
*   [Part I: CLUSTAL Analysis](#Part_I:)
*   [Part II: MEME Analysis](#Part_II:_)
*   [Part III: Mfold Analysis](#Part_III:_)

{{< anchor "Assignment_Overview" >}}{{< /anchor >}}Assignment Overview
----------------------------------------------------------------------

### Goals

Gain familiarity with a few common _in silico_ methods available for:

1.  Organizing RNA primary sequences into related families (CLUSTAL).
2.  Identifying conserved sequence motifs present in RNA (MEME).
3.  Predicting the secondary structures of single stranded RNA (Mfold).

It is worth noting here that while we will focus our analyses on RNA, CLUSTAL and MEME can also be successfully used for DNA and protein analysis. Mfold is additionally useful for single stranded DNA secondary structure predictions.

### Learning Outcomes

By the end of this exercise, you should be able to:

1.  Compile your data into a format readable by the web-based software being used for these analyses.
2.  Interpret the outputs from these algorithms.
3.  Formulate hypotheses based on your data interpretation for further testing using _in silico_ and/or wet-lab experimental methods.
4.  Appreciate some limitations associated with these methods.

{{< anchor "Logistics" >}}{{< /anchor >}}Logistics
--------------------------------------------------

The computational analysis assignment is due by 11 am on Day 1 of Module 2.

Formatting expectations:

*   Your main document (excluding figures) should be/have
    *   .doc (preferred) or .pdf
    *   12-pt font
    *   with 1-inch margins
    *   double-spaced
*   Figures can be included in the .doc, or made in a separate drawing program (such as powerpoint) and submitted as .pdf

{{< anchor "Background_Information" >}}{{< /anchor >}}Background Information
----------------------------------------------------------------------------

Imagine that you have just completed your final round of SELEX, and now have sequence data obtained after the cloning step. Each sequence is derived from a single bacterial colony harboring a single plasmid, which encodes one aptamer sequence. In this exercise, you will be performing analyses of both the primary and predicted secondary structures of these (putative) aptamers. Overall, you will be trying to gain insights into the sequence and/or secondary structure patterns that help you:

1.  Organize the aptamers from your SELEX experiment into sequence related classes; and
2.  Formulate testable hypotheses aimed at connecting sequence and predicted structural analyses to function (heme binding in this case).

A broader context for appreciating the importance of the analyses you are undertaking relates to the fact that the initial SELEX library is extremely diverse (≥ 1013 unique sequences), with many of the sequences recovered at the end of your selection process being present initially only in single copy! So, what is so special about the set of sequences surviving the selection process? Do they share specific sequence motif(s) favoring high affinity binding to the target? Or, do they share structural features (dependent on or independent of) primary sequence composition that favor their interactions with the target? Alternatively, you could imagine that in the vast nucleotide sequence space you are exploring, there are many independent ways for a given sequence to interact with a target. In this case, you could recover sets of aptamers bearing no sequence or structural similarity to each other, but are all still capable of interacting with the target. The analyses you are about to perform can provide some insight into these fundamental questions, but as you will discover there are some important limitations.

For the purposes of 20.109, we do not expect you to know the details of how these algorithms work.

{{< anchor "Part_I:" >}}{{< /anchor >}}Part I: CLUSTAL Analysis
---------------------------------------------------------------

CLUSTAL is a program that finds strings of homology among primary sequences of nucleic acids. You can learn more by following the link to the new user FAQ on the CLUSTAL homepage.

### Exercise

1.  Go to the [CLUSTAL Web site](http://www.ebi.ac.uk/Tools/clustalw2/index.html).
2.  Copy and paste the sequences from the attached data file into the text box labeled: "Enter or paste a set of sequences in any supported format:"
    *   Note: Be sure that all the ">" characters are included. This is FASTA formatted data, which is a common way for inputting data into many of the bioinformatics software packages used today. You can read more about this data format at the CLUSTAL Web site.
3.  Using the default settings, click the RUN button to begin your analysis.
4.  You will see an alignment of the sequences you entered. Orient yourself to appreciate how your sequences are grouped relative to each other.
    *   To better appreciate the groupings, select the "View Guide Tree" button and then select the "Show as Phylogram Tree" option. You will need to scroll to the bottom of the page to see the results of this operation. You can always go back to your sequence alignment using the "Back to Main Result" button.

### Questions

1.  Why analyze only the sequence derived from the variable portion of your library?
2.  Can you detect distinct groups based on this primary sequence analysis? Very briefly, how are members within a group related to each other?
3.  Do you find any repeated sequences? Give at least two reasons why these might be present. Provide your rationale for what you believe to be the most likely reason for this finding.
4.  Identify two very closely related, but non-identical sequences. Briefly describe the observed difference, and describe two ways in which these related aptamers could have originated.
5.  Provide a brief summary of what overall your CLUSTAL analysis has helped you accomplish.

### Associated Figure

Capture a screenshot of the phylogram tree and give it an informative title.

{{< anchor "Part_II:_" >}}{{< /anchor >}}Part II: MEME Analysis
---------------------------------------------------------------

MEME is a program that identifies "statistically significant" contiguous sequences that are common to a group of DNA or protein sequences. You can learn at the [MEME Overview](http://meme.sdsc.edu/meme/intro.html) page and associated links.

### Exercise

In this part of your assignment, you will be analyzing your sequence data to determine if there are any motifs that are enriched in your selected library pool. Using the sequence data derived from the variable region of your putative aptamers, perform a MEME analysis.

1.  Create a .txt file containing the variable region sequences derived from only your unique clones in FASTA format. Alternatively, you can paste these in as before.
2.  Go to the [MEME Web site](http://meme.sdsc.edu/meme/intro.html). Choose the MEME option, and follow the directions for entering your sequences. You will need to enter a valid email address to receive a link to your data for easy future access.
3.  Use the following settings for your analysis:
    *   Motif Frequency (how many occurrences of the motif you expect per sequence) = Zero or one
    *   Motif width (the number of contiguous bases you expect your recovered motif will contain): Minimum = 8 and Maximum = 15
    *   Number of motifs to discover: Use default value = 3

### Questions

1.  How do you decide which of the three observed motifs is most statistically significant and worth your further consideration? Explain briefly the meaning of the parameter(s) that helped you make your determination.
2.  Why limit your analysis only to unique sequences here, whereas during you CLUSTAL analysis you considered all your sequence data?
    *   Hint: Perform a MEME analysis with 2 sequences (A = 6-3 & B = 8-1, for example). In one analysis, let your dataset include 6 repeats of A and 1 of B. In the next analysis, reverse the representation. Compare the motif characteristics you recover in both situations with that you recover when A and B are stoichiometrically represented in your dataset.
    *   Give two potential functional roles for your highest confidence MEME-detected motif during heme binding to your aptamers.

### Associated Figure

When viewing the MEME output (HTML option), look to the left of each motif image to download it (e.g., as a .png file). Organize the 3 motifs found in your original analysis (not in question 2) into a figure. Give the figure an informative title and a brief caption, which should include the parameter values you used to make a determination of significance.

{{< anchor "Part_III:_" >}}{{< /anchor >}}Part III: Mfold Analysis
------------------------------------------------------------------

Mfold is a program that predicts nucleic acid secondary structures by computing free energies for the potential structure-space of a given sequence. You can learn more on the [Mfold homepage](http://mfold.rna.albany.edu/?q=mfold/download-mfold) and in the cited literature at the bottom of that page.

### Exercise

Here, you will predict the secondary structures for 6-5 and 8-12 using the full-length (constant + variable region) RNA sequence expected after transcription.

1.  Follow the directions provided in your data file (read all the background and notes carefully) to come up with the required RNA sequences.
2.  Go to the [Mfold Web site](http://mfold.rna.albany.edu/?q=mfold/download-mfold).
3.  Obtain folded structures for the 6-5 and 8-12 RNA sequences. Since you have a small number of sequences enter each individually, and perform your analyses sequentially.
    *   Use the default options, but please enter the following information:
        *   A name for your sequence
        *   A valid email address
    *   Before submitting the 8-12 sequence, highlight the location of the highest confidence conserved element detected during your MEME analysis in Part II.
        *   This is achieved by going to the "Choose structure annotation" line, selecting the "high-light" option and entering the region you'd like to highlight. Enter this sequence range as xi-xn, where xi and xn are the first and last residue positions of the region you'd like to highlight. Residue 1 is the first G in your RNA sequence. For example, entering 20-50 will highlight residues 20-50. Multiple regions can be highlighted if you separate them by a comma (if needed).

### Questions

1.  In both the CLUSTAL and MEME analyses, you analyzed only the sequence derived from the variable region of your library. Here, you have included the constant regions in your analysis. Why is this is important? \[Hint: Try your analysis using only the variable region, and compare the results with those obtained just prior\].
2.  Which folded structure is predicted to be more stable: 6-5 or 8-12? Explain your reasoning. Note that the same reasoning should help you decide which of the predicted 6-5 structures might be considered thermodynamically more favorable.
3.  Can you identify distinguishable secondary structure feature(s) between 6-5 and 8-12 that might explain their different heme-binding properties?
4.  Design an approach combining the _in silico_ prediction methods being used in this exercise with laboratory experiment(s) that will permit testing whether your identified feature is relevant to heme binding.
5.  A short sequence (27 bases) derived from 8-12 residues (33-59) containing the region corresponding to the conserved motif was chemically synthesized. It is capable of binding heme. Would you have predicted this based upon secondary structure predictions (take a look at the secondary structure of this fragment, too)? How do you rationalize these observations?

### Associated Figure

Include images of all 5 structures you found in the exercise above and give them informative titles. You do not need to write figure captions. For the two full-length aptamers, you might highlight features that you discuss in question 3 on the images. Otherwise, just refer to them by base number.