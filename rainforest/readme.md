# Amazon Rainforest project:   
Based on a 2017 Kaggle Challenge, Planet Labs data, NICFI data, 
Amazon Rainforest satellite image deep learning project.  

### Author: Jennifer E Yoon  

### Contents: 
 * See "Proposal.md" for plan.    
 * See "PlanetAPI-info.md" for accessing data from Planet Labs. 
 * See "resource" folder for other useful links.  
 * See "tests" folder for deep learning Jupyter notebooks: 
    - image loading tests
    - initial deep learning training tests
    - more deep learning training and predictions 
 * See "movie" folder for animation, deep learning training results.     

---  

### Project Management Logs:  

#### July 25, 2021 update, loading data:  

 Testing loading data, planet-2k, URLs.TINY_PLANET:  
  * C:\Users\jyoon\gdrive\repos\geo-ml\rainforest\tests\mytest_nbs\ 
      data_load_test2.ipynb
  * planet jpg image size (256, 256) 3 channel.  

#### Summary - 6/7/2021 small group:  

 * All files are in geo-ml repo, rainforest folder:  https://github.com/JennEYoon/geo-ml/tree/main/rainforest 
 * Word file I was using:  https://github.com/JennEYoon/geo-ml/blob/main/rainforest/tests/rainforest-load-jy1.docx 
 * More notes on loading data: https://github.com/JennEYoon/geo-ml/blob/main/rainforest/tests/load_data.md 
 * nb 04_data.external, fastai code:  https://github.com/JennEYoon/fastai-v2-app/blob/main/fastai/nbs/04_data.external.ipynb 
     (I save a copy to my repo "fastai-v2-app" but you can get it from fastai's own repo.  https://github.com/fastai/fastai)

Small amount of image files and my practice loading:
 * Tests folder:  https://github.com/JennEYoon/geo-ml/tree/main/rainforest/tests
 * From Google Drive mounted on Colab:  https://github.com/JennEYoon/geo-ml/blob/main/rainforest/tests/mytest_nbs/JY-notes-gdrive-v3.ipynb
      Previous google drive loading
 * Loading test local cats folder, my laptop ubuntu:  https://github.com/JennEYoon/geo-ml/blob/main/rainforest/tests/mytest_nbs/img_load.ipynb 
 * I created the "cats" folder inside "tests".  Both are under "geo-ml" repo.     

#### Scikit-Image seems good for colorizing, enhancing jpg image quality   
It's also good for adding graphic elements to an image, or doing numpy array style manipulations to an image.   
Tutorial - Scipy 2018:  https://www.youtube.com/watch?v=arXiv-TM7DY&t=148s  
There's 2019 version, very similar to 2018:  https://www.youtube.com/watch?v=d1CIV9irQAY  

#### napari, good for displaying images, filtering   

#### Planet API tutorial, SciPy 2018 Conference  
 * folder linke here, youtube video link  

#### Concepts for loading image files: 
1) Very broadly, image.open() and other library is needed to load into memory.  Pathlib is only a pointer (address) to the file.  File is not loaded into memory.  
2) To display image inside a notebook, plt.show() matpltlib, im.show() pillow, show_batch(3, Image_size=x,y) fastai, etc., need to be called.  
3) Path class from pathlib.py is used for dealing with folder structure (tree) and is OS agnostic, can use with Ubuntu and Windows.   
3b) untar_data(URLs.xxx, path=dest)  May be able to change default data download location.  
4) DataSet is a list, contains pointers (addresses) to image files.  
5) Collections -- need some way to use Path dest and DataSet list, to loop through each image file and load into fastai DataLoaders (dls).    
5b) Collections need at a minimum, 
   > ```__init__(), __len__(), and __get_item__() ```  
   > methods defined.  Fastai lib does this in "04_data.external.ipynb".  

#### General Project Ideas:  
  * We want to simplify dataset and training model as much as possible.  
    - use URLs.PLANET_TINY, fastai dataset, has less number of images.  
    - 6/14/2021: created small jpg dataset with 2,000 images per train, test folder, and labels csv file with 2000 items. 
       * Will use this and PLANET_TINY on first pass, to test models.  
       * Also need a simpler non deep-learning baseline, statistical average or regression methods.  
    - use only few important categories to train (primary forest, road, agriculture, maybe river, maybe haze), instead of 17 categories.  
    - selectively sample only images that match the above 3-5 categories.  Training set has more of these important categories.
    - try training with only 1 category per image, preference labels (road, primary forest, and agriculture).
  * Pre-trained models:  
    - simplest one first. Resnet34?  
    - fastai dataset imagenette, smaller set than full imagenet, may have pre-trained model.  
    - Refer to fastbook nb5 Pet Breeds and nb6 Multicategory -- for possible pre-trained models.  
    - Also use progressive image re-sizing (small to large) -- from fastbook nb7.  
    - Also use fp16 on all models. Is faster and equal or slightly better in learning quality.  
  * Later - model extending:  
    - For updating to recent years (2019 - 2021), concentrate on small regions, where there is already a road and a cattle slaughterhouse.  
    - Get (long, lat) coordinates and download Planet Labs Basemap for these smaller area(s).
    - Use colorized and enhanced images from Planet Labs Basemap -- download for a few years first (2019, 2016)
    - tif files -- Try recreating jpg file from original tif files using a different formula to strip out channels (Scikit-image library).  
    - data augmentation - image chip coordinates. We can use different way(s) to define image chips.  
      Randomly assign beginning (top-left) coordinates, and randomly size and crop images (row and column pixels). 

---  

