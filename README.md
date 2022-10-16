# Sign Language Symptom Detector App
> Real-time sign language detector app able to translate symptoms into text.
End to end project, from extracting the input data for training the model to production deployment.
> Live demo [_here_](https://signlanguagesymptoms.onrender.com/)

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Project Pipeline](#project-pipeline)
* [Features](#features)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)
<!-- * [License](#license) -->


## General Information

- How can we improve communication between deaf patients and healthcare professionals?
- As part of the final project for Le Wagon Data Science Bootcamp (Lisbon, Sep 22), together with 3 of my classmates we approached this question by building an end to end computer vision app able to predict sign language symptoms in real time. 
- By signing ASL (American Sign Language) symptoms via webcam, the deaf patient is able to communicate with the healthcare professionals in real time. This may be useful in emergency situations or when an interpreter is not readily available.  


## Technologies Used

- Python
- Media Pipe Holistic
- Open CV
- TensorFlow
- Keras
- JavaScript
- HTML
- PHP
- Render


## Project Pipeline

 **1. Extract Datapoints:** Collect the input data as coordinates from the movement of hands, face and body using Media Pipe Holistic and Open CV. Initially we extracted this coordinates from the [_WLASL_](https://dxli94.github.io/WLASL/) videos dataset. However, when training the model, we realized there was too much of a varience within the positions and close up frames of the signers. This resulted in the model having low accuracy and not really learning from the data. So instead we recorded the signs ourselves, collecting over 12 million datapoints and storing them as numpy arrays. 

**2. Train the model:**  Using Keras and Tensorflow, we build a deep neural network model. Instead of using the proposed LSTM, we used a single dense layer GRU model which not only proved better accuracy, but also made the model lighter and faster. This makes sense as the sequences of frames were short and the dataset was relatively small. 

**3. Deployment:** In order for the model to predict using a live webcam feed we translated the Python logic to JavaScript and processed it with PHP as a static website. Then was deployed via github in Render.    


## Features
- Predict sign over 4 different symptoms: Headache 🧠, Tired 😓, Sore throat 🤒 and Infection 😷


## Acknowledgements

- This project was based on [this tutorial](https://www.youtube.com/watch?v=doDUihpj6ro&t=125s) by Nicholas Renotte.
- Many thanks to Julien Berthomier and Vinicius Moura


## Contact
Created by [@pariosur](https://github.com/pariosur) - feel free to contact me!

