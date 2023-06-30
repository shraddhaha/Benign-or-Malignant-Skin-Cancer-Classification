# Benign or Malignant Skin Cancer Detector.
This project classifies images based on Benign Skin Cancer and Malignant Skin Cancer. In a world where many of us may worry about contracting new illnesses or our friends and family who may have those illnesses, this project serves as a great way to detect if someone may have Benign Skin Cancer or Malignant Skin Cancer. This project has real-life applications, as it can be an idea used in medical places of work and can be done from a safe distance.

## The Algorithm
The algorithm of sorting Benign and Malignant Skin Cancer works by first being trained by being shown a series of images that are Benign or Malignant. Through the resnet tool, AI learns certain features of Benign and Malignant Skin Cancer, like a series of patterns that the Benign Skin or Malignant photos would have. After the AI knows what images are Benign and Malignant skin, the AI is shown a new set of images, labels them Benign or Malignant from their pre-trained knowledge, and exports them to Benign and Malignant output folders. Only Benign and Malignant were the options for classifying the images, as determined by the categories defined in the labels.txt file in the project folder.
## Test Input and Output Images
INPUT IMAGE

![1](https://github.com/shraddhaha/Benign-or-Malignant-Skin-Cancer-Classification/assets/108448331/b8264c30-9d2f-47ec-a3a7-082d1b880c6c)


OUTPUT IMAGE

![2](https://github.com/shraddhaha/Benign-or-Malignant-Skin-Cancer-Classification/assets/108448331/9e33c05e-f7dd-465d-8b86-ae049ba65f81)

## Running this Project
1) Use Putty and SSH connection and change direcotories to the jetson-inference and run- `./docker/run.sh` inorder to run the docker container.
   
2) From inside the Docker container, change directories so you are in jetson-inference/python/training/classification
   
3) Ensure the Resnet18,labels.txt,Your Dataset is downloaded in the right directories.
4) Set the NET and DATASET variables
   	`NET=models/Skin1
   DATASET=data/Skin1`
5)Run the imagenet command to see how it operates on an image from the Skin1 folder.

   `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/Skin1/44.jpg Test12.jpg
`

6)Open VSCode to view the image output.

## View a Video Explanation Here
(https://youtu.be/1p5FmN4Tu4s)


