# Nanovea_Sur
Nanovea profilometer - plotting SUR file data

This is an attempt to plot SUR data from Nanovea products.   The software for Nanovea comes with a dongle (software key) so it is sometimes inconvenient for multiple users.    

Step 1.   You have to have the Nanovea software key to export your data into X,Y,Z format in CSV or TXT file(s).    This is in the Nanovea help files and documents.  This will depend on which studiable you are using, such as wheter
or not it was extracted, levels, or thresholds set.   So if you choose to export a raw and un-flattened image, that is what you will be working with.    This is therefore not idea, but I did not find any code for reading metrology *.sur failes
in Python, although they seem to exist in Matlab.

Step 2.   You need to know a little python.  Place your TXT files (they will possibly be quite large) in a directory where your python or Jupyter environment can find them.

Step 3.   Load and plot.    I am working with large samples so I included a step to load a photograph first, for reference.    My samples are 300mm long, so the scale is set to that, you will have to adjust this to your samples.    
          -- For my samples that are 300mm, this is the same a s3000 pixels, so I adjust accordingly by editing the photo I am using to fit the parameters.  Ifound that easier than changing the parameters.   However, if you use the same 
          size samples repeatedly, you should try adjusting the saettings accordingly if you want to use this feature.

Step 4.   Render the heatmap.   This is probably not ideal, but I can load a 350mb file in 90 seconds.   The X and  Y coordinates are set, and some python is needed to change some of the other settings.   This is optimized for missing
          data points.  If using the MATPLOTLIB version, you get a good image, but it hesitates and stalls quite a lot when it encounters empty data.  I have not found a perfect workaround for this.

step 5.   Render the heatmap (again) with sliders.    The Sliders will give you a profile along a line on the X or Y axis, so you can get a general roughness of the sample.
