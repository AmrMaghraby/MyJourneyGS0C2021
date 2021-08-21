## Welcome to My Blog

# Week 1

 Implemented Localization Network in STN (to be able to solve challenges like rotation challenge).

# Week 2 

 Implemented CNN (First Module) and connected it to SVM implemented by me also.
 
 Tried Different architectures and pre-trained CNN to see which one is more effective and getting higher accuracy.

# week 3 - 8

 From This week I started to ran about 21 Experiemnt till now to select the best one with best architecture. 
 
 Experiement 1:
  
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Fc3 --> ReLU --> Fc4 --> ReLU --> SVM
  
  This got Accuracy About ~= 65%
 
 Experiement 2:
 
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Fc4 --> ReLU --> Fc5 --> ReLU --> SVM
  
  This got Accuracy About ~= 65%
 
 Experiement 3:

  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Fc5 --> ReLU --> Fc6 --> ReLU --> SVM
  
  This got Accuracy About ~= 65%
 
 Experiement 4:
  
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> Fc6 --> ReLU --> Fc7 --> ReLU --> SVM
  
  This got Accuracy About ~= 70%
 
 Experiement 5:
  
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> pool --> Fc6 --> ReLU --> Fc7 --> ReLU --> SVM
  
  This got Accuracy About ~= 70%
  
 Experiement 6:
  
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> pool --> Fc6 --> ReLU --> Fc7 --> ReLU --> SVM
  
  This got Accuracy About ~= 75%
  
 Experiement 7:
  
  I have implemented  CNN with the following specs :
  Data --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> pool --> Fc6 --> ReLU --> Fc7 --> ReLU --> Fc8 --> SVM
  
  This got Accuracy About ~= 75%
  
 Experiement 8:
  
  I have implemented  CNN with the following specs :
  Data STN --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Fc4 --> ReLU --> SVM
  
  This got Accuracy About ~= 80%

 Experiement 9:
  
  I have implemented  CNN with the following specs :
  Data STN --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Fc5 --> ReLU --> SVM
  
  This got Accuracy About ~= 83.3%

 Experiement 10:
  
  I have implemented  CNN with the following specs :
  Data STN --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> Fc6 --> ReLU --> SVM
  
  This got Accuracy About ~= 87.6% 

 Experiement 11:
  
  I have implemented  CNN with the following specs :
  Data STN --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> Fc6 --> ReLU --> Fc7 --> ReLU --> SVM
  
  This got Accuracy About ~= 95.9% 
  
 Experiement 12:
  
  I have implemented  CNN with the following specs :
  Data STN --> Conv1 --> ReLU --> Pool1 --> Conv2 --> ReLU --> Conv3 --> ReLU --> Conv4 --> ReLU --> Conv5 --> ReLU --> Fc6 --> ReLU --> Fc7 --> ReLU --> Fc8 --> SVM
  
  This got Accuracy About ~= 98.9% 
  

# Week 9

 - Generated noise dataset to test our modle will it detect noise dataset as false or negative cuts.
 - Types of noise generated: Gaussian, Periodic, Salt and Pepper, Shot Noise, Film Grian.
 - Result of this experience: 
 - Gaussian Noise got accuracy ~ 60%
 - Periodic Noise got accuracy ~ 62%
 - Salt and Pepper got accuracy ~ 64%
 - Shot Noise got accuracy ~63%
 - Film Grain got accuracy ~61%
 
 
# Week 10
 
 - I have searched on the internet for statistical methods in order to make shot detection not based on machine learning but on image processing as OpenCV and 
   PyScene. I have found a good solution based on the histogram, generating a histogram for the current frame and forward frame and getting the difference between  
   them and then see if it passes a certain threshold then it is a new shot if not still the same shot.
  
 - Faced a challenge while making the statistical method, if in the movie suddenly we zoomed in and then zoomed out this will result in a huge difference in the
   produced histogram which will make at certain frame the difference between it and the next greater the threshold, and we will detect it is a different shot which    is not correct. 
  
 - Another challenge faced me when the video shows something and then suddenly someone passes or some children playing running through this scene. This will lead  
   to the previous issue that a histogram at a certain frame will produce a histogram that differs from the next one by a value that exceeds the threshold, which
   makes us classify a new shot while this is not true (false positive).
   
   
# Week 11
 
 -  I have searched how people used to use histograms, especially in tasks related to movies. I found some people recommending doing the previous solution but not 
    on the whole frame instead of on the four corners of the frame. I have also read that by convention in any task related to movies and video mos of the time, 
    people think about the corners. So, I believe we need to think about how to use histogram solutions on the corners, not the video content. 
 
 -  I have found also something good related to machine learning model image classification recommended by a friend called triplet loss. I have learned the basic 
    concepts and know how it works.
   
   
# Week 12
 
 - I have tested PyScene on color films datasets, and it worked well in case we defined a threshold to PyScene.
   
 - Without defining the threshold, results are not satisfying.
   
 - I am searching on the internet how to know the threshold that will fit each input, but till the moment I don't found anything useful. 
   
   
# Week 13
 
 -  My mentor Eng Ahmed Ismail contributed to me and found a good optimizer called baysean optimizer which could be integrated with PySene to detect best threshold.
   
   
# Week 14 
 
 - Building Singularity image and upload it to HPC.
   
 - A lot of problems happened as a result of library dependancy but at the end it is uploaded successfully.
   
   
# HOW TO RUN ON HPC OUR MODEL 

 - In case you want to run test file follow the following instructions:
 - Module load singularity
 - singularity run GSOC.img video_dir
 - For example: singularity run GSOC.img '/mnt/rds/redhen/gallina/home/aam193/GSOC2021_Detect_Video_Cuts/306-706.mp4'

# Future Work 

  1- Training Now we can train the model to get the best thrshold required by pyScene, but unfourtanley we didnot have time to test everything so as future work we      need to investigate more in it. In order to run the training pipeline follow the follwoing the steps below :
  - In case you want to run train file follow the follwoing instruction:
  - Module load singularity
  - singularity shell GSOC.img
  - source activate pyscene_env
  - python getOptimalThreshold.py 'path/to/directory/contain/mp4/files' 'path/to/directory/contains/csv/files/to/calculate/accuracy'
 
  2- Classify soft cuts and hard cuts in an efficient way baased on the output of pyScene.
