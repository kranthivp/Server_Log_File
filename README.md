# Server_Log_File

## Notebook Link

https://colab.research.google.com/drive/1ofH5dJs7KB2IoE8UwApMnm1ChZ87Vpmn#scrollTo=dxSNJXfUmHPz

## Problem Statement

The task is to fetch the data from a server log file, extract all the email addresses along   
with their corresponding dates and upload the data into a user history database.
The goal is to ensure extracted data is clean, accurate and accessible for further analysis and historical tracking.

## Steps followed

Step 1:-  From the given url the data is loaded into Colab notebook.

  'https://drive.google.com/file/d/13qr0NacvjeqC1jPESa8A3ViFY8XtEQAb/view'  

Step 2:-  Script to download the text file from local.

  'Text_File=open('/content/mbox.txt','r').read()'

Step 3:-  Using Regular expression all email addresses along with their corresponding date and time are retrieved.

Step 4:-  script used to retrieve the data.

 import re
 pattern = 'From([\s][a-z0-9]+[\.]?[a-z0-9]+[\@][a-z]+[\.]?[a-z]+[\.]?[a-z]+[\.]?[a-z]+[\s]+[a-zA-Z]+[\s]+[a-zA-Z]+[\s]+\d+[\s]+\d+[\:]\d+[\:]\d+[\s]+\d+)'
 match = re.findall(pattern,Text_File)

step 5:-  Ensured the extracted data is in structured format suitable for database insertion.

Step 6:-  Format of the date is converted into a standard format (e.g., YYYY-MM-DD).

Step 7:-  Pymongo installation 

  !python -m pip install "pymongo[srv]"
  
Step 8:-  The processed data is saved into a MongoDB collection with name user_history.

step 9:-  Data is fetched back from MongoDB collection into dataframe.

Step 10:- sqlalchemy installation

     # installing sqlalchemy to convert DataFrame into Database table
       !pip install sqlalchemy
       
Step 11:- Data is uploaded to a relational database(SQLite) using python code.

Step 12:- The table is named user_history.

Step 13:- Streamlit installation.

      !pip install streamlit

Step 14:- Localtunnel installation.

       !npm install -g localtunnel

Step 15:- sql queries are executed on the database and output is shown in streamlit




