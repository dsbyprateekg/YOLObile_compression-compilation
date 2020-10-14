# Environment setup:
conda install -c conda-forge/label/cf202003 opencv
pip install matplotlib
pip install seaborn
pip install scikit-learn
conda install -c pytorch pytorch==1.3.1
conda install -c pytorch torchvision==0.4.2

# Download weights file and put inside the weights folder
Google Drive: [Google Drive Download](https://drive.google.com/drive/folders/1FcWdXcWc3vScV-guIrxWsWGhjQwPOEQW?usp=sharing)

# Run following script to download the coco datasets(18.8 GB) in root directory, if you want to test the MAP:
YOLObile/data/get_coco2014.sh

# Adjust the path in YOLObile\data\coco2017.data

# run following command to test:
	python test.py --img-size 320 --batch-size 64 --device 0 --cfg cfg/csdarknet53s-panet-spp.cfg --weights weights/best8x-514.pt --data data/coco2017.data
	
# In case of memory error lower the --batch-size

