# DBGuideInstructEmbed
Natural Language Search to return pdf using Hugging Face Instruct embedding model.  <br />
Create a file in GoogleDrive called PDFs.  
Put PDFs in file MyDrive/PDFs.  
Creates a Vector database in MyDrive/VectorDBs/PDFsVecDBInstruct.  
On each run, it will check if any new pdfs have been added to the PDFs file, and if so, will add them to the database.  
It does not check if PDFs have been deleted. Currently, if the number of pdfs is small, easiest is to delete the VecDB file and it will rebuild the database from new.  
Make sure to select a GPU in the runtime type in colab.  
It returns an excerpt to help you choose which pdf you should choose (but would recommend the user then get the full pdf to ensure they get the full context to answer their query).  
It always returns the 4 'best' matches - if there are no 'good' matches then it will still return the 4 nearest, even if they are unhelpful (the user has to make that assessment).  
