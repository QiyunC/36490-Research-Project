# 36490-Research-Project

Code for the 36-490 statistics research project class at CMU.

This is a group project centered around Forgery Detection of 1649 English newsbooks. Here I have uploaded my part of the code. This code mainly performs feature selection.

This code reads in the csv files with information on different pieces of texts and chooses the features that are best at predicting Ideology for a given text. After these features are generated, we can run dimension reduction algorithms like PCA and visualize on 2D plots whether given a particular Ideology group, some texts differ in features from the main groups of texts to pick out the potential forgery candidates.

## Notes on Functionalities Within and Usages of Files

### The notebook `dataunzip_tfidf_jaccard`:

This notebook contains functions to unzip an archive of newsbooks, analyze the enumeration of all of the `.txt` files to determine the number of available newsbooks, collate them into all possible pairs, aggregate their contents to create a lexicon, develop vectors of weightining of lexical importance for each word in each newsbook, and compute the weighted Jaccard Index of similarity (on a scale of 0 (nothing) to 1 (identical)) for each one of the (all possible) pairs. 

Important NOTE on usage: All of the code is formatted with the expectation that the notebook will be used on Google Drive (via, e.g. Google Colaboratory). Additionally, there should be a filepath within the drive account to which the environment is mounted (i.e. the account on which the ipynb is run). For example, when our group was researching, the following was required: an archive with the filepath `'/content/gdrive/MyDrive/newsbooks_project_36490/newsbooks-1.zip'` exists in the drive of the account on which the functions are run. This *can be changed* by altering the second codeblock: on line 3 of the block is the filepath for the archive unzippping and on line 9 is the name of the directory (relative to the filesystem root folder, *not* the executing folder) into which the unarchived contents will be placed.