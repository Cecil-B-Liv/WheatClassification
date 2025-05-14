conda create --name tf python=3.9
conda activate tf
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
python.exe -m pip install --upgrade pip
pip install tensorflow==2.10
pip install numpy==1.26.4
conda install anaconda::jupyter
conda install -c conda-forge charset-normalizer
