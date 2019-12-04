# Visual Search Engine (CBIR)
[ INDP3 AIM - SUPCOM ] Project : Visual Search Engine  
Realized by :  
• **Ihebeddine Riahi** : ihebeddine.riahi@supcom.tn  
• **Chaima Bouzaidi** : chayma.bouzaidi@supcom.tn  

## Table of contents
1. [Overview](#Overview)
2. [Requirements](#Requirements)
3. [Setting up MongoDB/GridFS](#Setup)  
4. [Start the App](#StartApp)


<a name="Overview"/>  

## Overview
This Visual Search Engine (CBIR) allows users to send a request image in order to display similar images from 1M images stored in GridFs (MongoDB).

<a name="Requirements"/>

## Requirements
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Install MongoDB (version 4.2.1).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Install Python (version 2.7.15+).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Create a MongoDB database called `CBIR`.   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Specify your MongoDB connection URL in the script `app/app.py`.    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Go to `app/` directory and install the requirements via pip :  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • `pip install flask numpy scipy matplotlib scikit-image gunicorn`.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • `pip freeze > requirements.txt`.  


<a name="Setup"/>

## Setting up MongoDB/GridFs
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Go to `scripts/` directory and run toGridFs.py script in order to dump the Thumbnails, the Principal Components and the VP-Tree into GridFs :  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • `python toGridFs.py -td <YOUR_THUMBNAILS_DIRECTORY> -id <YOUR_PC_VPTREE_DIRECTORY>`.  
**NB** : You can get the Principal Components and the VP-Tree files from Dropbox : ` `.  


<a name="StartApp"/>

## Start the App  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Run `python app/app.py` to start the App.  
**NB** : The list of query images is static. You can change it by hosting the thumbnails on a Free server `https://fr.imgbb.com/` and specifying the image URL in `img` tag in `app/templates/index.html`.     
