## S1) Timeline of Rainforest project  

#### Jan 30, Agree on Amazon Rainforest for group project, Peter and Dan and me.  ~ 0.5 wk

#### Feb - try to download Kaggle data, problems.  ~ 1.5 weeks
 * Also read about other Kaggle projects, get to know Kaggle platform.  

#### March - full month solid work on project.  
 * first week, get Kaggle data downloaded, unzipped.  
 * Upload to Google Drive, share link with Peter and Dan  
 * Read about Amazon deforestation in recent decades.  
 * Read about Planet Labs and planet-data-api, free data during 2019-2022 due to external funding.  
 * Write on slack message to team-mates, create project channel  
 * Download useful fastai related notebooks  
 * Update repo geo-ml for rainforest project content.  

#### April - almost no work.  Personal stuff  

#### May - only 1 week of work, learn pathlib, regular expression, pandas
 * Start trying to understand fastai software, review fastbook chp 1-6

#### June - only 1.5 week of work, learn ways to show image in notebook.
 * Explore fastai software, look at chp 19, external fastai nb.  
 * More reiew of fastbook chp 1-7
 * Read chp 18, beginning chp 19, review 8 and 9. 

#### July - SciPy, ~2 weeks for project.  
 * Run focused tests in image input.  
 * Try out matplotlib, pillow, and sklearn image input methods.  
 * Rewatch tutorials on image manipulation. 
 * Rewatch all fastai 2020 lessons 1-8.  
 * Watch some code walk through video 1, 2019 foundations, lesson 8 (first).  

#### Aug 1-12, 1.5 wks

##### 8/2 - 8/6, 50hrs - finally get data loader to work, runs model  
 * resnet34, sample 2000 jpg data, not all 40,000.  
 * brighten 20%, resize to 224 pixels, maybe due to pre-trained model's image size?  
 * flip=true augmentation. 
 * 20% split into validation set, random selection from 2000 input images, seed set to 42.  
 * **Result: fbeta_score 0.923.  Top 0.93x**  
 
##### 8/10/21 Tuesday -- Presented to Meetup
 * Pre and post presentation review, fastai videos/book.  

## S2) Timeline to this point  
 * Calendar time, 8.3 months.  
 * Work on Project time, including learning libraries, 12 weeks, ***3 months***.  

## S3) August - October 2021, extend project  

#### I) First, test current model more --  
 * Test first, predict on known unused jpg images with labels.  
 * Test saved model, see if loading works.  
 * Test on all 40000 images. 
 * Try k-fold cross-validation instead of random splits, run model several times with controlled split, then average model parameters.  

#### II) Next, change input quality, categories, models, training --
 * improve source image quality, simplify categories down to 5 or 6 from 17, try different models and freeze and re-training.  
 * to run more tests.  improve source image quality, simplify categories down to 5 or 6 from 17, try different models and freeze and re-training.  
 * Manually verify 2000 jpg image labels, make corrected labels, use this to retrain the model.  Improvement?  
 * Try against "additional-jpg" images and labels provided (private set).  What is result?  
 
 #### III) Writeup, wiki, blog, fastpages blog  
  * datasciY.com, create separate project pages for Amazon Rainforest Project  
  * geo-ml, rainforest-wiki, fill out for GitHub repo audience of coders  
  * fastpages blog -- create interactive notebooks, also link to run on colab and run on binder.  
  * plotly and dash -- interactive pages on my datasciY project page, blog page  
 
