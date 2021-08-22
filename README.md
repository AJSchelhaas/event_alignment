# Automating Event Alignment in Football Match Reports
The data and material used in my master thesis project on event alignment in football matches.  

## evaluation_dataset.tsv
This file contains manually event aligned sentence pairs from match 2002833. This file was used as the evaluation file for the project.  

## match_reports_dataset.zip (not made public)
This zipe file contains the collection of match report text files. Each folder has the UEFA match ID.  
Within each folder there are text files. The name of the file indicates the language of the match report.  
* NL indicates Dutch match reports  
* DE indicates German match reports  
* EN indidicates English match reports 

## events_all.zip (not made public)
This zip file contains the structured data files that the model uses to create event alignment pairs.

## Master_Thesis_Main_Model.ipynb
This file is a Python notebook. It includes one code block that can be used in Google Colab to download all the required packages.  
If you want to use the model, there are a few variables you might need to change to make it work for your system.  
By default it will attempt to mount to a Google Drive folder, but you can turn this off by deleting the line that says 'drive.mount('/content/gdrive')'.  
* First you need to change 'txt_directory' to the path that leads to the folder 'match_reports_dataset'. 'match_reporst_dataset' should be a folder containing the contents of 'match_reports_dataset.zip'.  
* Second you need to change 'sum_directoy' to the path that leads to the folder 'events_all'. 'events_all' should be a folder containing the contents of 'events_all.zip'.  
* Third you need to change 'use_embeddings_for_scoring' to False if you want to use BLEURT. Change it to True if you want to use embedding cosine similarity.  
* Fourth you need to change 'match_id_input' to the match ID that you want to extract event alignment pairs from.
* Fifth you need to change 'k_amount' to the K value that you desire. By default it is 5.

## Contact
If you experience any issues, feel free to email me at the following addresses:  
a.j.schelhaas@student.rug.nl or arjan.schelhaas@live.nl  
