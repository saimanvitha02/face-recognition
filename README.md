# Face Recognition using OpenCV

Make sure that OpenCV is installed. 

pip install opencv-python

OpenCV already contains many pre-trained classifiers for face, eyes, smiles, etc. Face detection using Haar cascades is a machine learning based approach where a cascade function is trained with a set of input data. For this, download the haarcascade_frontalface_default.xml file from OpenCV's Github repository. 

# Face Recognition in Image:

1. OpenCV reads image in the sequence Blue Green Red (BGR). Thus, to view the actual image we need to convert the rendering to Red Green Blue (RGB). The method cvtColor allows us to convert the image rendering to a different color space.
2. OpenCV detection works only on grayscale images. Hence it is important to convert into grayscale. 
3. detectMultiScale function is used to detect the faces. It takes 3 arguments — the input image, scaleFactor and minNeighbours. scaleFactor specifies how much the image size is reduced with each scale. minNeighbours specifies how many neighbors each candidate rectangle should have to retain it.
4. faces contains a list of coordinates for the rectangular regions where faces were found. We use these coordinates to draw the rectangles in our image.

Here is the sample output:

![image](https://user-images.githubusercontent.com/63820567/123903207-e0323380-d98b-11eb-83bd-147600449813.png)

Image src: Google

# Face Recognition in Video:

1. An infinite loop is used to loop through each frame of the video and it is read using cap.read()
2. The first value returned is a flag that indicates if the frame was read correctly or not. We don’t need it. 
3. The second value returned is the still frame on which we will be performing the detection.

Here is the sample output:

![webcam_output](https://user-images.githubusercontent.com/63820567/123903256-fa6c1180-d98b-11eb-9578-561f0b593ff2.PNG)

Image Src: Webcam

