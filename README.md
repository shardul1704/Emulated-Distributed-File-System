**DSCI 551 MIDTERM PROJECT REPORT**

An insight into Climate Change using Emulated Distributed File System

![Shape1](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

**Contents:**

Group Members and Background

Project Description

Objectives

Workflow

Datasets

Implementation of Task 1

Outputs

Workflow for Task 2

Example Queries

Framework/Tools

![Shape2](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

**Group Members and Background:**

Shardul Nazirkar (USC ID - 6028439069) - B.Tech in Information Technology - Vishwakarma Institute of Information Technology, Pune, India

Niharika Abhange (USC ID - 1171034845) - B.Tech in Computer Science and Engineering - Maharashtra Institute of Technology, Pune, India

Nachiket Dunbray (USC ID - 7291924419) - B.Tech in Computer Science and Engineering - Maharashtra Institute of Technology

![Shape3](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

**Project Description:**

Climate Change is no longer a scientific theory. It is a real and devastating phenomenon that threatens life and our planet as we know it. The biggest reasons the circumstances keep deteriorating are rampant misinformation and lack of awareness and access to data. Some say it's a hoax but according to science and research, drastic changes in the environment have been reported in the last decade.

Every citizen of the world needs to comprehend the gravity of the situation before we reach an ultimatum. Statistics and Data are the most powerful tools to make the truth accessible to the public eye. This project will give in to the fact that climate change is real and has grave consequences, taking into consideration Datasets of the Global temperature, Sea water levels, and Ozone Layer.

![Shape4](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

Objectives:

1. To understand and design an EDFS, for different kinds of datasets based on Firebase and MySQL.
2. To implement partition based map and reduce as a part of the file handling system.
3. To correspond the file system to an application interface that is intuitive, well designed and allows the user to access the data seamlessly.
4. To optimize the system until it serves its purpose- creating awareness and providing accurate insights into the global climate scenario.

![Shape5](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

Workflow:

1. Construct Firebase-based emulation for a DFS.
2. Implementing partition based map and reduce (PMR) on data stored on EDFS, for the search or analytics functions in your application developed in the next task
3. Creating an app for searching the data stored in EDFS using the functions implemented using PMR.
4. Analytics operation to be performed on: Change in the different levels of the factors like ozone layer depletion, Temperature change, sea water level rise, etc.
5. Create an application interface that interactively exhibits different parameters that have been analyzed in step 4. Allow users to intuitively navigate through the dataset, and compare values based on locations and year, etc.

![Shape6](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

Datasets:

The following 3 datasets will be used in the course of this project:

1. Earth Surface Temperature:

[https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data)

1. Sea Water Level

[https://www.star.nesdis.noaa.gov/socd/lsa/SeaLevelRise/LSA\_SLR\_timeseries.php](https://www.star.nesdis.noaa.gov/socd/lsa/SeaLevelRise/LSA_SLR_timeseries.php)

1. Ozone Layers - [https://www.kaggle.com/datasets/jimschacko/ozone-layer](https://www.kaggle.com/datasets/jimschacko/ozone-layer)

We aim to provide global insights into the effects of climate change. Hence datasets with ranges across the globe have been chosen. The availability of information for as long a time period as possible has been ensured.

Direct correlation to Climate change: The parameters of the datasets included- Earth Surface Temperature, Sea Water Levels and Ozone are directly correlated to climate change. These 3 parameters taken into consideration will provide a comprehensive insight into the quantitative effects of climate change.

![Shape7](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

IMPLEMENTATION OF TASK 1:

The main() function will be executed to create the initial structure of EDFS for every new instance. The namenode and datanode are created in this step.

This command is implemented in Jupyter notebook.

![](RackMultipart20230129-1-diacz6_html_8495ec50fdad5784.png) ![](RackMultipart20230129-1-diacz6_html_31e4117ff57bc708.png)

![](RackMultipart20230129-1-diacz6_html_d228c3e222fc43e.png)

![](RackMultipart20230129-1-diacz6_html_60e98f07d0c7f81.png)

Implementation of commands:

The mkdir command is executed to create a new directory, and it involves specifying the Block location. The mkdir function and its structure in the realtime database system are shown below.

A global variable named location also defined to store the location of the current directory that is being used.

![](RackMultipart20230129-1-diacz6_html_c9496697078b8e01.png)

Following this are the screenshots and corresponding realtime database outputs of other EDFS commands like cd, ls, pwd, getchwd, put, and rm.

![](RackMultipart20230129-1-diacz6_html_42af7f59a392656f.png)

![](RackMultipart20230129-1-diacz6_html_21475990950c98c2.png)

![](RackMultipart20230129-1-diacz6_html_3050ac0eef014610.png)

![](RackMultipart20230129-1-diacz6_html_acd17d246956d4aa.png)

![](RackMultipart20230129-1-diacz6_html_d3eaf38c1365c26d.png)

The next function getPartitions() function gives us the locations od the file partitions. ![](RackMultipart20230129-1-diacz6_html_eb7f78884fde4961.png)

After getPartitions() the actual contents of the file are read by the readPartitions() function. The implementation of readPartition(file, partition#) which returns the content of partition of the specified file is given below.

![](RackMultipart20230129-1-diacz6_html_f169e9f4d74dd14a.png)

OUTPUTS:

Main Structure of System ![](RackMultipart20230129-1-diacz6_html_3fd56ec0f01c9cb5.png)

Implementing the CLI commands ![](RackMultipart20230129-1-diacz6_html_d7fb69eedf4f045f.png) ![](RackMultipart20230129-1-diacz6_html_300f838dabcd48b0.png) ![](RackMultipart20230129-1-diacz6_html_4af38bf9197c119b.png) ![](RackMultipart20230129-1-diacz6_html_5debc396e7b02e4a.png) ![](RackMultipart20230129-1-diacz6_html_899db7fb002eaf76.png) ![](RackMultipart20230129-1-diacz6_html_711918814798e5c2.png) ![](RackMultipart20230129-1-diacz6_html_bf4174a3f8caea1f.png) ![](RackMultipart20230129-1-diacz6_html_f5e028a43506f0ce.png) ![](RackMultipart20230129-1-diacz6_html_36c7298bbf8859d7.png) ![](RackMultipart20230129-1-diacz6_html_b38fbcebe0bec340.png) ![](RackMultipart20230129-1-diacz6_html_52cfbc0f31c16bb7.png) ![](RackMultipart20230129-1-diacz6_html_d053f994b418c531.png) ![](RackMultipart20230129-1-diacz6_html_1bb6ea6d94f4494e.png)

CODE SNIPPETS FOR MySQL IMPLEMENTATION

CODE SNIPPETS

![](RackMultipart20230129-1-diacz6_html_9e026f029fa372c5.jpg)

![](RackMultipart20230129-1-diacz6_html_b5fde06a2abe971f.jpg)

![](RackMultipart20230129-1-diacz6_html_b4a4a4979a2754a1.jpg)

![](RackMultipart20230129-1-diacz6_html_659d925da8181160.jpg)

![](RackMultipart20230129-1-diacz6_html_ae3c79183b3e00be.jpg)

![](RackMultipart20230129-1-diacz6_html_904685594a0cc144.jpg)

![](RackMultipart20230129-1-diacz6_html_da69eb05dbabdf89.jpg)

![](RackMultipart20230129-1-diacz6_html_ea33be547d70ec1.jpg)

![](RackMultipart20230129-1-diacz6_html_4c3e7645222587a0.jpg)

![](RackMultipart20230129-1-diacz6_html_654566e9168bd790.jpg)

![](RackMultipart20230129-1-diacz6_html_c1d1aff47fa7ac42.jpg)

![](RackMultipart20230129-1-diacz6_html_797825d4a6b5907.jpg)

![](RackMultipart20230129-1-diacz6_html_9a63de08cb1a7064.jpg) ![](RackMultipart20230129-1-diacz6_html_15a16ce9a080ab86.jpg) ![](RackMultipart20230129-1-diacz6_html_b079c24eae63b78a.jpg) ![](RackMultipart20230129-1-diacz6_html_d5e1505a90a54fbd.jpg)

![](RackMultipart20230129-1-diacz6_html_f0879036e1325b1.jpg)

![](RackMultipart20230129-1-diacz6_html_fdb825f8a16ad4f6.jpg)

![](RackMultipart20230129-1-diacz6_html_b3ac4412d98f4885.jpg)

![](RackMultipart20230129-1-diacz6_html_2b9a64dbe564ed17.jpg)

![](RackMultipart20230129-1-diacz6_html_a5f525f9ee13bc5d.png)

Analytics and Search Outputs

Sea Level Variation with Standard deviations per year between 1992 to 2002

Framework: Firebase, MySQL, Stream-Lit

Language: Python

Library: JSON, Requests, Matplotlib, Pandas, NumPy, Seaborn.

![Shape8](RackMultipart20230129-1-diacz6_html_237499165a11f2b9.gif)

We hope this project makes the right use of Statistics and Data Management tools and bring the fact that climate change is real and has grave consequences to light.

Analytics and Search operations using Partition Map Reduce

The task 2 is the final implementation of our project.

Implementation of Partition based map and reduce on data stored on EDFS, for search and analytics

- The map function takes input as the number of partitions and gives all the partitions as output.
- The reduce function takes each partition and gives a single output after combining them.
