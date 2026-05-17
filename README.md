# P10_I-20251097-EC
Analysis tools for beamtime `I-20251097` EC at P10, Petra III, DESY. 

To download the repo:

```bash
$ git clone https://github.com/fperakis/P10_I-20251097-EC.git
```

### Maxwell cluster
Intructions to Maxwell cluster: 
https://wiki.desy.de/maxwell/documentation/access/

Connect to maxwell cluster with jupyter notebook:
https://max-jhub.desy.de.

To access the data, launch a terminal (from new launcher) and make link to P10 data from your home folder
```bash
ln -s /asap3/petra3/gpfs/p10/ link_to_p10
```
Path to current data 
```bash
/asap3/petra3/gpfs/p10/2026/data/11023455/
```

### Install Xana and setup a virtual environment
If you want to use Xana for the g2 calculation you can:
* Install Xana [https://github.com/reiserm/Xana] 
* Creates a new virtual environment that you can use from the jupyter notebooks
* installs all the requirements with the following commands:
  
```bash
# check python and pip
python3 --version         # check python version
python3 -m venv .venv     # make new virtual environment
source .venv/bin/activate # activate it
pip install --upgrade pip # upgrade pip

# install xana
pip install -r requirements.txt # install requirements for xana
git clone https://github.com/reiserm/Xana.git  
cd Xana
pip install -e .

# make kernel based on your environment
pip install --upgrade ipykernel
python -m ipykernel install --user --name p10-env
```



