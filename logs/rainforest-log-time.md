Create rainforest-log-time.md
# Timeline of Rainforest project  

#### 8/2 - 8/6, 50hrs - finally get data loader to work, runs model  
 * resnet34, sample 2000 jpg data, not all 40,000.  
 * brighten 20%, resize to 224 pixels, maybe due to pre-trained model's image size?  
 * flip=true augmentation. 
 * 20% split into validation set, random selection from 2000 input images, seed set to 42.  
 * **Result: fbeta_score 0.923.  Top 0.93x**  
 * to run more tests.  improve source image quality, simplify categories down to 5 or 6 from 17, try different models and freeze and re-training.  
 * -- But first, test current model more --  
 * Test first, predict on known unused jpg images with labels.  
 * Test saved model, see if loading works.  
 * Test on all 40000 images. 
 * Try k-fold cross-validation instead of random splits, run model several times with controlled split, then average model parameters.  

#### 8/10/21 Tuesday -- Presented to Meetup
