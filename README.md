# Traffic-Sign-Detection-YOLOv4

In this project, deep neural network model will be trained to detect traffic signs. Model will predict the bounding box of the found object and will recognize the what is the object is



1) Download GTSDB FullIJCNN2013.zip
	from https://sid.erda.dk/public/archives/ff17dc924eba88d5d01a807357d6614c/published-archive.html 

2) Extract Dataset

3) Run Scripts/ppm2jpg.ipynb 
	this will convert images from ppm to jpg format.

4) Scripts\annotations.ipynb will convert Ground Truth(gt.txt) to yolo format. 
	They need to be same folder with images and same name but .txt format.

5) Scripts\names.ipynb will create a txt file which contains class names. (.names)

6) Scripts\filepaths.ipynb will create train.txt and test.txt file and split data into test and train. 
	These two files contains train and test images' paths.

7) Configure .data file.
	classes=<number-of-class>
	train=<Paths-to-train.txt>
	valid=<paths-to-test.txt>
	names=<paths-to-class.names>
	backup=<paths-to-where-to save-model>

8.) Execute train.ipynb 
	If you execute the code that start with [!./darknet detector -map train] then you will start a training.
		!./darknet detector -map train "path-to-.data" "path-to-.cfg" "path-to-.weights" -dont_show -points 0
	If you execute the code that start with [!./darknet detector test] then you can execute a pretrained model to detect object.
		!./darknet detector test "path-to-.data" "path-to-.cfg" "path-to-trained.weights" -dont_show "images-you-want-to-predict.jpg"

9) naive folder created for 4 class configurations
   8Class folder created for 8 class configurations
   43Class folder created for 43 class configurations
   *** Images folders are empty. You can extract images accordingly which number of class you want to use ***

*** If you want to download pre-trained model for transfer learning ***
    Yolo v3 : https://pjreddie.com/media/files/darknet53.conv.74
    Yolo v4 : https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137

*** To use darknet, you need to extract following file***
    https://drive.google.com/file/d/1-5ZhSMMOGRYgKpKxwW8okMD7iLwFfnJT/view?usp=sharing

*** To try my trained models you can use following links***
    8 Class With aug Yolov3    : https://drive.google.com/file/d/1-7EFaD9T4xhWoz1lHcTyhL1__gy7RcO7/view?usp=sharing
    8 Class With aug Yolov4    : https://drive.google.com/file/d/1xxEw4qZFZaieR96hnByV9YPQ_d7xilPw/view?usp=sharing
    8 Class Without aug Yolov3 : https://drive.google.com/file/d/1vefvjDeCZuWrvWyl1HHW9IWGHeRx6jzg/view?usp=sharing
    8 Class Without aug Yolov4 : https://drive.google.com/file/d/1-05zLfiCmYVNF96cECj_tBj9GnlYa1LY/view?usp=sharing
    4 Class Yolov3             : https://drive.google.com/file/d/1--RiU5o15NtWqx8D3TPE5LOfHFox5r8b/view?usp=sharing
    4 Class Yolov4             : https://drive.google.com/file/d/1-2S6dDbyjF3CFIsaKaMjLR9XrjSHmgvP/view?usp=sharing


*** You need to adjust paths accordinly ***
