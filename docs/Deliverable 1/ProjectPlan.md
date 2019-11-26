# Project Plan: SafeSEX Screen

<!-- 
*This is the template for your project plan. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.*
-->

## Author: *Team Cranky Euler*


## 1 Introduction

<!-- 
*Here you introduce the product. Keep this  clean and simple, one or two sentences at most.*
--> 

The objective is to build a web-based tool that recommend screening for Chlamydia and Gonorrhea in sexually active women age 24 years and younger and in older women who are at increased risk for infection.	

## 2 Process Description

<!-- *Process description as a set of activities; for each activity, provide the following:* -->
- Authentication Service
- The service should authenticate the user into the application. It should allow the user to login and logout of the application.
- Input: Authentication information such as email, username e.t.c
- Output: Authentcation feedback, if successful, redirect to recommendation service, else inform user of the errors.

- Patient Screening Recommendation Service
- This service should provide recommendation to women on whether they should go for screening if they are likely to suffer from Chlamydia and Gonorrhea.
- Input: Patient health information: age, demographriics, medical history, sexual history e.t.c
- Output: Likelihood of suffering from Chlamydia, Gonorrhea, whether or not they should go for screening, how often they should go for screening.

- Integration with FHIR Screening Recommendation Service
- This service will help doctors recommend patients for screening of Chlamydia or Gonorrhea if they are at risk based on data accessible through the FHIR API.
- Input: Patients' medical history records, demographrics, sexual history
- Output: Likelihood of suffering from Chlamydia, Gonorrhea, whether or not they should go for screening, how often they should go for screening.


## 3 Team

<!-- *Describe the team and their roles (there may be more roles than there are team members)* -->

- Team members : 

Project Manager - Responsible for all aspects of project success. Defining project, building work plan, assigning work, and overseeing execution. 

Quality Assurance - Assures that project quality expectations will be fulfilled.

Sofware Developer - Responsible for building the project itself from a software perspective.  


| TITLE              |  |  | Name             |  | Email                    |
|--------------------|---|---|------------------|---|--------------------------|
| PROJECT MANAGER    |  |  | David Awad       |  | me@davidawad.com         |
| QUALITY ASSURANCE  |  |  | Anne Chepkeitany |  | rerimoianne.4@gmail.com  |
| SOFTWARE DEVELOPER |  |  | Wassim Fourati   |  | wassim9429@gmail.com     |
| SOFTWARE DEVELOPER |  |  | Federico Ciner   |  | federico.ciner@gmail.com |


## 4 Preliminary Questions

- What are the features the tool needs to support? 

- How will it be used? 

- Are we limited in any way in terms of the technologies we can use? 

- How do we determine who is and isn't at risk of infection? Is that part of research that we should do? Is that out of scope for us? 

- Any specific design we have to follow?

- Is our work affected in any way by the fact that another team (Terminators) is working on the same project? 
 




