# My notes

### 5/30/2021 Sunday

Image loading into list worked.  
To show inline, need to first open the image using PIL Image. 
Matplotlib pyplot format, shows images in row.  
Figure out how to do it, but I think "batching" images is just a list of file objects, or file path names.  

 * Next, review fastai batching, how did they get images into "DataBlock" and "DataLoader"?  


#### fastai v3 lesson3 nb: 
```python
src is a list, readin from file in path.
src = (ImageItemList.from_csv(path, 'train_v2.csv', folder='train-jpg', suffix='.jpg')
       .random_split_by_pct(0.2)
       .label_from_df(sep=' '))

data = (src.transform(tfms, size=128)
        .databunch(num_workers=0).normalize(imagenet_stats))
show_batch still works, and show us the different labels separated by ;.

data.show_batch(rows=3, figsize=(12,9))

# data.show_batch() must be fastai function, data is src list, 
# has .databunch attribute.
# need to review code at fastai v2. 
```

#### fastai 04_data.external.ipynb  
  * Has sample of Planet-jpg data and tiny for faster interation.  Try this first   
  * Can also custom download any web images or folder path  
    ```function image_download() ```
    
#### untar_data(URLs.NAME)    
   ```untar_data(URLs.NAME) ```   
   where NAME is defined url address in data_external.ipynb. 
 * PLANET_SAMPLE: A sample of the planets dataset from the Kaggle competition Planet: Understanding the Amazon from Space.
 * PLANET_TINY: A tiny version of the planets dataset from the Kaggle competition Planet: Understanding the Amazon from Space for faster experimentation and prototyping. 
 * data source already exists in fastai datablock.  
 * data.external.ipynb  
 * Default destination is ~.fastai/data/ or ~./fastai/data/archive  
   ```def download_url(url, dest, ... chunk_size=1024)```
   Downloades compressed data file to local destination, unzips files, etc.   

#### Python Iterable, Collections class:
```python
class Collection(inherit):  
# Need special class methods -- init, len, get_item.    
    def __init__(self, passed variables)
    def __len__(self, passed object collection) 
    def __get_item__(self, ith iteration item)  
```    
    
