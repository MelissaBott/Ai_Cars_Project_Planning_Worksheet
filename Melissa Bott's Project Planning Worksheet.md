**Project Planning Worksheet**

To pass this course, you'll need to create a project that matches this criteria:   
*"Based on your understanding of the material, you're required to build and submit an open-source project that uses NVIDIA Jetson and incorporates elements of AI (machine learning or deep learning) with GPU acceleration, along with a video demonstrating the project in action. For example, you could collect your own dataset and train a new DNN model for a specific application, add a new autonomous mode to JetBot, or create a smart home / IoT device using AI \- these need not be limited only to topics covered in the course. For inspiration, see the [Jetson Community Projects](https://developer.nvidia.com/embedded/community/jetson-projects) page \- the possibilities are endless\!"*

To pass the certification, your project will be reviewed based on the following criteria:

* **AI** \- The project uses deep learning, machine learning, and/or computer vision in a meaningful way and demonstrates a fundamental understanding of creating applications with AI. Factors include the effectiveness, technical complexity, and performance of your AI solution on Jetson.  
* **Impact / Originality** \- The concept of your project is novel and applies AI to solve or address challenges or issues faced by yourself or society. Also, our ideas and work are either original or derivative in a significant way.  
* **Reproducibility**\- Any plans, code, and resources needed for someone else to build and use the project are included in the repository and are easy to follow.  
* **Presentation and Documentation** \- The video effectively demonstrates and explains various aspects of the project, and there exists a clear, complete README in the repository that documents any steps needed to build/run the project, along with diagrams and images. 

Follow these steps to plan out your project

## **Part One: Brainstorming**

Write down 3-5 ideas for problems that you see in the world around you that you could create an AI to help solve. You can use [student example projects](https://docs.google.com/document/d/1qbBLDkW3-SwLu7tWY\_Q1qZnuGC5miO8y-oHWKxU4\_10/edit?usp=sharing) or [community example projects](https://developer.nvidia.com/embedded/community/jetson-projects) for inspiration or look back on past lessons that you enjoyed. 

1. Door detector, an ai that makes sure you closed your door all the way  
2. Detects different items if you have a messy table    
3. Clean table detector, detects how clean your table is  
      
4. Have a messy table and don’t know where to find anything   
5. Traffic detection, detects how many cars there are in a light intersection   
6. Pose detection for the 2024 Gymnastic Olympic 

## **Part Two: Details**

Write down the answers to these questions for your **two** **favorite** ideas:

**AI**: How would the AI work? Technically speaking what kind of network is it and how does this network work? 

Idea 1: Door detector, an ai that makes sure you closed your door all the way. I would use an object detection ( DetectNet) network for this ai. The network works by detecting an image or a frame from a video (the door) and classifies the object( its position). 

Idea 2: Traffic detection, detects how many cars there are in a light intersection. I would use an object detection ( DetectNet) network for this ai. The network works by detecting images or frames per second of an object and classifying it. 

**Impact**: What impact would this project have? Who does it impact and in what ways? 

Idea 1: What if you were in a rush and didn’t know if you closed your door all the way or what if it’s night time and you wanted to double check if the front door of your house is closed for good measures? The Door Detector would be an efficient way to help in those situations because it checks to see if you closed your door all the way or not.  

Idea 2: So basically, people hate sitting in traffic. Ai (adjustable traffic signal timing)  vs traffic signal controller (predesigned set timer) : ai would win because it would be more efficient to reckon that there could be different amounts of people on the roads everyday.

## **Part Three: Resources**

Now that you have thought out the impact and technical aspects of how the AI will work, it is time to map out what resources are going to be needed to complete your project. 

**Docs from jetson-inference**: Add your documentation or tutorial link below

[Jetson AI Fundamentals \- S3E4 \- Object Detection Inference (youtube.com)](https://www.youtube.com/watch?v=obt60r8ZeB0\&list=PL5B692fm6--uQRRDTPsJDp4o0xbzkoyf8\&index=13) \- video demo

**Example code:** Add your example code below

https://github.com/dusty-nv/jetson-inference/blob/master/python/examples/detectnet.py = detectnet.py code
https://github.com/dusty-nv/jetson-inference/blob/master/docker/run.sh = run.sh code

**Datasets**: If applicable, add the dataset that you will be using below

(I just got a picture's link from the internet)

**Miscellaneous**: Add any other resources you might need for your project below. 

- pictures of cars, copy image link and use wget to upload into the terminal 

## **Part Four: Documentation**

**Video**: Write down any key points that you want to add into your video below

*  Hook, intro, problem: With this ai your drive to work no longer includes rigid programmed traffic lights but instead traffic flows smoothly from adapting by the amount of cars there are in real time. 

*  How the ai works: Powered from a NVIDIA Jetson Nano. Their inference library is from an object detection ( DetectNet) network for this ai. The network works by detecting an image or a frame from a video. 

*  How this can be used in other places: This adaptable ai can not only be used on roads but also in detecting other things too like people so it can optimize the sidewalks as well. 

*  Video demo

**Documentation**: Write down any key points that you want to make sure are in your readme doc. 

*  Basic summary of what this technology does: Ai that detects and optimizes the flow of traffic by analyzing cars to help with traffic data. 

*  Set up: have VS code installed, go to github and copy the link (should be the green code button) and type in the terminal git clone \<repository\_url\>. Then cd into the repository name, etc…

*  How to run the project: to execute the ai, paste in your terminal ./detectnet.py \--network=ssd-inception-v2 input.jpg output.jpg   
  You can then check out your video from whatever you have named the output.jpg  
    
*  Possibly other resources: 

**Reproducibility**: How could your project be reproduced or run on another machine. Make sure to remember all steps that make your project work. 

1.  download the Jetson Inference Library to VS Code (if you're taking the NVIDIA Ai Machine Learning camp then you already have it so you don't need to do this step)

2. cd jetson-inference 
      
3. docker/run.sh 
      
4.  cd build/aarch64/bin/images

5.  wget (image link of cars on a highway or intersection)

6.  cd ..

7.  ./detectnet "images/name of image" images/test/new name.jpg

8.  pull up the new image (you can do it from the side panel, should be under jetson-inference/build/aarch64/bin/image/test

[Jetson AI Fundamentals \- S3E4 \- Object Detection Inference (youtube.com)](https://www.youtube.com/watch?v=obt60r8ZeB0\&list=PL5B692fm6--uQRRDTPsJDp4o0xbzkoyf8\&index=13) \- also a video demo 

