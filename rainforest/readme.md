# Project Proposal: Amazon Rainforest, 2017 Kaggle Challenge data

### Author: Jennifer E Yoon  

### Collaborators:  
Peter, Dan, maybe others from a local Meetup.

### Date: Feb 15, 2021 start  

### Goal 1) Reproduce original 17 class image identification task  

Baseline use Resnet34 and transfer learning,   
unfreeze last layer for one-cycle learning, 2 cycle fine tun,  
then unfreeze and retrain all 34 layers, fine tune 20 cycles (slower learning rate for earlier pretrained layers).  

### Goal 2) Predict areas most likely to be exposed to human deforesting activity  

Date: Get other years data from Planet.  
Label data using our DL model, once it's 95% accurate at identification  
Augment date using proceeses  
Maybe Augment data from outsize Amazon-region, at other inhabited places in South America.  
Balancing the number of human inhabited image with forest image is going to be a challenge. 

### Goal 3) Visualizaion, time-series mapping, movie of Amazon-Rainforest damages over time.  


### Kaggle Data source 2017:  

<link>

### Student 1 project example:  

https://towardsdatascience.com/land-use-and-deforestation-in-the-brazilian-amazon-5467e88933b  
https://medium.com/@cambostein 
 * from General Dynamics Bootcamp, capstone project:  
 * example using GeoJason data format.  


### Student 2 project example:  

fastai v3 student's notebook, closer to what I want.  
50 layer deep learning model 

### Other links:  

GIS open data format  
