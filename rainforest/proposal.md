# Group Project Proposal:  
## Amazon rainforest analysis using satellite images, 2017 Kaggle challenge data:

### From: Jennifer Yoon  
### Date: Feb 15, 2021  
### Collaborators: Peter Stephan, Dan Kelly, open to DSML Meetup

### Links:  
kaggle.com
Planet: Understanding the Amazon from Space
Use satellite data to track the human footprint in the Amazon rainforest 
 * https://www.kaggle.com/c/planet-understanding-the-amazon-from-space/overview  
 * https://www.kaggle.com/c/planet-understanding-the-amazon-from-space/data    \-\-\-    
 * Blog of a newbie project using this data:  
https://towardsdatascience.com/land-use-and-deforestation-in-the-brazilian-amazon-5467e88933b  
 * Second project from a student of fastai 2 years ago:  
https://www.kaggle.com/hortonhearsafoo/fast-ai-v3-lesson-3-planet  

### Goal 1:  
Goal 1) To complete the original 2017 challenge with Planet data provided.  Classify images into 17 category labels including cloud cover labels.
We can compare our model vs the leaderboard to see how well we did.  Our goal is to get 95% + accuracy in most categories, esp. on human impact land use categories.  

### Goal 2:  
Goal 2) Possibly extend the project by making predictions about forest locations that are most likely to be damaged next - from illegal logging or mining.  (Or from legal agriculture or settlement).
Data is unbalanced with fewer examples of human settlement, logging, mining, slash & burn, farms, etc.  First, do the usual data augmentation (transforms) to increase samples from human use categories.  Second, find additional image data on human settlement nearby that may be in similar format, possibly labelled.  Look for more data from Planet for outside of the Amazon Rainforest. We may want to add data from other parts of Brazil that has human settlement.  Preferably get images with labels, but if not, use our model to label new images and manually correct "most confused" image labels.
Third, make predictions.  Data was collected from early 2016 to early 2017, so it may be possible to make a prediction by holding back early 2017 dated images.  Will have to get into it to see if this is possible.  If not, we may be able to get Planet images from rest of 2017 in the same format (labelled) to test our prediction.  

### Goal 3:  
Goal 3) Possibly show result over time on a map of the South America, a movie showing progressive loss of prime forest landmass.  This could be challenging.
We would want to get new data from Planet or other satellite image data source for later years, 2017 - 2020 but also earlier years, going back several decades, maybe to 1970.   We may need to do a lot of data processing to get it into a form that will conform with Planet data for 2016-2017.  We also don't have labeled data for any of the other years, so we will be using our model to label images for us.  Our model would need to be 95% accurate or better at classifying the images into 17 original categories.  We would also need to keep track of location identifier, in order to "quilt" the image tiles back together.  Python quilt pkg may be useful.
Final movie can be shown using Tableau or interactive viz using Python Plotly.  (Maybe both, Tableau for non-tech and Plotly for deep-learning people.)  
  
  > Planet Labs - Amazon Rainforest Time-lapse Movie -- applicable to Goal 3  
  > Movie of a sample area within the Amazon.  It starts out pristine in the movie, then gets decimated over time. Movie does not have sound.  
  > https://youtu.be/Cyok7sHSHIQ  
  
This is my proposal.  I would say roll up your sleeves and have at it.  Transfer learning models from fastai class would be a good place to start.  

