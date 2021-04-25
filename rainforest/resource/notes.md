# Rainforest project notes

### Notebooks with examples and data loading:  

fastai fully worked notebook, 2018 version, by Jeremy Howard:  
https://github.com/JennEYoon/fastai-app/blob/main/fastai/dev_nbs/course/lesson3-planet.ipynb

youtube  
https://youtu.be/9C06ZPF8Uuc 2018 class lesson 3, start time 8 min.
He also talks about dogs and cats.  Uses fastai vesion 1.  

 * Finished DL model, without outputs. 92.96% f-score, 80th ranking.    
https://github.com/JennEYoon/geo-ml/blob/main/rainforest/resource/fast-ai-v3-lesson-3-planet.ipynb  
(similar to "lesson3-planet.ipynb")  

 * software bare metal, less wrapper, fastai:  
https://github.com/JennEYoon/geo-ml/blob/main/rainforest/resource/amazon-satellite-dehazingv1.ipynb  

 * Example with outputs, loading data:  
https://github.com/JennEYoon/geo-ml/blob/main/rainforest/resource/0-93-multi-category-planet-dataset-fast-ai.ipynb  


### Directed Graph:  
directed graph - flow order, from source to destination.  
undirected graph - no direction, can flow either way from A to B, or B to A.  

Rainforest is directed graph because deforestation spread out from source, an existing damaged area, to destinations of primary forest in surrounding area.  Truck accessible road to move hogs and timber out to markets is a critical component of increasing deforestation.   

### Steps, Jennifer Yoon:  

 * Figure out how to load data into Google Colab with Mounted Gdrive path.  Pathlib, how to use.  
 * Download pre-trained model, copy from one of the above notebooks  
 * Load CSV labels into pandas dataframe  
 * Show image example, image[0] * 1.3  # Increase pigment intensity, images too washed out.  
 * Q Is there jpg already in RGB color format??  
 * Train model, unfreeze last layer.  
 * Train model, unfreeze all layers.  
 * Try progressive resizing, smaller image size first.  
 * Try other image quality enhancements.  
 * Look into label mis-labelling issue.  

\-\-\-   

end.  


