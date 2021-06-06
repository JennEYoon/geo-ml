# Working logs, 2021, Amazon Rainforest project 

Jennifer Yoon's working logs.  

#### Feb 21, 2021:  

  * Slack, need to add announcement and tell people to browse channel and add project.  

  * Chp 10 tokenization - to char tokenization on my own using Numpy, then look at PyTorch char tokenization.  
  * Lookup Word2Vec.  How is stem identified?  How much is manually fixed?  
  * Breaking up matix into A, B, C blocks by column numbers, look for real world use, how large are the blocks? Do sentence wrapping fit inside most blocks?  
  * Review matrix multiplication in Numpy, breaking up large arrays into column blocks, yet still keeping track of adjacent bordering columns, when calculation, then putting it back into shape.  
  * Image also stack into long rows, then puts back into shape.  But does not break up word wrapping, one long row per image. Sentences are not all the same length, need to keep track of which cell was next at the edges of block.  

#### Feb 28, 2021 Sunday:  

  * detailed data & project description review, 5h  
    - Main data need BitTorrent. Not sure how to get at the data without it      	 - use Kaggle API?  
    - Sample code in fastai nb, not a full exercise, seems to be practice.  
    - Leaderboard -- 1st 0.93317, 101st 0.92894, 201st 0.92535, 714th 0.85019  
      Most people got around 93% accuracy.   

  * Found a somewhat related nb, Brazil deforestation increasing?  
    - No image analysis, tabular data correlations only.  
    - fire events, el nino, sqft primary forest per country, annual data.  
    - only fire data has location info 
      (latitude, width, N/S from equator; and longitude, height, E/W from 0)
      (Greenwich Meridian is in Greenwich Park near London)

#### March 1, 2021 Monday:  

  * BitTorret, UTorrent -- failed to download fully, stopped partially.  
  * File too big, won't open.  Should be a folder structure with smaller image files within, .tif format. 
  * Bill helping with it.  
  * Not enought seeds (providers of complete download) for BitTorrent to work. 
  * Discovered download icon for .tar files, directly from Kaggle.  
  
  --  seup WSL Ubuntu ---  
  * Installed Ubuntu desktop, GUI.  
  * Installed Jupyter Lab on "dlpy" conda env.
  * Enabled startup XLauncher - Ubuntu 
  * Firefox works!  Pops up window when start jupyter lab  
    Text fuzzy, not like Windows native applications. Maybe WSL limit program size.  Looks identical to URL copy to Chrome, but fuzzy resolution.  
  * Windows - only one conda env, "base"/ 
  * base has jupyter lab installed.  
  * Moved repos folder to inside Google Drive, Updated Google Drive to 200GB - large data files for deep learning. 
  * Use Google Cloud Platform -- paid service next.  
  
#### March 2-3, 2021 Tues - Wed:  
 * Successfully downloaded .7z files to external drive.  
 * 7Zip software installed on windows.  
 * Extract does not seem to work yet, Ubuntu?  
 * File open OK, but images pale.  
 * Try again from Ubuntu Terminal.  

#### March 3, 2021 Wed AM:  
 * Everything downloaded to external USB2 drive, 102 GB total space!!!  
 * Deleted a lot of folders, and moved whole python folders from C drive to external drives.  
 * 82GB free on C drive now.  
 * Working python folders moved to SDXC card, 128 GB.  
 * Data-Planet on D drive, USB2.  
 * All photos, music, document moved to USB Stick, 128 GB  
 * Removed unused programs.  Completely removed python from C drive.  
 * Ubuntu remove all conda env except 2, base, fastai20.  
 * Install jupyter kernels to both envs. ipykernerls, nb_kernels etc.  
 * -  
 * Load image and disply inside notebook.  
 * Next see how to show rows or images using Matplotlib.  
 * Fastai - how to load images and show in notebook. 

#### March 8, Monday 0:55 am:  
 * Github repo - To upload 500 jpg images, after convering to RGB color scheme.  
 * Also upload to Google Drive.  
 * Same for tif files unconverted.  
 * Find out how to split channels efficiently, test.  
 * Pause while working on Fastai for Meetup.  

#### March 19, 2021 Friday Update:  

 * ***Next - upload data into Google Colab using Google Drive.***    
   - 40K JPEG files train, test saved to Google Drive "data-large" folder.       Only 2 GB so far.  
   - 30 files per category saved to "geo-ml" repo.  
 * ***Then next - try fastai chp 6, multicategory model.***    
 * Planet -- special free data available during 2020-2022.  
   - Biannual, 2015 Dec, 2016 June/Dec, 2017, 2018, 2019, 2020 Dec latest. 
   - AOI interactive "order" tool, python API (need key) tool, learn how to use.  
   - Downloaded data, extended license with attribution, attach same copyrigth, non-commercial use, for assisting conservation cause or personal research.   
 * Youtube and News - research on Amazon Rainforest condition, 2019 and 2020 were extremely bad years, from political source, Bolsonaro president.  

 * Bill Gates book, How Not to ... - 51 billion tons of carbon dioxide emssiion per year, globally, as of 2020.  Need to reduce to net zero by 2050 or earlier, if possible.  Daunting task.  Maybe possible with global effort and new innovations.  

#### March 30, 2021 update:  
* Last week monday, small group, Peter volunteered to take a look at Python API from Planet Labs.  
* Talked to Dan today, he may start working on project.  
* Today, organized resource links, posted on Slack DSML. Cleaned up reference info.  


#### April 26, 2021 small group:  
 * Met with Peter, Dan, me, and 3 new people, Sampath, Sid, Ken.  
 * Sampath is finishing his Masters in Data Science in May 2021, Sid has been taking MOOCs still relatively new to data science, Ken?  
 * We'll all try to get fast.ai 2018 NB 3 to run and think about the project.  
 * Peter - PlanetLabs Python API
 * Me - how to improve model  
 * Sampath colorization, jpeg image quality enhancements?    
 * goal 3 movie, which areas to pick for demonstration?  
 * Directed graph idea using geo-location id (lattitude and longitude).  

#### May 29, 2021 Saturday:  
 * DataBlock - creates a list with items reference to file names, file Object.  
 * Try manually making a list with 3 items in a folder path.  
 * Testing software folder.  
 
#### 6/5/2021 Saturday:  
 * Working on DataBlock - iterable collections class.  
 * URLs.PLANET_SAMPLE and URLs.PLANET_TINY have jpg images served from fastai s3.aws bucket.  
   - Use these first to run notebook, Ubuntu local computer and Google Colab connection.  
   - Try glob  
   - Try os.walk  
   - Try fastai data_external.ipynb (.py)  
 * Scikit-Image tutorial from SciPy2018 -- finish watching, incorporate into Rainforest Project.  
   - filter will be useful, enhance color contrast on images.  
 * Rainforest Ideas:  
   - Try simpler categories, primary forest, road, agriculture, and cloud/haze only.  
   - Importance is if there is a road nearby, and a cattle slaughter house nearby.  
   - Logging and Cattle export need road.  
   - Look at discrete time periods, after Bolsonaro, after right-bottom area deforested, after trans-Amazon highway.  
   - After conservation policy and enforcement - how much of forest was recovered, or reduced rate of forest loss.  



