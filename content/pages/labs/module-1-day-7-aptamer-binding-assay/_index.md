---
content_type: page
parent_title: Labs
parent_uid: c810141c-0282-3f29-da2a-83f1fe93dcb1
title: 'Module 1, Day 7: Aptamer Binding Assay'
uid: 6074c179-64ef-9a51-f5e9-785309daca35
---

< [Previous lab day]({{< baseurl >}}/pages/labs/module-1-day-6-post-selection-ivt-and-journal-club) | [Module 1 lab index]({{< baseurl >}}/pages/labs#MODUle_1:_RNA_Engineering) | [Next lab day]({{< baseurl >}}/pages/labs/module-1-day-8-journal-club-continued) >

Introduction
------------

Between the first round of journal club talks, and the paper that we all discussed on day three of this module, you have begun to learn a lot about the usefulness of RNA aptamers and the SELEX process.

One particularly compelling type of aptamer is that which not only binds to a target, but in doing so reproducibly effects a particular function. Riboswitches consisting of an aptamer domain and an expression platform are common in nature, particularly in bacteria. The aptamer domain often recognizes a small molecule metabolite. Due to a resulting conformational change in the expression platform, transcription of a gene (or translation of its associated protein) may subsequently be turned on or off. For example, target binding may alter premature transcript termination via terminator/anti-terminator pairing. Engineers can mimic nature's designs to create riboswitches with arbitrary desired functions. Ribozymes, or RNA with cleaving activity, may be incorporated in engineered riboswitches for additional functions.

The specificity and affinity exhibited by aptamers is well-suited to several therapeutic uses. You have now seen examples of aptamers acting as drugs, drug antidotes, and potentially as targeted drug carriers that hone in on disease sites. You can start to appreciate the trade-offs inherent in experimental design for human health applications. For example, is the greater cost and labor of _in vivo_ experiments offset by increased likelihood that the aptamer actually works in the required environment?

While RNA aptamers theoretically present infinite engineering possibilities, in reality researchers are limited by time and resources. Thus, improvements to SELEX efficiency are also an important research topic. Use of microfluidics and magnetic beads, and dual selections, are two examples of modified SELEX you saw in the journal club papers. Some modifications to SELEX are particular to specific applications, such as preparing aptamers to complex targets (e.g., tumors).

In this module, we have investigated SELEX efficiency at the column selection step, using known RNA sequences (one that binds to heme and one that doesn't) as a model system. We varied stringency in two ways: number of washes, and amount of target aptamer present. After today's experiment, you should be able to discover some trends in SELEX efficiency. Consider how applicable your results are to an arbitrary SELEX system, and what further experiments or you might suggest doing in the future.

Protocols
---------

### Part 1: Purify, Quantify, and Prepare RNA

Repeat the [Day 4]({{< baseurl >}}/pages/labs/module-1-day-4-purify-rna-and-run-affinity-column) protocol, parts 1 through 3. That is, briefly:

1.  Digest the RNA, then purify on a Micro Bio-Spin column.
2.  Quantify the RNA by spectrophotometry.
    *   If you have less than 1.4 nmol of either "post" sample, let one of the teaching faculty know.
3.  Dilute each sample to 8 μM in the selection buffer (SB).
    *   Note that to dilute your post-column sample, you will have to make an educated assumption about the ratio of 6-5 to 8-12, because they do not have the same molecular weight. What do you expect to have happened on the column?
4.  Finally, denature not only your "post" samples, but also your four "pre" samples, at 70 °C and then let them cool for at least 10 minutes.
    *   If you are missing some "pre" samples due to low RNA yields, let the teaching faculty know; we have extra 6-5 and 8-12 to give you.

### Part 2: Binding Assay

1.  Retrieve some 6 μM heme from the teaching faculty. _Why might you use 6 μM instead of 8 μM, if we want 1:1 molar RNA:heme?_
    *   A 1M stock solution of heme was originally prepared in DMSO, then diluted in multiple steps to 6 μM. Note that the stock solution is prepared by dabbing a little (solid) hemin into DMSO, and then testing the concentration on a spectrophotometer. The extinction coefficient of heme at 405 nm is 180 mM\-1cm\-1.
2.  For each sample in the table below, add 175 µL of heme solution to an eppendorf tube.
3.  Now add 175 µL of selection buffer to the first tube. To the remaining tubes, add 175 µL of the appropriate aptamer solution.
4.  Incubate for a minimum of five minutes at room temperature.
5.  Meanwhile, unwrap some microcuvettes, one for each sample. Add 350 µL of selection buffer to the first cuvette.
    *   Remember that SB has soap in it. If you form bubbles as you are pipetting, these may interfere with the absorbance measurement. Thus, as you pipet each sample into its cuvette, do not expel the final drop of SB.
    *   If a bubble forms anyway, ask the teaching faculty to help you pop it with a needle.
6.  Blank on selection buffer alone. Then, beginning with the heme sample, read the spectrum from 350 to 425 nm (in 0.1 nm steps). **It is essential that after each reading you send that data to the attached USB key**. To do this hit _Options_ on the touchscreen, select _More_ from the menu, and then press _Send Data_. Make sure a "sending data..." message pops up. Hit _Return_ once to return to the absorbance screen. You should also note down the absorbance value at 405 nm, and observe whether the peak appears to have shifted away from 396 to 405 nm.

| SAMPLE | ABS AT 405 nm | PEAK SEEMS SHIFTED? |
| --- | --- | --- |
| Blank | N/A | N/A |
| Heme alone | &nbsp; | N/A |
| 6-5 "pre" | &nbsp; |
| 8-12 "pre" | &nbsp; |
| Mixture "pre" | &nbsp; |
| Mixture "post," fewer washes | &nbsp; |
| Mixture "post," more washes | &nbsp; |   

### Part 3: Begin Analysis

You may want to start your analysis in lab, or wait until later. The directions below provided an outline of the steps you need to take.

1.  Retrieve your group's binding data files, posted by the instructors as .csv spreadsheets.
    *   Each group gets a set of six .csv files containing the data. Representative samples for five groups are contained in this ZIP file ([ZIP]({{< baseurl >}}/resources/m1d7_student_data)).
2.  Within Excel's _File_ → _Open_ menu, enable opening of All _Documents_ in the dialog box that appears, and select your first txt file. Click _Open_, then _Next_, and finally select the _Comma_ delimiter (you don't need to also unselect _Tab_) before clicking _Finish_.
3.  Open a blank Excel file into which you can paste all your data, and save it with an informative name. Copy and paste the wavelength values into the first column of the new Excel file.
    *   The column is very long! To copy-paste efficiently, delete the top few rows of the text file, then click on the whole column (rather than selecting the appropriate cells) before using the copy command.
4.  Copy the first sample's absorbance data into the second column of the Excel file.
5.  Open the next text file, and proceed as above. Note that you do not need to copy the wavelength values again, because they are the same for each sample.
6.  Quickly plot absorbance vs. wavelength for each sample, all on the same chart. Re-scale as necessary to get a good look.
7.  Do the sample curves all overlap pretty well at 380-385 nm? If so, move to step X. Otherwise, proceed with the next step.
8.  Choose one sample - for example, the 6-5 or 8-12 "pre" sample - as a standard. Find the average difference between each sample and your standard sample in the 380-385 nm range.
    *   For example, set up a new column - perhaps on a new sheet - that takes the difference of each subsequent column from the standard.
    *   For example, set up a new column - perhaps on a new sheet - that takes the difference of each subsequent column from the standard.
    *   The two "pre" aptamers should have a difference quite near zero, perhaps 0.0004. Other samples may have differences closer to 0.01 or even 0.1.
9.  For each sample, subtract the average difference in the (supposed-to-) overlap region from the entire absorbance spectrum.
10.  Plot the subtracted samples and confirm that they now overlap where expected.
11.  Insert a few rows at the top of your sheet. In one row, select the A405 value for each sample. In the next row, write the % 8-12 for each "pre" sample.
12.  For the "pre" and "post" mixtures, linearly interpolate between the 6-5 and 8-12 A405 values to estimate the % 8-12.
    *   How well does the "pre" value match what you thought you put in? How might you account for any observed difference?
    *   How does your "post" value compare with what you expected, given the % 8-12 you started with, and relatively speaking for your and your partner's wash number?
    *   Do the horizontal peak shifts seem consistent with your findings based on the vertical shifts?
13.  {{< anchor "result_link" >}}{{< /anchor >}}Post a summary of your findings ASAP, but by 48 hrs after Day 8. That way the entire class can look for trends while writing their respective lab reports.
    *   [Sample findings]({{< baseurl >}}/pages/labs/module-1-day-7-aptamer-binding-assay/module-1-day-7-results) from the five lab groups for which data was supplied above.

For Next Time
-------------

1.  Some of you will be presenting during journal club next time. No other homework is due on day 8.
    *   An awareness of your own strengths and weaknesses can often help you improve your future work. After you give your presentation next time, write a brief self-evaluation. Specifically, describe (in a short phrase or sentence each) two things that you thought you did well, and two that could use improvement. Feel free to include both big-picture and detail-oriented comments. This assignment is due by email within **48 hours** after your presentation.
2.  Your first draft of the [laboratory report]({{< baseurl >}}/pages/assignments/module-1-assignment-rna-engineering-laboratory-report) is due by 11 a.m. on Day 1 of Module 2.
3.  Your [computational analysis assignment]({{< baseurl >}}/pages/assignments/module-1-assignment-rna-computational-analysis) is due by 11 a.m. on Day 1 of Module 2.
4.  Your first self-assessment is due in lab on Day 1 of Module 2, as a hard-copy.
    *   Rubric for Participation, Self-Assessment ([PDF]({{< baseurl >}}/resources/mit20_109s10_syll_self))

Reagent List
------------

*   DNase stock concentration is 2000 U/mL (from New England Biolabs)
*   Micro Bio-Spin Columns
    *   Resin: Bio-Gel P30 in Tris buffer
    *   40,000 MW cut-off
    *   RNase free
    *   From Bio-Rad
*   Selection Buffer
    *   100 mM Tris-acetate
    *   500 mM Na-acetate
    *   25 mM K-acetate
    *   10 mM Mg-acetate
    *   5% DMSO
    *   0.05 % Triton-X
*   Poly-Prep Chromatography Columns from Bio-Rad
*   Hemin-agarose beads
    *   Available as 2x slurry (1 part resin: 1 part solution)
    *   4 μmoles hemin per mL resin
    *   From Sigma-Aldrich
*   Pure hemin
    *   Solid chemical stock from Sigma-Aldrich
    *   Concentrated stock solution (~ 10-15 mM) prepared in DMSO
    *   Diluted to 2.5 mM in Sample Buffer
*   RNA Precipitation (stock solutions)
    *   5 M ammonium acetate
    *   20 mg/mL glycogen