# yolov7_pose

# New Features
 - Added Support for Comparision of (FPS & Time) Graph
 - How to run Code in Google Colab
 - Code can run on Both (CPU & GPU)
 - Video/WebCam/External Camera/IP Stream Supported

# Coming Soon
Development of streamlit dashboard for Pose-Estimation

# Steps to run Code
 - If you are using google colab then you will first need to mount the drive with mentioned command first, (Windows or Linux users) both can skip this step.
'''from google.colab import drive
drive.mount("/content/drive")'''
Clone the repository.
git clone https://github.com/RizwanMunawar/yolov7-pose-estimation.git
Goto the cloned folder.
cd yolov7-pose-estimation
Create a virtual envirnoment (Recommended, If you dont want to disturb python packages)
### For Linux Users
python3 -m venv psestenv
source psestenv/bin/activate

### For Window Users
python3 -m venv psestenv
cd psestenv
cd Scripts
activate
cd ..
cd ..
Upgrade pip with mentioned command below.
pip install --upgrade pip
Install requirements with mentioned command below.
pip install -r requirements.txt
Download yolov7 pose estimation weights from link and move them to the working directory {yolov7-pose-estimation}

Run the code with mentioned command below.

python pose-estimate.py

#if you want to change source file
python pose-estimate.py --source "your custom video.mp4"

#For CPU
python pose-estimate.py --source "your custom video.mp4" --device cpu

#For GPU
python pose-estimate.py --source "your custom video.mp4" --device 0

#For View-Image
python pose-estimate.py --source "your custom video.mp4" --device 0 --view-img

#For LiveStream (Ip Stream URL Format i.e "rtsp://username:pass@ipaddress:portno/video/video.amp")
python pose-estimate.py --source "your IP Camera Stream URL" --device 0 --view-img

#For WebCam
python pose-estimate.py --source 0 --view-img

#For External Camera
python pose-estimate.py --source 1 --view-img
Output file will be created in the working directory with name ["your-file-name-without-extension"+"_keypoint.mp4"]
