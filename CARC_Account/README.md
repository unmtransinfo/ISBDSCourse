
__Independent Study in Biomedical Data Science (ISBDS)__

# (I) How to setup your account for computations on Center for Advanced Research and Computing (CARC) at UNM? 

* Step 1: Go to [UNM CARC - Request and account](https://carc.unm.edu/new-users/request-an-account1.html) link and accept CARC User Agreement
* Step 2: If you have previously had an account on CARC, select the first option otherwise enter information as a new person and click Next 

  <img src="step2.png" width="500">

* Step 3: Select following options as shown in image below
  * Category: Project accounts are for classes and workshops
  * Order by: PI 
  * Click Refresh List
  * Then click on Project ID 2016213 for Independent Study in Biomedical Data Science (ISBDS) course with Jeremy Yang as PI 

  <img src="step3.png" width="500">

* Step 4: Select Wheeler and Xena clusters and hit Submit as shown below

  <img src="step4.png" width="500">

* Step 5: Upon approval of your account, you will receive an email with instructions to obtain your passwords for both the clusters

# (II) After you have obtained your passwords for the two clusters

* Step 1: Open Terminal (command line) on your local machine (laptop/desktop)
* Step 2: Type the following command and hit enter 
```
ssh yourusername@wheeler.alliance.unm.edu
``` 
   Enter the password provided by the CARC admin. You shall see a welcome message. 
  
   <img src="afterstep2.png" width="500">  
  
 * Step 3: Since this may be the first time you are logging in, you need to change your password to something different from CARC admin's password. Use following command to change your password
```
passwd
``` 
 * Step 4: Follow steps 2-3 on Xena cluster by replacing 'wheeler' with 'xena' in the `ssh` command in step 2

# (III) Some useful commands on Terminal on local machine 

Sl. No. | Commands | Actions
------------ | ------------- | ------------
1 | `ls`|  Get list of files 
2 | `qstat` | Check current users 
3 | `qgrok` | Check available/busy nodes 
4 | `mkdir foldername` | Create a new folder 
5 | `cd foldername` | Access a folder
6 | `cd ..` or `cd ~` | Go to home directory 
7 | `cd .` | Go back one step towards home directory
8 | `nano filename` | Open a file to edit 
9 | `Ctrl X` | Exit the editing environment 
10 | `exit` | Exit the ssh server  
11 | `Python` | Open python environment 
12 | `python filename.py` | Run a Python file 
13 | `R` | Open R environment 
14 | `module avail` | List of available modules on the cluster
14 | `module list` | List of available modules for you to use 
16 | `history` | Access previously executed commands 
17 | `qsub -I` | Access a node interactively
18 | `qsub PBSscript.sh` | Run a PBS script

# (IV) How to access servers via JupyterHub? 

* Step 1: Go to [Xena Cluster JupyterHub](https://xena.alliance.unm.edu:8000/hub/login) link, enter your username and password and sign in  
  
  Alternatively, you can go to [Wheeler Cluster JupyterHub](https://wheeler.alliance.unm.edu:8000/hub/login) as well 
  
  Select required server option

  <img src="jhubstep1.png" width="500"> 
  <img src="jhubstep1a.png" width="500">
  
* Step 2: Under New tab you can open a new Notebook in Python 3 environment

  <img src="jhubstep2a.png" width="500"> 
  
* Step 3: You can access the terminal from JupyterHub as shown below

  <img src="jhubstep3.png" width="500"> 
  
# (V) Some useful commands on Terminal via JupyterHub 
  Most of the commands from section (III) will work here as well 
 
Sl. No. | Commands | Actions
------------ | ------------- | ------------
1 | `conda create -n mypythonenv ipykernel`|  Create a new Python environment  
2 | `conda create -n myRenv r r-irkernel` | Create a new R environment 
3 | `conda info --envs` | List available environments 
4 | `conda activate myenv` | Activate the environment 
5 | `source activate myenv` | Activate the environment 
6 | `conda deactivate` | Deactivate the environment 
7 | `source deactivate` | Deactivate the environment 
8 | `pip3 install packagename` | Install package via Python3*
9 | `pip install packagename` | Install package via Python*
10 | `conda install packagename` | Install package via Conda*
11 | `conda install -c conda-forge packagename` | Install package via Conda* 
12 | `emacs filename` | Open a file to edit 
13 | `Ctrl Z` | Exit the editing environment  
14 | `python filename.py` | Run a Python file 
15 | `python` | Open python environment 
16 | `module avail` | List of available modules on the cluster
17 | `module list` | List of available modules for you to use 
18 | `conda list` | List of available packages in the environment
19 | `history` | Access previously executed commands 
20 | `qsub -I` | Access a node interactively
21 | `ls`|  Get list of files 
22 | `qstat` | Check current users 
23 | `conda install -n mypyenv nameofpackage nameofpackage` | Install packages without activating the environment 

[*] environment needs to be active in which the packages are required
