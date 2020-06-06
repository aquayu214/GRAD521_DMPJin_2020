# Data Management Plan

## Introduction
In addition to lower speeds, speed variation on the roadway is a contributing factor to roadway crashes. In Phase 1 of the present study, it reveals that speed variation on roadway sections with a work zone present is higher than that without a work zone. The safety in work zones affects both motorists driving through the work zone and construction workers. The goal of Phase 2 is to identify potential traffic control measures and examine their effectiveness in reducing speed variation in work zones.

## Data Description

### Dataset Types and Methods of Collection
Both qualitative and quantitative data about the implemented traffic control measures and traffic data will be collected based on observations. Two primary datasets are needed, they are: 1) data collected by traffic sensors and GPS loggers, including their ID and placement information (GPS coordinates and work zone locations), as well as information about passing vehicles (time stamps, travel speeds and vehicle lengths); and 2) digital files (text, photo, and video files) document work zone layout and conditions, and observed driver behavior changes in response to the presence of traffic control measures throughout the study. The data collected by traffic sensors and GPS loggers will be documented in Excel and saved as .csv files. With respect to digital files, handwritten notes taken during the data collection will be documented in Word as .docx files, photographs will be saved as .jpg files, and videos will be saved as .mov files.

Several portable traffic sensors will be used to collect traffic data. Handheld GPS devices and GPS trackers will be used to record the GPS coordinates of the placed traffic sensors and the implemented traffic control measures. An iPhone camera and a video camera will take photos and videos about the examined work zones and passing vehicles.  

### Data Analysis
Quantitative data manipulation and analysis will be completed using R software. Descriptive analysis will be conducted to examine the overall pattern of speed variation, and statistical analysis, e.g., Wilcoxon signed-rank test, will be performed to confirm whether the difference between treatments is statistically significant in speed variation reduction in work zones. 

### Data Size
It is anticipated to collect field case study data on three work zones, three days per work zones. The expected volume of data collected will be between 20 to 30 GB.

## Roles and Responsibilities
The research assistant will draft the data management plan for the PI to review and revise. The PI will be responsible to ensure the data management plan is followed throughout the course. Prior to data collection, the research assistant has to ensure all the equipment (traffic sensors, GPS loggers, video cameras, etc) are fully-charged, and calibration tests of traffic sensors are performed. The funding agency will not collect or provide any raw data. To the best knowledge of the research team, there is no formal documents describing data manamgenet requirements from the funding agency that will affect the present data management strategy. Data collection will be conducted by the PI and the research assistant, with occasional assistance from the PI’s research group team. 

It will be the research assistant’s responsibility to be the data manager after data are collected. The research assistant will be responsible for downloading and storing any data they collected at the same locations (a local computer at the School of Civil and Construction Engineering at Oregon State University, and a shared folder that is hosted by the department), and making sure to format and name the files appropriately. No sensitive or confidential data will be collected for this project. 

Data analysis will be primarily performed by the research assistant, with assistant/supervision from the PI and the Technical Advisory Committee (TAC). The research assistant will be responsible to document the analysis process and associated files. After the project is completed, the PI will be the primary researcher responsible for data archiving and preservation. If the research assistant has to leave the project, all the data generated will be transferred to the PI. The PI will be the main person to ensure data are organized, managed and backup properly.

## Data Standards and Metadata
There are no metadata standards that could be applicable for this research project in the civil engineering field. However, a file structure is pre-defined and will be followed to maintain data generated throughout the study. Files will be stored in separate folders based on different case study projects, subfolders will store raw data, processed data, and data analysis procedures associated with each project, and other appropriate subsections to store data that are collected with different equipment (e.g., GPS loggers, traffic sensors and cameras). To be specific, three main types of data will be included in this project, including two raw datasets and one processed dataset. The following content provides a description of what metadata will be generated and the version control measures that will be taken for the three datasets.

Dataset 1 (raw data): data collected with GPS loggers and traffic sensors. The excel datasets will be named following casestudyNo_equipmentID_YYYYMMDD.csv where casestudyname is a abbreviation of the case study project name, equipmentID is an identifier of the equipment used to collect the data, and YYYYMMDD is the date that data are collected. A text file will be stored describing who and when the data are collected, contact information, and general information of the variables including units, description, abbreviations, and list of possible values when necessary. Since this dataset contains primarily raw data generated at the data collection stage, it is not expected they will change over the time, no version control will be applied to this dataset.

Dataset 2 (raw data): digital files. For the digital files, .txt files delineating details about data logger/photographer, work zone conditions, and traffic control treatments will be uploaded in the associated folders. Similar to dataset 1, no version control will be used for this raw dataset.

