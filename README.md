# Sign Language Symptom Detector App
> Real-time sign language detector app able to translate symptoms into text.
End to end project, from extracting the input data for training the model to production deployment.
> Live demo [_here_](https://signlanguagesymptoms.onrender.com/)

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Features](#features)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Usage](#usage)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)
<!-- * [License](#license) -->


## General Information

- How can we improve communication between deaf patients and healthcare professionals?
- As part of the final project for Le Wagon Data Science Bootcamp (Lisbon, Sep 22), together with 3 of my classmates we approached this question by building an end to end computer vision app able to predict sign language symptoms in real time. 
- By signing the symptoms via webcam, the deaf patient is able to communicate with the healthcare professionals in real time. This can be useful in emergency situations or when an interpreter is not readily available.  

## Project Pipeline and Technologies Used

1. Extract Datapoints: Collect the input data as coordinates from the movement of hands, face and body using Media Pipe Holistic and Open CV. Initially we extracted this coordinates from the [_WLASL_] (https://dxli94.github.io/WLASL/) videos dataset. However, when training the model with these datapoints we realized that there was high varience in the positions and close up of the signers of the videos. This resulted in the model having very low accuracy and not really learning from the data. So instead we recorded the signs ourselves, collecting over 12 million datapoints and storing them as numpy arrays. 

2. Train the model: a deep neural network GRU model using Keras and Tensorflow. This 
• Set to production using Javascript and deployed in Heroku.
Python
- Open CV 
- Media Pipe Holistic
- TensorFlow
- Keras
- Javascript
- PHP


## Features
List the ready features here:
- Awesome feature 1
- Awesome feature 2
- Awesome feature 3


## Screenshots
![Example screenshot](./img/screenshot.png)
<!-- If you have screenshots you'd like to share, include them here. -->


## Setup
What are the project requirements/dependencies? Where are they listed? A requirements.txt or a Pipfile.lock file perhaps? Where is it located?

Proceed to describe how to install / setup one's local environment / get started with the project.


## Usage
How does one go about using it?
Provide various use cases and code examples here.

`write-your-code-here`


## Project Status
Project is: _in progress_ / _complete_ / _no longer being worked on_. If you are no longer working on it, provide reasons why.


## Room for Improvement
Include areas you believe need improvement / could be improved. Also add TODOs for future development.

Room for improvement:
- Improvement to be done 1
- Improvement to be done 2

To do:
- Feature to be added 1
- Feature to be added 2


## Acknowledgements
Give credit here.
- This project was inspired by...
- This project was based on [this tutorial](https://www.example.com).
- Many thanks to...


## Contact
Created by [@flynerdpl](https://www.flynerd.pl/) - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
