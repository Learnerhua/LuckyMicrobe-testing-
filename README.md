# LuckyMicrobe
## Introduction
A pipeline to analyse 16S rDNA sequencing amplicon data.<br>
Three softwares were used in this pipeline (Qiime2, Usearch and LEfSe) to investigate your pair-end 16S rDNA sequencing data,you can process taxonomy composition analysis , microbialcommunity diversity analysis and differential abundance analysis through it.<br>
Reading the following guide carefully and start the journey of data analysis !<br>
## Guide for use
### A flow diagram for this pipeline
![](https://github.com/Learnerhua/LuckyMicrobe/blob/master/Help/workflow.png)       
***Note:*** As is shown above, there are totally four algorithms to get the feature table and representative sequences in the Qiime2 and Usearch, we provide three batches of them here except the vsearch methods in the dotted box.
### Environment configuration
 We make and test the pipeline in operation system: CentOS Linux release 7.6.1810.<br>
You must install these three softwares mentioned above, of course, you needn't install the LEfSe if you don't want to process a differential abundance analysis.<br>
The specific installation methods are recorded in the file "Installation.txt".
### Get started
You can enter the "example" directory and run the "run.batch" file by entering the command "sh run.batch" to test if this pipeline is compatible with your environment,
if not any mistake shows, congratulations, you successfully build an appropriate environment to run this pipeline!<br>
After testing the environment, what you just need to do is to prepare the data and metadata files and changing the parameters in "Configuration.txt" file for your analysis according to the example, such as preparing pair-end sequences data which contain a suffix "_1.fq.gz" and its counterpartner file with a suffix "_2.fq.gz". Another point you must take care of is the value in absolute-filepath colum of the metadata file must be under the directory "prefix_merged" with a suffix ".MG.fq" just like the metadata file in "example" directory.<br>
***Note:*** **To save your time, the diversity analysis and differential abundance analysis won't run automatically. The methods to run them:**<br>
* For differential abundance analysis, you just need to delete the "#" before "diffAbunAnalysis" at the end of the file "run.batch".
* For diversity analysis, firstly you should ensure the level you rarefy by viewing the visualized results on the "Qiime 2 View" website, then change the parameters in "Configuration.txt", finally delete the "#" before "diversityAnalysis" and add "#" before other two functions at the end of the file "run.batch".









