# Amazon Rainforest project write up plans  

### Plan for write-up 1, baseline training model:     
 * Re-do clean deep learning training, baseline, resnet34  
    * 2k small sample batch, train for 20 epochs.  
    * full 40k, train for 20 epochs -- overfit first.  
    * Test on test set, also try additional data released set.  

### Plan for write-up 2, Plandet Labs data API:   
 * Use Python data API to download sample images from later periods, some can overlap time period to test.  
 * Do we know actual bounding box of area used in Kaggle 2017 competition?  Reproduce as much as possible.  
 * Also download data from Planet Basemap Graphical User Interface  
 * Also try Google Earch User Interface and API  

> contact Planet Labs after this step - 10 days focused work.  

### Experiment and Write-up 3: auto-labelling:  
 * Try auto-labelling other time period images using trained models.  
 * Predict labels, pretrained weights in .pkl file.  No need to fine tune.  
 * Need to manually label some images in order to get test set. 
 * Yes but need ground truth to be sure, Me label 500-2000 images should do it (validation set), make sure to have enough of all classes.  
 * Then go back and improve training model. Iterate back and forth.  
 * Source image in Kaggle had way more primary forest class than other classes.  
   - Think of ways to balance class samples.  Does it matter?  
 * Infrared channel uses?  

### Write-up 4, Overview for lay audience:    
 * Explain Area of Interest, JSON file format.  
 * Explain history, politics, rainfall dependency on the trees.  
 * Add historical older images from LanSat.  
 * Later -- My own version of deforestation movie, add music and detailed comparison time snap-shots, voice over and pause at major changes.  
 * Later -- Add to it with newer data I am working on.  

### Write-up 5: Economic ML anlaysis:  
 * Compare deforestation with global trade and market for Brazil Beef, Soybeans.  
 * Measures of precepitation and temperature in Amazon Rainforest, in context of global climate change (faster/slower).  
 * Compare to economy of Brazil, global economy. Global price of beef, soybean, oil & shipping cost.  
 * EIA.gov - download oil trading data, for API use case demo.  


