# P10_I-20251097-EC
Analysis tools for beamtime `I-20251097` EC at P10, Petra III, DESY. 

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

### Virtual environment
You can also create a new environment to install all the requirements with the following commands:
```bash
python3 --version # check that it's Python 3.11 - usually
python3 -m venv .venv
ls -a 
source .venv/bin/activate
pip install --upgrade pip
pip install -r 03-scripts/requirements.txt
git clone https://github.com/reiserm/Xana.git
cd Xana
pip install -e .
pip install --upgrade ipykernel
python -m ipykernel install --user --name p10-env
```



