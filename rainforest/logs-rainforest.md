# Rainforest Project - work in progress logs  

#### 8/7/2021 Saturday:  

 * S1) Next, load_test_4 - working trained nb, test writing to "submissions_csv" file, make prediction.  
       - Use 2000 images test images first, not all 40,700.  
 * S1b) Make a couple of predictions, individual images.  Did it produce correct labels for test images?  
 * ---   
 * S2) Run other models.  Test exporting again.  Use GPU and CPU.  How to export as cpu for production?   
 * S3) Try chp 2 "bears" category,  How to export model as cpu?  Host on my Amazon AWS s3. 
 * S3b) Extend "bears" to 3 categories, "black bear", "grizzly bear", and "teddy bear"; and use multi-category block.  
 * ---  
 * S4) Do image enhancements, sk-image.  
       - try fat pixels, different colorization from tif to rgb, adjust light for jpg.   
 * S5) Explore planet-labs colorization images.  
 * S6) Planet - download "orders" using planet_data_api.  
       - review Planet's data_api tutorial   

## Rainforest, Ideas:  

### Data, improve:  

 * simplify categories, try 5-6 (road, water, agriculture, slash_burn, mining, primary)  
 * Maybe just 3? (primary, road, agriculture)  
 * Try prediction, where, need location information, download with coordinates from Planet Labs.  
 * numbers not even across category, even out road, agriculture, with primary only category.  

### Data, quality improve:  

  * jpg images too dark, try ndarray * 0.3, brighten 30%.  
  * apply filter to jpg image to enhace contrast and brightness.  
  * recreate jpg from tif, use different formula.  tif is the original from satellite. 
