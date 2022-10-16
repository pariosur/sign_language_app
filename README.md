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
- By signing ASL (American Sign Language) symptoms via webcam, the deaf patient is able to communicate with the healthcare professionals in real time. This may be useful in emergency situations or when an interpreter is not readily available.  

## Project Pipeline and Technologies Used

• Extract Datapoints: Collect the input data as coordinates from the movement of hands, face and body using Media Pipe Holistic and Open CV. Initially we extracted this coordinates from the [_WLASL_] (https://dxli94.github.io/WLASL/) videos dataset. However, when training the model with these datapoints we realized that there was high varience in the positions and close up of the signers of the videos. This resulted in the model having very low accuracy and not really learning from the data. So instead we recorded the signs ourselves, collecting over 12 million datapoints and storing them as numpy arrays. 

• Train the model:  Using Keras and Tensorflow, we build a deep neural network model. Instead of using the proposed LSTM, we used a single dense layer GRU model which not only proved better accuracy, but also made the model lighter and faster. This makes sense as the sequences of frames were short and the dataset was relatively small. 

• Deployment: In order for the model to predict using a live webcam feed we translated the Python logic to JavaScript and processed it with PHP as a static website. Then was deployed via github in Render.    


## Features
- Predict sign over 4 different symptoms: Headache 🧠, Tired 😓, Sore throat 🤒 and Infection 😷


## Setup
What are the project requirements/dependencies? Where are they listed? A requirements.txt or a Pipfile.lock file perhaps? Where is it located?

Proceed to describe how to install / setup one's local environment / get started with the project.


## Acknowledgements

- This project was based on [this tutorial]([https://www.example.com](https://www.youtube.com/watch?v=doDUihpj6ro&t=125s)).
- Many thanks to Julien Berthomier and Vinicius Moura


## Contact
Created by [@pariosur](https://github.com/pariosur) - feel free to contact me!

