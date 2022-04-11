# Comparison of Avian Clutch Size, Physical Characterists, and Mating Tactics
# ENV872: EDA Final Project

## Summary

This repository holds the contents related to a Duke Nicholas School of the Environment course titled Environmental Data Analytics. The course was taught during the Spring of 2022, in which this was created. Within it are raw, and processed data files used for analysis of our research questions related to bird data found on an open-source websites. The creators of this repository are in no way connected to the creation of the data set, please see the metadata files for more information and websites relating to its origin.

Our analysis intends to identify trends found between the avian species represented in this data. Within this field of study there is a lot of interest related to avian body size and the impacts this has on other characteristics of a species. Ultimately, we will give insight into two relationships. The first is conducted while controlling for mass to identify how female tail length impacts clutch size. The second, dives into the relationship between mating tactics and tail length. To achieve this, linear regressions and ANOVA were conducted and further explored to simplify models.


## Investigators

* Lydie Costes, lydie.costes@duke.edu
* Jackie Fahrenholz, jacqueline.fahrenholz@duke.edu

## Keywords

<add relevant keywords here>

birds, mating system, clutch-size, avian mass


## Database Information

This data set was found using www.ecologicaldata.org, an open source website for various kinds of biological data. It was originally accessed on March 29th, 2022 and later altered for analysis purposes using RStudio. Variables from the original data sets that were repetitive, or not relevant to comparative analysis were removed. The original data can be found in the Data/Raw folder, while other data sets created by the authors of this repository can be found in Data/Processed. 


## Folder structure, file formats, and naming conventions 

The folders contained within our repository split up our Code and our Data. The Code folder contains the R scripts used to complete analyses to answer our over arching research questions. The Data folder contains the original data set (Raw folder) and our wrangled data sets (Processed folder).


Files within our folders were kept only if relevant to avoid cluttering up our work space. Our `.Rproj` file created the workspace in which we worked through creating our final report. Code files were all written using RStudio and are therefore in `.Rmd` for easy sharing. Our project template is where analysis was conducted, while the project instructions .Rmd provided guidance for the project at large. 

Files are named conventionally, using the original file name for our raw data set that is associated with the `.txt` file in the Data/Raw folder. Processed data is named to distinguish it between the raw dataset and all file names will be explanatory as to the contents held within the file. For this project, `birds.subset` is the file used for analysis. 

## Metadata

Data contained in the Raw folder, consists of a total of 41 variables, and 146 avian families. Information about each of these variables can be found in the .tex file within the Raw data folder.

For our wrangled data, located in the Processed folder, 11 variables were maintained, along with 11 families of avian species. Not all families were kept to simplify visualizations as 146 is overwhelming. Families were chosen by filtering out all incomplete instances of data in explanatory variables. Variables maintained with the processed data include and are defined below:

|Column Name           | Description                | Class   | Units |
|--------------------  | -------------------------- | ------- | ----- |
|  Family              | Family Number              | integer | NA    |
|  F_mass              | Female Mass                | number  | grams |
|  M_mass              | Male Mass                  | number  | grams |
|  F_bill              | Female Bill Length         | number  | mm    |
|  M_bill              | Male Bill Length           | number  | mm    |
|  F_tail              | Female Tail Length         | number  | mm    |
|  M_tail              | Male Tail Length           | number  | mm    |
| Clutch_size          | Average # of eggs          | number  | NA    |
| Common_Mating_System | Score of system            | integer | NA    |
| Common_Display       | Score of display agility   | integer | NA    |
| Common_Resource      | Score of territoriality & inter-mate sharing  | integer | NA    |
                         

### Scores defined

Scoring for each system is created as follow:

_Mating System_

* 1: polyandry
* 2: monogamy
* 3: mostly monogamy, occasional polygyny
* 4: mostly polygyny
* 5: lek or promiscuous

_Common Display_

* 1: ground displays only, including displays on trees and bushes
* 2: ground displays, but with occasional jumps/leaps into the air
* 3: both ground and non-acrobatic flight displays
* 4: mainly aerial displays, non-acrobatic 
* 5: mainly aerial displays, acrobatic

_Common Resource_

* 0: males and females don't share resources and they feed away from their breeding territory
* 1: males and females share resources on their territory only during the breeding season
* 2: males and females share resources on their territory all year round

## Scripts and code

Within this repository, you will find a `Project_Template.Rmd` which includes all the code used to wrangle, visualize, and evaluate our research questions. This `.Rmd` file can be found within the Code folder. 

## Quality assurance/quality control

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>
