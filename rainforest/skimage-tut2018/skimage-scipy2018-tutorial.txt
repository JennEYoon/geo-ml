# Scikit-Image SciPy 2018 tutorial, Juan, Stephan, +1.  

Colorscale conversion is not 1/3 red, 1/3 green, 1/3 blue to grayscale. Need to apply a formula.  
Probably same happened to .jpg images, which is in cymk format, when converted from .tif original files.  
Color filters probabily useful for enhancing Planet Labs images.  

#### Planet Labs API tutorial from SciPy 2018.  
It shows how to download Planet data and show images in notebooks.  Also, it seems like the source .tif files are in blue, green, red, infared channel order.  Tutorial uses rasterio library to manipulate image files (UI is like numpy) and geojson.io website to create a geojson (url get specification file) based on UI polygon selection.  These would make it easier to use Planet Labs "basemap" application to download images.  Generally quite useful to know.  

***Hands-on Satellite Imagery Analysis | SciPy 2018 Tutorial | Sara Safavi***  
 * https://www.youtube.com/watch?v=txhjhjWqF7c  
 * github tutorial: https://github.com/planetlabs/notebooks/tree/master/jupyter-notebooks/data-api-tutorials  

