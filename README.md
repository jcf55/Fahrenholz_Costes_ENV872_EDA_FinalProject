# Comparison of Avian Clutch Size, Physical Characteristics, and Mating Tactics
# ENV872: EDA Final Project

## Summary

This repository holds the contents related to a Duke Nicholas School of the Environment course titled Environmental Data Analytics, taught during the Spring of 2022. The data used for our analysis consist of publicly available bird size and behavioral characteristics consolidated from various sources by Lislevand et al (2007). The data folder includes both raw and processed versions of the dataset as well as metadata. The creators of this repository are in no way connected to the creation of the dataset, so please see the metadata files for more information.

Our analysis intends to identify trends found between the avian species represented in this data. Within this field of study there is a lot of interest related to avian body size and the impacts this has on other characteristics of a species. Ultimately, we will give insight into two relationships. The first is conducted while controlling for mass to identify how female tail length impacts clutch size. The second, dives into the relationship between mating tactics and male tail length. To achieve this, linear regressions and ANOVA were conducted and further explored to simplify models.

## Investigators

* Lydie Costes, lydie.costes@duke.edu
* Jackie Fahrenholz, jacqueline.fahrenholz@duke.edu

## Keywords

birds, mating system, clutch size, avian mass, display behavior, morphology, life history, data analytics

## Database Information

This data set was found using www.ecologicaldata.org, an open source website for various kinds of biological data. It was originally accessed on March 29th, 2022 and later altered for analysis purposes using RStudio. Variables from the original data sets that were repetitive or not relevant for our comparative analysis were removed. The original data can be found in the Data/Raw folder, while other data sets created by the authors of this repository can be found in Data/Processed. 

## Folder structure, file formats, and naming conventions 

The folders contained within our repository split up our Code and our Data. The Code folder contains the R scripts used to complete analyses to answer our over arching research questions. The Data folder contains the original dataset (Raw folder) and our wrangled datasets (Processed folder).

Files within our folders were kept only if relevant to avoid cluttering up our work space. Our `.Rproj` file created the workspace in which we worked through creating our final report. Code files were all written using RStudio and are therefore in `.Rmd` for easy sharing. Our project template is where analysis was conducted, while the project instructions .Rmd provided guidance for the project at large. 

Files are named conventionally, using the original file name for our raw data set that is associated with the `.txt` file in the Data/Raw folder. Processed data is named to distinguish it between the raw dataset and all file names will be explanatory as to the contents held within the file. For this project, `birds.subset` is the data frame used for analysis, which is saved as `birds_subset.csv` in the Data/Processed folder. 

## Metadata

Data contained in the Raw folder consists of a total of 41 variables and 3769 species from 125 avian families. Information about each of these variables can be found in the .tex file within the Raw data folder.

For our wrangled data, located in the Processed folder, 11 variables were maintained including a newly created Genus category. Variables maintained with the processed data include and are defined below:

|Column Name           | Description                | Class   | Units |
|--------------------  | -------------------------- | ------- | ----- |
|  Family              | Family number              | factor | NA    |
|  Species_name	| Scientific name of species | character | NA	|
|  Genus		| Genus				| character	| NA	|
|  F_mass              | Female mass                | number  | grams |
|  M_mass              | Male mass                  | number  | grams |
|  F_tail              | Female tail length         | number  | mm    |
|  M_tail              | Male tail length           | number  | mm    |
| Clutch_size          | Average # of eggs          | number  | NA    |
| Mating_System | Score of system            | integer | NA    |
| Display       | Score of display agility   | integer | NA    |
| Resource      | Score of territoriality & inter-mate sharing  | integer | NA    |
                         
### Scores defined

Scoring for each system is created as follow:

_Mating System_

* 1: polyandry
* 2: monogamy
* 3: mostly monogamy, occasional polygyny
* 4: mostly polygyny
* 5: lek or promiscuous

_Display_

* 1: ground displays only, including displays on trees and bushes
* 2: ground displays, but with occasional jumps/leaps into the air
* 3: both ground and non-acrobatic flight displays
* 4: mainly aerial displays, non-acrobatic 
* 5: mainly aerial displays, acrobatic

_Resource_

* 0: males and females don't share resources and they feed away from their breeding territory
* 1: males and females share resources on their territory only during the breeding season
* 2: males and females share resources on their territory all year round

## Scripts and code

Within this repository, you will find a `Project_Code.Rmd` which includes all the code used to wrangle, visualize, and evaluate our research questions. This `.Rmd` file can be found within the Code folder. 

## Quality assurance/quality control

Original data for this project was simplified and wrangled to support research questions. Outliers were not removed from the data, but only during visualizations in order to gain a clearer picture in areas where was high in quantity. Because this data was collected currently from 2005-2007 and it not a total dataset of all bird species, it should be noted that conclusions made in this report, and others generated are insights and should be further explored with other datasets that may be more robust.

