# Download Files From Google Driver using Google Drive Download API
This is to Download files from google repository using google driver download API: 'https://docs.google.com/uc?export=download'

Approach:
    Here we have used pythons Requests library to query and download the files from google download API: 'https://docs.google.com/uc?export=download'
   > To download google drive files from google drive using 'https://docs.google.com/uc?export=download' url, one has to have a google drier account or publicly shared google document/file's file_id. 
   > Idea is to download the file from google drive which has the permissions to download(public) using the file_id through above mentioned url. If the file does not have permissions, lets say its resitricted file, then your will be prompted with the appropriate error message.
   > If the file is already downloaded, then it will be overwritten(by default, overwrite option is present if the file is already there). If the file is not present, then it will be downloaded. 
   > There are two types of downloads here:
      1. Download files which are having Content details like Content-Disposition, Content-Length etc in the headers when queried with get request to google download link.
      2. Download files which does not have correct content details ilike Content-Disposition, Content-Length etc in the headers when queried with get request to google download link.

      Files with Content details:
          For these files, I have already kept the file details like file_id, file_name, file_type in one of the files called data/gdrive_file_data.py. User will take these file details and trigger the download form runners/TestExecutor.py file. I have not used pytest/robot framework to reduce the dependecy of libraries to be installed to run these tests
          
HOW TO RUN:
  Go to runners/
  export PYTHONPATH=<path of project>. ex: 
  Execute python TestExecutor.py
