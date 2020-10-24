# TrafficDemo
This is a software for practice of developing a system from completely scratch. Understanding this will help a lot in system development and basic structure of a system along with computer vision, GUI with python library Tkinter and basic opencv.
Go here if you don't have time.

Methodology
Vehicle Classification
From the given video footage, moving objects are detected. An object detection model YOLOv3 is used to classify those moving objects into respective classes. YOLOv3 is the third object detection algorithm in YOLO (You Only Look Once) family. It improved the accuracy with many tricks and is more capable of detecting objects. The classifier model is built with Darknet-53 architecture. Table-1 shows how the neural network architecture is designed.

Darknet Architecture

Violation detection
The vehicles are detected using YOLOv3 model. After detecting the vehicles, violation cases are checked. A traffic line is drawn over the road in the preview of the given video footage by the user. The line specifies that the traffic light is red. Violation happens if any vehicle crosses the traffic line in red state.

The detected objects have a green bounding box. If any vehicle passes the traffic light in red state, violation happens. After detecting violation, the bounding box around the vehicle becomes red.

Implementation
Computer Vision
OpenCV is an open source computer vision and machine learning software library which is used in this project for image processing purpose. Tensorflow is used for implementing the vehicle classifier with darknet-53.

Graphical User Interface (GUI)
The graphical user interface has all the options needed for the software. The software serves administration and other debugging purposes. We don’t need to edit code for any management. For example, if we need to open any video footage, we can do it with the Open item (Figure-2).

Figure 2

 Figure-2: Initial user interface view.
Primarily, for the start of the project usage, the administrator needs to open a video footage using ‘Open’ item that can be found under ‘File’ (Figure-2). The administrator can open any video footage from the storage files (Figure-3).

Figure 3

 Figure-3: Opening a video footage from storage.
After opening a video footage from storage, the system will get a preview of the footage. The preview contains a frame from the given video footage. The preview is used to identify roads and draw a traffic line over the road. The traffic line drawn by administrator will act as a traffic signal line. To enable the line drawing feature, we need to select ‘Region of interest’ item from the ‘Analyze’ option (Figure-4). After that administrator will need to select two points to draw a line that specifies traffic signal.

Figure 4

 Figure-4: Region of Interest (Drawing signal line)
Selecting the region of interest will start violation detection system. The coordinates of the line drawn will be shown on console (Figure-5). The violation detection system will start immediately after the line is drawn. At first the weights will be loaded. Then the system will detect objects and check for violations. The output will be shown frame by frame from the GUI (Figure-6).

Figure 5

 Figure-5: Line Coordinates (from console)
Figure 6

 Figure-6: Final Output (on each frame)
The system will show output until the last frame of the footage. In background a ‘output.mp4’ will be generated. The file will be in ‘output’ folder of ‘Resources’. The process will be immediately terminated by clicking ‘q’.

After processing a video footage, the administrator can add another video footage from the initial file manager (Figure-2). If the work is complete the administrator can quit using ‘Exit’ item from File option.

Libraries used for graphical user interface:

Tkinter
Contributing
The main reason to publish something open source, is that anyone can just jump in and start contributing to my project. So If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

Links and References
Project homepage: https://github.com/anmspro/Traffic-Signal-Violation-Detection-System
Repository: https://github.com/anmspro/Traffic-Signal-Violation-Detection-System.git
Issue tracker: https://github.com/anmspro/Traffic-Signal-Violation-Detection-System/issues
G. Ou, Y. Gao and Y. Liu, "Real TimeVehicularTrafficViolationDetectioninTrafficMonitorin gStream," in 2012 IEEE/WIC/ACM , Beijing, China , 2012.
X. Wang, L.-M. Meng, B. Zhang, J. Lu and K.-L.Du, "A Video-based Traffic Violation Detection System," in MEC, Shenyang, China, 2013.
Joseph Redmon and Ali Farhadi, "YOLOv3: An Incremental Improvement".
https://machinelearningmastery.com/how-to-perform-object-detection-with-yolov3-in-keras
In case of any help you may need from me, please contact abunomanmd.sakib@gmail.com directly without any hesitation! I will be glad to help you.
Author
Abu Noman Md. Sakib, Pias Roy
abunomanmd.sakib@gmail.com
pias.kuet@gmail.com
Student at Department of Computer Science and Engineering
Khulna University of Engineering & Technology, Khulna
Bangladesh

Supervised under
Mahmudul Hasan Shauqi
mahmudulhasanshauqi@gmail.com
Lecturer
Dept. of Computer Science and Engineering
Khulna University of Engineering & Technology

Licensing
The code in this project is licensed under GNU GPLv3 license.

Stargazers over time
Stargazers over time
