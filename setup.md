---
permalink: /setup/

classes: wide

---


# Before you Come: Computer Setup

Before the workshop, each participant needs to work through the following instructions to ensure their computer is set up to successfully run the workshop materials. **Choose which set of instructions to follow based on the operating system of the computer you will be using for the workshop.**

Please note, the workshop team does not have a Mac to test these setup instructions, but previous participants with Macs were successful at software installation following steps 2 and 3 of the Windows instructions.

## Contents 

[For Mac Machines](#for-mac-machines)

[For Windows Machines](#for-windows-machines)

[On the Ceres HPC](#on-the-ceres-hpc)

[Troubleshooting Tips](#troubleshooting-tips)


## For Mac Machines

**Please try to troubeshoot installation on your own or with assistance from local IT or other local ARS staff for help. See the end of the Windows section for minimal troubleshooting tips**  

**1) Install Anaconda**

  If you don't already have Anaconda installed, follow the instructions for downloading and installing it (for an individual) at [https://docs.anaconda.com/anaconda/install/mac-os/](https://docs.anaconda.com/anaconda/install/mac-os/).
  
  If you do not have administrative privileges on your machine you may still be able to install to your computer's Desktop. Otherwise, ask your local IT for assistance installing it. If you do not have local IT assistance, then you can use either the Ceres HPC (if you have an account) or a personal computer.
  
  **2-3) Follow the instructions as best you can under "For Windows Machines"**

    

## For Windows Machines

**Please try to troubeshoot installation on your own or with assistance from local IT or other local ARS staff for help. See the end of this section for minimal troubleshooting tips**  

**1) Install Anaconda**

  If you don't already have Anaconda installed, follow the instructions for downloading and installing it (for an individual) at [https://docs.anaconda.com/anaconda/install/windows/](https://docs.anaconda.com/anaconda/install/windows/).
  
  If you do not have administrative privileges on your machine you may still be able to install to your computer's Desktop. Otherwise, ask your local IT for assistance installing it. If you do not have local IT assistance, then you can use either the Ceres HPC (if you have an account) or a personal computer.
    
**2) Build the workshop Conda environment**

  From the Windows search bar type "anaconda" and select the Anaconda Powershell Prompt. At the prompt:
  
  ```
  conda create --name aiworkshop python=3.8 numpy pandas scipy imageio scikit-learn scikit-image matplotlib hdf5 nodejs jupyterlab -y
  conda activate aiworkshop
  conda install keras -y
  python -m ipykernel install --user --name aiworkshop
  ```
    
  **See the troubleshooting section below if you get an error on the keras install step**
  
  The create and install steps of the build may take a while. The total build could take up to 10 minutes or possibly longer. 
    
  When the build finishes, navigate using the Anaconda Powershell Prompt to the folder you want JupyterLab to open in (for example create a workshop folder and cd into it) and open JupyterLab:
  
  ```
  mkdir NMSU-ARS-aiworkshop
  cd NMSU-ARS-aiworkshop/
  jupyter lab
  ```
        
**3) Run a test Jupyter Notebook and screenshot your results**

  - launch a new notebook in JupyterLab: File > New > Notebook
  - make sure the workshop kernel is selected: Kernel > Change Kernel > select aiworkshop from the drop down menu     
  - in the notebook's empty cell paste this: 
  
  import keras<br>
  print(keras.backend.backend())
  
  - run the cell: click Run > Run All Cells or with your cursor inside the cell type Shift+Enter. The result should tell you you're using TensorFlow backend.
  - position the scroll bar so all results can be seen on your screen and then take a screenshot
  - paste the screenshot in an email to Kerrie Geil, kerrie dot geil at usda dot gov

#### Troubleshooting Tips

Occasionally, a conda environment build will fail for no apparent reason (especially when keras is involved). Please attempt to build the workshop environment at least 3 times. Sometimes it takes up to 3 attempts, executing the exact same commands for the environment build to complete successfully (no idea why).

**If the install of python=3.8 numpy pandas scipy imageio scikit-learn scikit-image matplotlib hdf5 nodejs jupyterlab completed successfully but you get an error when trying to install keras:**
  - first try getting keras from the conda-forge channel: replace "conda install keras -y" with 
  ```
  conda install -c conda-forge keras -y
  ```
  - if that doesn't work, try using pip: replace "conda install keras -y" with 
  ``` 
  pip install keras
  pip install tensorflow
  ```

**If an error occurred during the conda environment build process and creation of the environment didn't complete successfully:**
  - check if part of the environment was created by typing in the Anaconda Powershell Prompt  
  ```
  conda env list
  ```
  
  - If you see 'aiworkshop' in the list delete it by typing
  ```
  conda env remove --name aiworkshop
  ```
  
   and start at the beginning of 'Step 2 Build the workshop Conda environment' again. Try this process at least 3 times before giving up.
  
  - If you don't see 'aiworkshop' in the list then you don't need to delete anything, just try step 2 of the installation again. Try this process at least 3 times before giving up.
  

**If your environment builds successfully but 'aiworkshop' doesn't appear as a kernel option in jupyter lab:**
  - first try relauching Jupyter Lab
    - in Jupyter Lab: File > Shut Down
    - in Anaconda Powershell Prompt: ```jupyter lab```
    - in Jupyter Lab: try selecting the kernel again
    
  - if that doesn't work shut down Jupyter Lab, delete the whole environment and start over. In the Anaconda Powershell Prompt type
  ```
  conda env remove --name aiworkshop
  ```

   and start over with 'Step 2 Build the workshop Conda environment' again. Try this process at least 3 times before giving up.



## On the Ceres HPC

**Please try to troubeshoot installation on your own or contact HPC support at scinet_vrsc@usda.gov**  


**1) Request a project directory on Ceres if you don't already have one or use /90daydata/scinet/yourname/**

  You will not be able to run the workshop materials in your HPC home directory due to the space limitations. If you already have a project directory, proceed to step 2- you can run the workshop materials from any existing project directory with approximately 20GB of free space.
  
  If you do not have a project directory yet, you can request one using the [project directory request form](https://scinet.usda.gov/support/request-storage). eAuth is required to access the form. If you do not have eAuth credentials (i.e. you don't have a USDA PIV or CAC card) you will need to ask your USDA sponsor to complete the project directory request for you. Do this quickly since the approval process can take a week or more. Make sure to state on the request form that you need the directory to participate in a SCINet training event and give them the workshop start date.
  
  The other option is to use the /90daydata/scinet/ folder. As the folder name suggests, files stored there are not permanent and will be deleted after 90 days. We suggest creating a new folder at /90daydata/scinet/yourname/, building the workshop conda environment there, and also running the workshop jupyter notebooks from that location as well. To do this you would modify the instructions below by substituting /90daydata/scinet/yourname/ wherever you see /project/your_project_name/. 

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
    - Working Directory: /lustre/project/your_project_name ***or*** /90daydata/scinet 
    - leave all other fields blank

**3) Build the workshop Conda environment**

  If using /90daydata/scinet, create a new folder there ```mkdir /90daydata/scinet/yourname```, then modify the instructions below by substituting /90daydata/scinet/yourname/ wherever you see /project/your_project_name/.
  
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
  
  import keras<br>
  print(keras.backend.backend())
    
  - run the cell: click Run > Run All Cells or with your cursor inside the cell type Shift+Enter. The result should tell you you're using TensorFlow backend.
  - position the scroll bar so all results can be seen on your screen and then take a screenshot
  - paste the screenshot in an email to Kerrie Geil, kerrie dot geil at usda dot gov 

