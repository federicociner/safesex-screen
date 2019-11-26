

# Design Document


**Team**: *Team Cranky Euler*

## 1 Design Considerations


### 1.1 Assumptions


The purpose is to build a web-based tool that recommend screening for Chlamydia and Gonorrhea in a selection of patients. The app consists then of a doctor/provider facing portal with FHIR integraion that based on medical history for the patient and manual input about the patient can give insights or help decide whether or not they at increased risk of infection.  
For this we will use FHIR Api to interact with the database either by querying or modifying, we may add some backend logic to help determine if the patient is at risk of infection or not.  
The dependencies should be:
SQL, python, python-flask, javascript, react js

### 1.2 Constraints

The lack of formal medical experience
### 1.3 System Environment

Software: Chrome/Firefox browser Hardware: Not applicable in our case

## 2 Architectural Design


### 2.1 Component Diagram



![Component Diagram](https://i.ibb.co/Pxrkzz9/Untitled-Diagram.jpg)
### 2.2 Deployment Diagram

Based on the HDAP lecture:

![enter image description here](https://i.ibb.co/pXm0t0y/deploy-diag.jpg)

## 3 Class and Other Diagrams


![enter image description here](https://i.ibb.co/mC517Z7/class-Diagram.jpg)

## 4 User Interface Design

These are very basic UI Design to get an idea on the things we may need to implement


![enter image description here](https://i.ibb.co/gPkCxD5/login-page.png)

![Patient Search](https://i.ibb.co/3FTgFws/search-patients.png)


![Patient ass risk](https://i.ibb.co/0t0ryxM/patient-details.png)