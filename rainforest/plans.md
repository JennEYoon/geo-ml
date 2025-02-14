# Amazon Rainforest project writing plans  

### 2024 plan update:  
To finish write-up and data download by Dec 2024. NICFI ends Jan 2025.  
To sign-up for Google Earth Engine for same NICFI data.  
Finish write-up and post online by Dec 2024.  


### Write-up 1, Baseline Training Model:     
 * Re-do clean deep learning training, baseline, resnet34  
    * show downloading data from Kaggle 2017 challenge.  
    * 2k small sample batch, train for 20 epochs.  
    * full 40k, train for 20 epochs -- overfit first.  
    * Test on test set, also try additional data released set.  
    * show prediction on unlabeled images, matplotlib or Pillow imshow.  

### Write-up 2, Planet Labs - Python Data API:   
 * Use Python data API to download sample images from later periods, some can overlap time period to test.  
 * Do we know actual bounding box of area used in Kaggle 2017 competition?  Reproduce as much as possible.  
 * Also download data from Planet Basemap Graphical User Interface  
 * Also try Google Earch User Interface and API  

### Write-up 3: Experiment and Auto-Labelling:  
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
 * Global oil/gas trade economic data and maps, shipping route, refinery capacity, weather.  