Dataset 3 (processed data): data analysis files with R. The file names of the R scripts generated will follow casestudyNo_codepurpose.R. Version control will be applied to this dataset using Git, and will also be done manually by adding a date to the name file, and keeping a log of the differences. In addition, a text file will keep the general information about details of the analysis procedure, links to the inputs and outputs, and contact information of the people who created these files.

A master metadata file will be created throughout the research process, and will store information including but no limited to:
1) contact information for project members;
2) a brief introduction of the overall study;
3) data structure, a uniform description of the dataset that helps to locate specific files easily;
4) a master data dictionary that contains abbreviation meanings, controlled vocabularies, etc. ;
5) a summary description of the data collection for each case study project, such as the start and end mileposts of the roadway section, when the data were collected, and what traffic control treatments was placed;
6) a brief description of analysis procedure;
7) URLs for public available reports or datasets, if available.

### Master Metadata Template

Attached is a draft template that will be used for the master metadata.

[Instructions in between square parenthesis]

-----------Context-----------

1. Project title:

2. Project abstract:

3. Project members and contact information:

4. Where to find more information about the overall project:

[Links to other documentation files somewhere else or to project website]

5. Data structure

[An example structure is provided below, add some descriptions if necessary]

    01_CaseStudy1
       01_RawData
         01_TrafficSensor
         02_GPSLogger
         03_Others
           01_Photos
           02_Videos
           03_Observations  
        02_ProcessedData  
        03_DataAnalysis
    02_CaseStudy2 (structure similar to 01_CaseStudy1)
    03_CaseStudy3 (structure similar to 01_CaseStudy1)
    04_Report

6. Data dictionary

[Some examples are provided below.]

COV: Coefficient of variation, a standardized measure of data dispersion. COV is often measured as the ratio of the standard deviation to the mean of a data set.

RWA: Road Work Ahead signs used in work zones to indicate the start point of the advance warning area of a work zone.

PCMS: Portable changeable message signs.

7. Data collection

Case study project number and name:[Example: 01__Swanson Canyon]

Location:[Example: Interstate 84]

Start and end mileposts:[Example: MP 125.5 and MP 129]

Personnel who collected the data:[Surname, Name]

Data collection period:[mmddyyyy - MMDDYYYY]

Equipment list:[Example: 10 M.H. Corbin NC-200, and 5 NC-350 Portable Traffic Analyzers]

Traffic control treatments examined:[Example: PCMS, Pilot vehicle]

Where to find more information about the data collection for each case study project: [Links to other documentation files somewhere else]

8. Data analysis

Software and version used: [Example: RStudio ver Version 1.0.153]

Main data analysis procedures:
[Example]:

1) Data filtering [input: path + filename, output: path + filename]
2) Data aggregation [input: path + filename, output: path + filename]
3) Summary statistics [input: path + filename, output: path + filename]
4) Statistic analysis [input: path + filename, output: path + filename]

Where to find more information about the data analysis: 
[Links to other documentation files]

9. Related materials:
[URLs]

## Storage and Security
For the present study, all data are currently stored on a local computer at the School of Civil and Construction Engineering at Oregon State University, and are also saved on the shared research folder that is hosted by the department and shared by the research team. Both accounts are password-protected. To retain extra copies of the research data, files are synced to the research assistant’s Box project folder automatically, and full backups on an external drive are done monthly and the external drive is kept at a safe place. By saving data in multiple locations and keeping extra copies, it prevents loss or corruption of the data from unfortunate circumstances (e.g., thefts, technological failures, human errors, etc.). 

The local copy and the one on the Box folder will be retained and maintained by the research assistant throughout the duration of the project, while those kept on the shared drive and the external drive will be kept at least 5 years after project completion. This will allow the PI to access, download, and reuse the data after graduation of the research assistant. 

## Access and Data sharing
The data collected in the present study do not contain personal identifiable information or human subjects. All data and associated metadata will be made available on the ScholarArchive@OSU repository under the public domain (CC 1.0 Universal license, similar to a previous study https://ir.library.oregonstate.edu/concern/datasets/mw22vb94j?locale=en). Redistribution, reuse, and creation of derivatives of the data  are allowed. The data will be shared at the time of the research report is published by the sponsor (Oregon Department of Transportation). Spreadsheets in the form of csv files, observational log in the form of pdf files, photos in the form of jpg files, and videos in the mov files will be made available. 

## Archiving and Preservation
It is expected the ScholarArchive@OSU will preserve the datasets as long as possible and ensure the datasets are publicly available. In addition, the PI will keep backup copies (with the same formats as described previously) locally, and retain copies on Box to provide additional security for at least 5 years after project completion for possible additional analysis or data reuse. After that, data will be accessible from the ScholarArchive@OSU website as needed. 
