# Earth Data Science Portfolio: Urban Greenspace

## Overview
In this project, we will split the green space (NDVI) data by census tract, as this matches the human health data from the CDC. If we were interested in the average NDVI at this spatial scale, we could easily use a source of multispectral data, such as Landsat (30 m) or MODIS (250 m), without significantly impacting our results. However, because we need to know more about the structure of green space within each tract, we need higher-resolution data. For that, we will access the National Agricultural Imagery Program (NAIP) data, which is taken for the continental US every few years at 1m resolution. That’s enough to see individual trees and cars! The main purpose of the NAIP data, as the name suggests, is agriculture. However, it’s also a great source for urban areas where lots is happening on a very small scale.

The NAIP data for the City of Chicago occupies about 20 GB of space. This amount of data is likely to crash your kernel if you try to load it all in at once. It would also be inconvenient to store on your hard drive, so that you can load it in bits at a time for analysis. Even if you are using a computer that can handle this amount of data, imagine analyzing the entire United States over multiple years!

To help with this problem, you will use cloud-based tools to calculate your statistics instead of downloading rasters to your computer or container. You can crop the data entirely in the cloud, thereby saving on your memory and internet connection, using rioxarray.


