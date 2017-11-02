# Black.ai Computer Vision Technical Challenge
The purpose of this challenge is to test your ability and chosen approach in dealing with a computer vision problem. 

## Introduction
You are tasked with developing an algorithm to refine object detections from partially segmented image data.   

## The task

1. Download the sample input data from [here](https://s3-ap-southeast-2.amazonaws.com/public.data.black.ai/cv_challenge_dataset.zip) or using the cli:

    wget -t 15 https://s3-ap-southeast-2.amazonaws.com/public.data.black.ai/cv_challenge_dataset.zip

    The dataset contains a series of the following:
    1. A depth image with a scene containing people. 
    2. A label mapping for this image. The Mapping represents regions containing people as:
        
        * 0 = furniture
        * 1 = floor
        * 2 = walls/ceiling
        * 3 = female
        * 4 = male
    
2. Using any language or collection of libraries you wish, write a short program that for each depth image:
    * Loads the input data 
    * Applies the relevant label mask to the depth image;
    * segments the masked depth image;
    * Handles occlusion in the label mask; and 
    * Outputs the number of unique people in each of the given input images.
    * Outputs the time taken to process this image in miliseconds. 

    You can go about this in any way you wish, though your implementation should be robust to the following scenarios:

#### Scenario 1: Separate clearly defined people
![separete clearly defined people](https://s3-ap-southeast-2.amazonaws.com/public.data.black.ai/separate_people_labelled.png)

#### Scenario 2: Occlusion; Overlapping people
![separete clearly defined people](https://s3-ap-southeast-2.amazonaws.com/public.data.black.ai/overlapping_people_labelled.png)

#### Scenario 3: Occlusion; Incomplete label mask
![separete clearly defined people](https://s3-ap-southeast-2.amazonaws.com/public.data.black.ai/occluded_junk_labelled.png)

#### Scenario 4: Erranous labelling artifacts.
ie. noise whereby labels encapsulate impossibly small regions. 

## Submission

Just upload your codebase to a public github repository and send us the link! 

Final submission should be made to contact@black.ai, with the subject line "CV_CHALLENGE | <your_name>"

*note:* please also include instructions for simple setup and testing, so that we can easily run your program against our own test data. Be sure to include a list of dependencies, if any are required, to simplify the installation process. 

## Evaluation
We are primarily looking to assess the accuracy of detection, detection speed, and the implementation itself. We will be testing/training both the implementation and model on a machine running 64-bit Ubuntu 16.04 LTS, with a quad-core CPU, and a Nvidia GTX 1080 graphics card.  

## Bonus
Alongside the number of unique individuals in any given input image, report any additional information you can think of for each person. 

## Happy hacking! 
