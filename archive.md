---
permalink: /archive/
classes: wide
---

These workshops have been/will be repeated a number of times. The Learn page contains the most up-to-date version of workshop materials. This page contains older materials from previously taught workshops.
<br><br>

# Quick Links

[Workshop 1 - 10/19/2020, 10/21/2020, 10/23/2020](#workshop-1---10192020-10212020-10232020)
  - [Laptop Materials](#wkshp1-for-laptop-users-right-click-the-links-to-download-and-save-to-working-directory)
  - [HPC Materials](#wkshp1-for-ars-ceres-hpc-users)
  - [Zoom Recordings](#wkshp1-zoom-recordings)

[Workshop 2 - 10/26/2020, 10/28/2020](#workshop-2---10262020-10282020)
  - [Laptop Materials](#wkshp2-for-laptop-users-right-click-the-links-to-download-and-save-to-working-directory)
  - [HPC Materials](#wkshp2-for-ars-ceres-hpc-users)
  - [Zoom Recordings](#wkshp2-zoom-recordings)



# Workshop 1 - 10/19/2020, 10/21/2020, 10/23/2020

#### Wkshp1 for laptop users (right click the links to download and save to working directory)

Day 1 Workbook: [Tutorial1_Image_Processing_Essentials.ipynb](/tutorials/Tutorial1_Image_Processing_Essentials.ipynb)

Day 1 Data: [cameraman.png](/data_images/cameraman.png), [peppers.png](/data_images/peppers.png)

Day 1 static notebook with outputs/answers: [Tutorial1_Image_Processing_Essentials_complete.html](/tutorials/Tutorial1_Image_Processing_Essentials_complete.html)

Day 1 instructor ipynb with ad hoc cells added during instruction: [Tutorial1_Image_Processing_Essentials_Boucheron.ipynb](/tutorials/Tutorial1_Image_Processing_Essentials_Boucheron.ipynb)

Day 2 Workbook: [Tutorial2_Classical_Machine_Learning.ipynb](/tutorials/Tutorial2_Classical_Machine_Learning.ipynb) (right click the link to download)

Day 2 Data: [CalTech101 dataset 101_ObjectCategories.tar.gz](http://www.vision.caltech.edu/Image_Datasets/Caltech101/101_ObjectCategories.tar.gz) (126 MB; follow link to download), [CalTech101 dataset Annotations.tar](http://www.vision.caltech.edu/Image_Datasets/Caltech101/Annotations.tar) (13 MB; follow link to download)

(Move the compressed image data folders to your working directory and unzip. Unzip using a terminal (e.g. Windows PowerShell) with ```tar -xvf filename```)

Day 2 Slides: [Day2_Rules_ML_DL.pdf](/slides/Day2_Rules_ML_DL.pdf)

Day 2 static notebook with outputs/answers: [Tutorial2_Classical_Machine_Learning_complete.html](/tutorials/Tutorial2_Classical_Machine_Learning_complete.html)

Day 2 instructor ipynb with ad hoc cells added during instruction: [Tutorial2_Classical_Machine_Learning_Boucheron.html](/tutorials/Tutorial2_Classical_Machine_Learning_Boucheron.ipynb)

Day 3 Workbook: [Tutorial3_Deep_Learning_for_Images.ipynb](/tutorials/Tutorial3_Deep_Learning_for_Images.ipynb)

Day 3 Slides: [Day3_CNNs.pdf](/slides/Day3_CNNs.pdf), [Day3_CNN_Epic_Fails.pdf](/slides/Day3_CNN_Epic_Fails.pdf)

Day 3 static notebook with outputs/answers: [Tutorial3_Deep_Learning_for_Images_complete.html](/tutorials/Tutorial3_Deep_Learning_for_Images_complete.html)

Day 3 instructor ipynb with ad hoc cells added during instruction: [Tutorial3_Deep_Learning_for_Images_Boucheron.ipynb](/tutorials/Tutorial3_Deep_Learning_for_Images_Boucheron.ipynb)


#### Wkshp1 for ARS Ceres HPC users

Day1:
```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial1_Image_Processing_Essentials.ipynb -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/cameraman.png -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/peppers.png
```

Day2:
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

Day3:
```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial3_Deep_Learning_for_Images.ipynb
```

#### Wkshp1 Zoom Recordings

to be posted



# Workshop 2 - 10/26/2020, 10/28/2020

#### Wkshp2 for laptop users (right click the links to download and save to working directory)

Day 1 Workbook: [Tutorial4_Visualizing_and_Modifying_DL_Networks.ipynb](/tutorials/Tutorial4_Visualizing_and_Modifying_DL_Networks.ipynb)

Day 1 Data: [my_digits1_compressed.jpg](/data_images/my_digits1_compressed.jpg), [latest_256_0193.jpg](/data_images/latest_256_0193.jpg)

Day 1 static notebook with outputs/answers: [Tutorial4_Visualizing_and_Modifying_DL_Networks_complete.html](/tutorials/Tutorial4_Visualizing_and_Modifying_DL_Networks_complete.html)

Day 1 instructor ipynb with ad hoc cells added during instruction: [Tutorial4_Visualizing_and_Modifying_DL_Networks_Boucheron.ipynb](/tutorials/Tutorial4_Visualizing_and_Modifying_DL_Networks_Boucheron.ipynb)

Day 2 Workbook: [Tutorial5_Advanced_DL_Networks.ipynb](/tutorials/Tutorial5_Advanced_DL_Networks.ipynb)

Day 2 Data: [https://pjreddie.com/media/files/yolov3.weights](https://pjreddie.com/media/files/yolov3.weights) (236 MB), [https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2019/03/zebra.jpg](https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2019/03/zebra.jpg)

Day 2 static notebook with outputs/answers: [Tutorial5_Advanced_DL_Networks_complete.html](/tutorials/Tutorial5_Advanced_DL_Networks_complete.html)

Day 2 instructor ipynb with ad hoc cells added during instruction: [Tutorial5_Advanced_DL_Networks_complete.ipynb](/tutorials/Tutorial5_Advanced_DL_Networks_complete.ipynb)


#### Wkshp2 for ARS Ceres HPC users

Day 1:
```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial4_Visualizing_and_Modifying_DL_Networks.ipynb -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/my_digits1_compressed.jpg -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/data_images/latest_256_0193.jpg
```

Day 2:
```
curl -O https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/tutorials/Tutorial5_Advanced_DL_Networks.ipynb -O https://pjreddie.com/media/files/yolov3.weights -O https://3qeqpr26caki16dnhd19sv6by6v-wpengine.netdna-ssl.com/wp-content/uploads/2019/03/zebra.jpg
```

#### Wkshp2 Zoom Recordings

to be posted
