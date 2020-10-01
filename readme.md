# Online Exam Student Anti-Cheat Tool

In the age of a global pandemic the entire industry has shifted to a work from home enviornment. However Student Examintions taken online are still a tricky problem to solve as there are still a lot of loop holes for students to use while giving online exams or sitting for online lectures.
A smart new secure testing software is set 
Technology today has made learning easier for kids and students. Researching and reading the news has never been quicker and more convenient with the internet, laptop, and mobile devices. Connecting through the internet is just like bringing your own library with you. However, technology has also allowed many students to cheat without a second thought. Accessible information has made it easier for them to look for new ways to cheat.

The problem is so prevalent that many schools have resorted to reverting back to pen and paper exams, a costly process which also greatly increases necessary administration.

Banning technology in the classroom or in the exam setting is not the solution to this problem, especially when computers are heavily used in the classroom curriculum and in the workplace. Battling technology should be done with the use of similar technology.

Having exam or anti-cheating software installed in the school’s or company's computers will help by restricting the sites that students can access during examinations. The software restricts certain web pages and processes in the computer to ensure the examinees are focused on the task in hand – the tests. This also prevents possible cheating and sharing of test questions online, and can have numerous benefits to any company using online training and testing software.to combat cheating and change the way students tackle exam preparation for good.


![Demo of app](https://github.com/Zorrat/Student-Online-Exam-AntiCheat-Tool/blob/master/models/images/demo.gif)

The Student Anti-Cheat Tool helps reduce these problem by detecting students faces with face recognition for identification and 
Students onscreen time with cellphone cheating detection.



Note :- Cell phone Detection uses Yolo V4 for object detection and will impact performance.
 
Requirements :
Create a virtual conda enviornment.

    conda create --name StudentAntiCheatEnv --file requirements.txt
    conda activate StudentAntiCheatEnv
Usage:
1) Place Students Face photo with their names as "Firstname Lastname.jpg"  in the "Faces/"  folder in project diretory for face recognition and identification.

2) Place the model file in correct folder i.e.
models/yolo/yolov4.h5
https://drive.google.com/file/d/1RCD4x8rudipNBahxO6Tsk4VsmhbxrmBL/view?usp=sharing

3) Press 'Q' during rendering to abort.

![Help](https://github.com/Zorrat/Student-Online-Exam-AntiCheat-Tool/blob/master/models/images/Capture.PNG)


4) Similar Usage for webcamDemo.py. This will render your webcam feed live with object detection and face detection for testing.
```
    python StudentAntiCheat.py --path "TestVideo.mp4" --name "FirstName LastName" --fps 12 --phone true --save --verbose
 ```       

   
Output:
![Output](https://github.com/Zorrat/Student-Online-Exam-AntiCheat-Tool/blob/master/models/images/verbose-final-output.PNG)



*Requires Cuda and CuDNN along with Tensorflow GPU Else CPU inference for phone detection will be extreemely slow*
```
TensorFlow version: 2.1.0
Eager execution: True
Keras version: 2.2.4-tf
Cuda version: 10.1
Cudnn version: 7.6
Num Physical GPUs Available:  1
Num Logical GPUs Available:  1
```

Note: Depending on certain Windows machines the face_recogntion library may not install correctly.

```
pip install cmake
pip install dlib
pip install face_recognition
```
If still having issue you have to build dlib with cmake.

Refrences :
YoloV4 Tensorflow by 
https://github.com/RobotEdh/Yolov-4
