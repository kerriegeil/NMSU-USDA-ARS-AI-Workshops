---
permalink: /setup/

classes: wide

---


# Before you Come: Computer Setup

Before the workshop, each participant needs to work through the following instructions to ensure their computer is set up to successfully run the workshop materials. **Choose which set of instructions to follow based on the operating system of the computer you will be using for the workshop.**

Please note, the workshop helpers (Suzy Stillman and Kerrie Geil) do not have a Mac to test these setup instructions, but hopefully the setup won't be much different from the Windows instructions.

## Contents 

[For Mac Machines](#for-mac-machines)

[For Windows Machines](#for-windows-machines)

[On the Ceres HPC](#on-the-ceres-hpc)


## For Mac Machines

**Please try to troubeshoot installation on your own or with assistance from local IT or other local ARS staff**  

**1) Install Anaconda**

  If you don't already have Anaconda installed, follow the instructions for downloading and installing it (for an individual) at [https://docs.anaconda.com/anaconda/install/mac-os/](https://docs.anaconda.com/anaconda/install/mac-os/).
  
  If you do not have administrative privileges on your machine then you may have to ask your local IT for assistance installing it. If you do not have local IT assistance, then you can use either the Ceres HPC (if you have an account) or a personal computer.
  
  **2-3) Follow the instructions as best you can under "For Windows Machines"**

    

## For Windows Machines

**Please try to troubeshoot installation on your own or with assistance from local IT or other local ARS staff**  

**1) Install Anaconda**

  If you don't already have Anaconda installed, follow the instructions for downloading and installing it (for an individual) at [https://docs.anaconda.com/anaconda/install/windows/](https://docs.anaconda.com/anaconda/install/windows/).
  
  If you do not have administrative privileges on your machine then you may have to ask your local IT for assistance installing it. If you do not have local IT assistance, then you can use either the Ceres HPC (if you have an account) or a personal computer.
    
**2) Build the workshop Conda environment**

  From the Windows search bar type "anaconda" and select the Anaconda Powershell Prompt. At the prompt:
  
  ```
  conda create --name aiworkshop python=3.7 numpy pandas scipy imageio scikit-learn scikit-image matplotlib hdf5 nodejs jupyterlab -y
  conda activate aiworkshop
  conda install keras -y
  python -m ipykernel install --user --name aiworkshop
  ```
    
  The create and install steps of the build may take a while. The total build could take up to 10 minutes or possibly longer. 
    
  When the build finishes, navigate using the Anaconda Prompt to the folder you want JupyterLab to open in (for example create a workshop folder and cd into it) and open JupyterLab:
  
  ```
  mkdir NMSU-ARS-aiworkshop
  cd NMSU-ARS-aiworkshop/
  jupyter lab
  ```
        
**3) Run a test Jupyter Notebook and screenshot your results**

  - launch a new notebook in JupyterLab: File > New > Notebook
  - make sure the workshop kernel is selected: Kernel > Change Kernel > select aiworkshop from the drop down menu     
  - in the notebook's empty cell paste this: 
  
  from keras.models import Sequential<br>
  print(keras.backend.backend())
  
  - run the cell: click Run > Run All Cells or with your cursor inside the cell type Shift+Enter. The result should tell you you're using TensorFlow backend.
  - position the scroll bar so all results can be seen on your screen and then take a screenshot
  - paste the screenshot in an email to Kerrie Geil, kerrie dot geil at usda dot gov



## On the Ceres HPC

**Please try to troubeshoot installation on your own or contact HPC support at scinet_vrsc@usda.gov**  


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

**3) Build the workshop Conda environment**
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
  
  The build may take a while- up to 10 minutes or possibly longer. When the build finishes:
  ```
  conda activate /project/your_project_name/envs/aiworkshop
  ```
  
**4) Run a test Jupyter Notebook and screen shot your results**

  - launch a new notebook in JupyterLab: File > New > Notebook
  - make sure the workshop kernel is selected: Kernel > Change Kernel > select aiworkshop from the drop down menu 
  - in the notebook's empty cell paste this: 
  
  from keras.models import Sequential<br>
  print(keras.backend.backend())
    
  - run the cell: click Run > Run All Cells or with your cursor inside the cell type Shift+Enter. The result should tell you you're using TensorFlow backend.
  - position the scroll bar so all results can be seen on your screen and then take a screenshot
  - paste the screenshot in an email to Kerrie Geil, kerrie dot geil at usda dot gov 

