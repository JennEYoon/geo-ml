# Report for Baseline training model, jupyter notebook  

### Baselin model: Write a tutorial instead of a showing work notebook  

 * Download data from Kaggle 2017 competiion, has both labeled training set and labeled test set.  
   - Also has "additional" labeled datase, was used for final judging by Kaggle.  
   - Sidebar: how to use Kaggle API to download dataset.  
   - Sidebar: tar and untar commands, bash/linux  
 * Load into Python fastai library, show image samples  
 * Create 2000 images small sample, run trining on this, to save time if model does not work.  
 * Use full 40,000 sample, trian. Try to overfil, then back off.just  
 * Try using subset of data, categories  
 * Try bigger model, try fp16  
 * Try infrared channel (only? for river or cloud cover?)  
 * Straight lines, road - edge detection?  

### Get Planet NICFI dataset, 2017 - 2022 

 * Tutorial on how to download using User Interface, and Python API  
 * Examine data, show image some. Select a small area to download first (AOI, near Manais, Edge near farms, Deep in forest)
 * Train model on ResNet34. Small sample dataset. Predictions on unlabeled data.  
 * Manially verify 2000 images for label accuracy, calculate category prediction accuracy.  
 * Try limiting categories to (forest, road, river, mining, burning/smake, agriculture, cattle ranch, aboriginal agriculture, mining)
 * Use corrected data and retest.  
 * return to Kaggle labeled data, manually verify a sample of 2000 images, find categories where model is most confused.  
 * retrain after manual verification of labels.   

 
