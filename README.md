# Dataset-of-Contaniner-Termainal-
The deep learning is a key technology in future, because it helps us in our life, so we should use this technology in dangerous location, hard jobs, or hard weather such as ports. it can be done when we can recognition of items and read number, and characters (OCR) by deep learning.
![test-detect](https://user-images.githubusercontent.com/102228359/197005312-93805296-ad21-4456-975f-26183fc52af9.png)
 for do that we have 5 stages:
1. labels: this stage very important, because if the labeling is correct, we will get good dataset, and after labeling we need program for augmented dataset.
2. training: there many algorithms, and application for training, after my search, there is the YOLOv7 is good, open source, and easy. 
3. detected: this stage to run, and test dataset if the program can detection items or not. 
4. OCR (Optical character recognition): there are many algorithms for it, for me I am using tesseract.
5. save in database: after detection and recognition on container number we can save it on database.
-------------------------------------------------------------------------------------------------------------------
overview:
 the application read container number then take image in 4 cameras for save container status, then it will save container number in database TOS without enter data from clerk. 
we can use this application for entry gate, exit gate, and discharge from vessel that is easy, because we only need insert records for container number and plate license of truck, and the rest of the information from TOS system.
for running:
python detect.py --weights last.pt  --source rtsp://username:password@ip # for IP camera
python detect.py --weights last.pt  --source 0 # for laptop camera
python detect.py --weights last.pt  --source test.jpg # for image
python detect.py --weights last.pt  --source test.mp4 # for video

------------------------------------------------------------------------------------------------------------------
requirements:
1. this application needs four cameras install in truck path for detect container and container number.
2. deep learning programs need NVIDIA GPU , because NVIDIA working with CUDA in PyTorch (NVIDIA Tesla V100, GeForce RTX 2080 Ti, NVIDIA Titan RTX).
---------------------------------------------------------------------------------------------------------------------
Issues:
I can’t run one application for all cameras , I only can run one application for one camera , that mean I need one server with GPU for every cameras , that is high cost.

-----------------------------------------------------------------------------------------------------------------------
future:
1. I will improve the application for loading to vessel there is more working for detect bay, row, and tier.
2.  improve application for detect if the container is good or damaged.
3. create GUI by django/python for display data with image of container or track to clerk for confirm data with permission for edit.

