# EEG Data Collection GUI Enhancement

## Table of Contents

1. [Project Overview](#project-overview)
2. [Teams Involved](#teams-involved)
3. [Features to be Added](#features-to-be-added)


---

## Project Overview

Enhance the existing EEG Data Collection GUI by adding new features aimed at improving usability, data management, and user support. This project will involve collaboration between the **Experimentation Team** of R&D the **Real Time Signals Team** and the **UI/UX Integration Team** of Software to ensure the successful integration of these features over the next week and a half.

## Teams Involved

- **Design Team**
  - Ensure GUI implements all necessary user interface and user experience for successful experiment design.
  - Team Lead: Amrita Arora
  - Members: Please include all names working on this project

- **UI/UX Integration Team**
  - Handles the implementation of new features (described below) and communication with other teams.
  - Team Lead: Zarqa Fathima
  - Members: Please include all names working on this project

- **Real Time Signals Team**
  - Implements fucntionality for signal acquisitiion and approriate data storage. Communicate with other teams.
  - Team Lead: Maddox Fletcher
  - Members: Amrut Pennaka, Hibba Mansoor, Maddox Fletcher, Samarth Rao, Sruthi Chintaparthi

## Features to be Added

### 1. Allow input for subject name and questionaire for subject
- **Description:** Before data collection occurs require the subject to enter their name. Subsequently, the subject should be prompted with a set of questions that will ask questions about sleep, recent food intake, use of caffeine and other questions provided by design team. These questions should only be asked if the subjects name hasn't been entered in the last 12 hours.  
- **Assigned Team:** Design Team (R&D) & UI/UX Integration Team (Software) & RT Signals Team (Software)

### 2. Signal Acquisition
- **Description:** Implement code to acquire data in real time. Recordings should be labeled with direction, name, session number, and questionaire responses. Data should be saved after each 7 second recording.
- **Features:**
  * Create a function to initialize board using BrainFlow
  * After the focus period (Indicated by plus sign in Center) a function should be called that starts data collection. 
    * Data collection runs for 7 seconds in total
    * Reference [BrainFlow Documentation](https://brainflow.readthedocs.io/en/stable/) for support
  * After data collection period a function should be called that grabs the last 7 seconds of data
    * Brainflow has a function for this
    * Only save EEG channels
  * Data saving
    * Decide on a data type that allows storage of the numpy EEG file, the label, the questionaire responses, session number, and patient name
    * Decide on data naming structure to allow for easy identification of individual recordings
      * Create formal documentation for this and send it to your team lead.
- **Assigned Team:** RT Signals Team (Technical Integration)

### 3. Data Saving Pipeline
- **Description:** Implement a pipeline that saves data to a cloud directory. I suggest UT Box for now. This does not need to be in real time but atleast all samples sould be saved to cloud after each session.
- **Assigned Team:** RT Signals Team (Software)

### 4. After Session Menu
- **Description:** After each session provide a menu that allows the user to continue recording instead of exiting the application.
- **Assigned Team:** UI/UX Integration Team (Software)

### 5. Session Tracking
- **Description:** instead of having to input the session number, implement functionality so that the session number is tracked for each subject.
- **Assigned Team:** RT Signals Team (Software)





