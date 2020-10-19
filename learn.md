---
permalink: /learn/
classes: wide
---

All tutorials available on this page were created by Dr. Laura Boucheron of the Klipsch School of Electrical and Computer Engineering at New Mexico State University.

This information is free; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.

This work is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

A copy of the GNU General Public License can be viewed/downloaded at [COPYING.txt](/COPYING.txt) or see <https://www.gnu.org/licenses/>.
<br><br>

# Workshop 1

## Day 1

Download the Jupyter Notebook and image data

**If working on a laptop** (right click the links to download)

[Tutorial1_Image_Processing_Essentials.ipynb](/tutorials/Tutorial1_Image_Processing_Essentials.ipynb)

[cameraman.png](/data_images/cameraman.png)

[peppers.png](/data_images/peppers.png)

save these items in your working directory


**If working on the ARS Ceres HPC**

navigate to your working directory, then:

```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial1_Image_Processing_Essentials.ipynb -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/cameraman.png -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/peppers.png
```


To see a static notebook with all the outputs/answers: [Tutorial1_Image_Processing_Essentials.html](/tutorials/Tutorial1_Image_Processing_Essentials_complete.html)

<!-- link to view a static ipynb with all the outputs shown-->



## Day 2

Download the Jupyter Notebook and image data

**If working on a laptop** 

[Tutorial2_Classical_Machine_Learning.ipynb](/tutorials/Tutorial2_Classical_Machine_Learning.ipynb) (right click the link to download)

[CalTech101 dataset 101_ObjectCategories.tar.gz](http://www.vision.caltech.edu/Image_Datasets/Caltech101/101_ObjectCategories.tar.gz) (126 MB; follow the link to download)

[CalTech101 dataset Annotations.tar](http://www.vision.caltech.edu/Image_Datasets/Caltech101/Annotations.tar) (13 MB; follow the link to download)

Move the compressed image data folders to your working directory and unzip. Unzip using a terminal (e.g. Windows PowerShell) with ```tar -xvfz filename```


**If working on the ARS Ceres HPC**

navigate to your working directory, then:

```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial2_Classical_Machine_Learning.ipynb
cp /project/shared_files/NMSU-AI-WORKSHOP/*.zip ./
unzip '*.zip'
```

Note: If you are following this tutorial after the workshop has ended and the NMSU-AI-WORKSHOP shared folder no longer exists, do the following:
- Download and untar the image data to your local machine with the laptop instructions above
- Zip both folders of data (on Windows: right click > Send to > Compressed (zipped) folder)
- Login to Ceres with JupyterHub and upload the zip files (the larger zip will take a few minutes). The upload button is on the JupyterLab navigation pane between the New Folder icon and the Refresh File List icon
- Move the files to your working directory on Ceres and ```unzip `*.zip'```

<!-- link to view a static ipynb with all the outputs shown-->


## Day 3

Download the Jupyter Notebook

**If working on a laptop** (right click the links to download)

[]()

[]()

[]()

save these items in your working directory


**If working on the ARS Ceres HPC**

navigate to your working directory, then:

<!--
```
curl -O https:// -O https:// -O https:
```
-->

<!-- link to view a static ipynb with all the outputs shown-->

