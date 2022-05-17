# LuckyMicrobe
## Introduction
A pipeline to analyse 16S rDNA sequencing amplicon data.<br>
Three softwares were used in this pipeline (Qiime2, Usearch and LEfSe) to investigate your pair-end 16S rDNA sequencing data,you can process taxonomy composition analysis , microbialcommunity diversity analysis and differential abundance analysis through it.<br>
Before using this pipeline, we assume that you are very familiar with the principles of these softwares and clearly know what you really want to get.
Reading the following guide carefully and start the journey of data analysis !<br>
## Guide for use
### A flow diagram for this pipeline
![](https://github.com/Learnerhua/LuckyMicrobe/blob/master/Help/workflow.png)       
***Note:*** As is shown above, there are totally four algorithms to get the feature table and representative sequences in the Qiime2 and Usearch, we provide three batches of them here except the vsearch methods in the dotted box.
### Environment configuration
 We make and test the pipeline in operation system: CentOS Linux release 7.6.1810.<br>
You must install these three softwares mentioned above, of course, you needn't install the LEfSe if you don't want to process a differential abundance analysis.<br>
The specific installation methods are recorded in the file "Installation.txt".
### Getting started
You can enter the "example" directory and run the "run.batch" file by entering the command "sh run.batch" to test if this pipeline is compatible with your environment,
if not any mistake shows, congratulations, you successfully build an appropriate environment to run this pipeline!<br>
After testing the environment, what you just need to do is to prepare the data and metadata files and change the parameters in "Configuration.txt" file for your analysis according to the example, such as preparing pair-end sequences data which contain a suffix "_1.fq.gz" and its counterpartner file with a suffix "_2.fq.gz". Another point you must take care of is the value in absolute-filepath colum of the metadata file must be under the directory "prefix_merged" with a suffix ".MG.fq" just like the metadata file in "example" directory.<br>
***Note:*** **To save your time, the diversity analysis and differential abundance analysis won't run automatically. The methods to run them:**<br>
* For differential abundance analysis, you just need to delete the "#" before "diffAbunAnalysis" at the end of the file "run.batch" and make some small changes in the "lefse.batch".
* For diversity analysis, firstly you should ensure the level you rarefy by viewing the visualized results on the "Qiime 2 View" website, then change the parameters in "Configuration.txt", finally delete the "#" before "diversityAnalysis" and add "#" before other two functions at the end of the file "run.batch".

**The parameters in "configuration.txt" are very important that you need to understand them thoroughly and change them according your own need.**
## Citation
* Bolyen E, Rideout JR, Dillon MR, Bokulich NA, Abnet CC, Al-Ghalith GA, Alexander H, Alm EJ, Arumugam M, Asnicar F, Bai Y, Bisanz JE, Bittinger K, Brejnrod A, Brislawn CJ, Brown CT, Callahan BJ, Caraballo-Rodríguez AM, Chase J, Cope EK, Da Silva R, Diener C, Dorrestein PC, Douglas GM, Durall DM, Duvallet C, Edwardson CF, Ernst M, Estaki M, Fouquier J, Gauglitz JM, Gibbons SM, Gibson DL, Gonzalez A, Gorlick K, Guo J, Hillmann B, Holmes S, Holste H, Huttenhower C, Huttley GA, Janssen S, Jarmusch AK, Jiang L, Kaehler BD, Kang KB, Keefe CR, Keim P, Kelley ST, Knights D, Koester I, Kosciolek T, Kreps J, Langille MGI, Lee J, Ley R, Liu YX, Loftfield E, Lozupone C, Maher M, Marotz C, Martin BD, McDonald D, McIver LJ, Melnik AV, Metcalf JL, Morgan SC, Morton JT, Naimey AT, Navas-Molina JA, Nothias LF, Orchanian SB, Pearson T, Peoples SL, Petras D, Preuss ML, Pruesse E, Rasmussen LB, Rivers A, Robeson MS, Rosenthal P, Segata N, Shaffer M, Shiffer A, Sinha R, Song SJ, Spear JR, Swafford AD, Thompson LR, Torres PJ, Trinh P, Tripathi A, Turnbaugh PJ, Ul-Hasan S, van der Hooft JJJ, Vargas F, Vázquez-Baeza Y, Vogtmann E, von Hippel M, Walters W, Wan Y, Wang M, Warren J, Weber KC, Williamson CHD, Willis AD, Xu ZZ, Zaneveld JR, Zhang Y, Zhu Q, Knight R, and Caporaso JG. 2019. Reproducible, interactive, scalable and extensible microbiome data science using QIIME 2. Nature Biotechnology 37: 852–857. https://doi.org/10.1038/s41587-019-0209-9
* R.C. Edgar (2010), Search and clustering orders of magnitude faster than BLAST, Bioinformatics 26(19) 2460-2461
* Nicola Segata, Jacques Izard, Levi Walron, Dirk Gevers, Larisa Miropolsky, Wendy Garrett, Curtis Huttenhower."Metagenomic Biomarker Discovery and Explanation" Genome Biology, 2011 Jun 24;12(6):R60
## Cantact us
If you encounter any question during the use of this pipeline, please contact us by email oyjh417701@163.com

**May 17 CST 2022**<br>
**Copyright (c) 2022 OYJH**<br>
**All Rights Reserved.**










