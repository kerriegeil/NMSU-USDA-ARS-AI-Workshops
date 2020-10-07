---
title: Before You Come: Computer Setup 
permalink: /setup/

classes: wide

---


Before the workshop, each participant need to work through the following instructions to ensure their computer is set up to successfully run the workshop materials. Choose which set of instructions to follow based on the operating system of the computer you will be using for the workshop.

## Contents 

[For Windows Machines](#for-windows-machines)

[On the Ceres HPC](#on-the-ceres-hpc)


## For Windows Machines

**1) Install Anaconda**

  Follow the instructions for downloading and installing Anaconda (for an individual) at [https://docs.anaconda.com/anaconda/install/windows/](https://docs.anaconda.com/anaconda/install/windows/).
    
**2) build the workshop Conda environment**

  From the Windows search bar type "anaconda" and select the Anaconda Powershell Prompt. At the prompt type:
  
  ```
  conda create --name aiworkshop python=3.7 numpy pandas scipy imageio ipykernel scikit-learn scikit-image matplotlib nodejs jupyterlab -y
  conda activate aiworkshop
  conda install keras -y
  ```
    
  Each step of the build will take a while. The total build may take 10 minutes or possibly longer. 
    
  When the build finishes, navigate to the folder you want JupyterLab to open in (for example create a workshop folder and cd into it) and open JupyterLab:
  
  ```
  mkdir NMSU-ARS-aiworkshop
  cd NMSU-ARS-aiworkshop/
  jupyter lab
  ```
  
  **If you get any errors contact Suzy Stillman and Kerrie Geil** at 
  
  sstillman dot jrn dot lter at gmail dot com and
   
  kerrie dot geil at usda dot gov.
        
**3) Run a test Jupyter Notebook and screenshot your results**

  - download the [test notebook][https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/aiworkshop.yml]
  ```
  wget https://
  ```
   - open the test notebook in JupyterLab using the file navigator on the left side of JupyterLab
   - select the workshop kernel: Kernel > Change Kernel > select aiworkshop from the drop down menu 
   - click Run > Run All Cells
   - position the scroll bar so all results can be seen on your screen and then take a screenshot
   - paste the screenshot in an email to Kerrie Geil
    



## On the Ceres HPC

**1) Request a project directory on Ceres if you don't already have one**

  You will need a project directory to successfully run the workshop materials due to the space limitations of Ceres home directories. If you already have a project directory, proceed to step 2- you can run the workshop materials from any existing project directory with approximately 20GB of free space.
  
  If you do not have a project directory yet, request one using the [project directory request form](https://scinet.usda.gov/support/request-storage). eAuth is required to access the form. If you do not have eAuth credentials (i.e. you don't have a USDA PIV or CAC card) you will need to ask your USDA sponsor to complete the project directory request for you. Do this quickly since the approval process can take a week or more. Make sure to state on the request form that you need the directory by 10/16 to participate in a SCINet training event.
  
  The other option is to ask the Virutal Research Support Core to temporarily increase your home directory quota from 5GB to 20GB. You can make this request by emailing scinet_vrsc@usda.gov. Make sure to tell them that the extra home directory space is needed to participate in a SCINet training event and define the time period for which you need the extra space.

**2) Log into the Ceres HPC using JupyterHub**
  - Go to [https://jupyterhub.scinet.usda.gov/](https://jupyterhub.scinet.usda.gov/)
  - Use your SCINet credentials to log in.
    - Username: firstname.lastname 
    - Verification Code: 6 digit time-sensitive code that comes from Google Authenticator
    - Password: your SCINet password
  - Enter the following info on the spawner page
    - Node Type: short
    - Number of Cores: 4
    - Job Duration: 02:00:00
    - Working Directory: /lustre/project/***your_project_name***
    - leave all other fields blank

**3) build the workshop Conda environment**
  - open a terminal in JupyterLab with File > New > Terminal
  
  - navigate to your project directory
  ```
  cd /project/your_project_name
  ```
  
  - download the workshop yml file
  ```
  wget https://kerriegeil.github.io/NMSU-USDA-ARS-AI-Workshops/aiworkshop.yml
  ```
  
  - build the environment in your project directory
  ```
  source activate
  conda env create --prefix /project/your_project_name/envs/aiworkshop -f aiworkshop.yml
  ```
  
  The build will take a while- maybe 10 minutes or possibly longer. When the build finishes:
  ```
  conda activate /project/your_project_name/envs/aiworkshop
  ```
  
  **If you get any errors contact Kerrie Geil** at kerrie dot geil at usda dot gov.
  
**4) Run a test Jupyter Notebook and screen shot your results**
  - download the test notebook
  ```
  wget https://
  ```
  - open the test notebook in JupyterLab using the file navigator on the left side of JupyterLab
  - choose the workshop kernel 
    - click "Python 3" at the top right of the notebook
    - select "Python [conda env:aiworkshop]" from the dropdown list and click Select
  - click Run > Run All Cells
  - position the scroll bar so all results can be seen on your screen and then take a screenshot
  - paste the screenshot in an email to Kerrie Geil

