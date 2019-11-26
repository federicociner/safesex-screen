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



## 5 Research Overview
#### Overview
Chlamydia is a sexually transmitted disease caused by a bacteria called Chlamydia trachomatis. It is an infection that usually affects young, sexually active persons. Chlamydia trachomatis is a bacteria responsible for most sexually transmitted infections [1]. In most of the cases, the infection is asymptomatic which means it has no symptoms in fact 70% of women and 50% of men chlamydia produces few or no symptoms and remains undetected. Chlamydia can cause complications if not treated, especially in young women.

In Denmark the infection rate of chlamydia is about 456/100 000 in 2007. It is reported that around 10% of women and 13% of men aged under 25 years have chlamydia infection (1). In 2015 more than 1M chlamydia infection cases were reported in the US (2) Reported infection rates have increased in the last 10 years, this is due to the expansion of screening and better reporting systems (2).

  

Gonorrhea is also a sexually transmitted disease, it is caused by a bacteria called Neisseria gonorrhoeae. Just like chlamydia it is most common among young, aged under 25 years and sexually active persons. It can be asymptomatic, especially in women (2).

Gonorrhea is the second most common STD. in 2015 more than 1M cases of Gonorrhea infection were reported in the US (2).

  

Chlamydia and Gonorrhea can cause cervicitis, urethritis, proctitis, and pelvic inflammatory disease (PID). It is crucial to prevent and detect these infections early in order to protect and improve the sexual and individual health of patients and of the community. (2)

  

Patients infected with gonorrhea are more likely to be co-infected with chlamydia (3). It is recommended that a patient diagnosed with chlamydia or gonorrhea should consider screening for other STDs such as syphilis and HIV.

  

#### Tests and Screening

There has been major advancements in chlamydia and gonorrhea detection in the past 30 years, there are different diagnosis method but cell culture remains as a reference.

Repeated NAAT test ( Nucleic Acid Amplification Testing ) is the most sensitive test for chlamydia and gonorrhea (2)(1).

There are other available tests with different costs, specificity and sensitivity. Examples of those tests are Cell culture and Nucleic acid hybridization tests. (1) contains more details about various tests for chlamydia diagnosis.

  
In most cases Chlamydia and Gonorrhea infections are asymptomatic for both men and women. The United States Preventive Services Task Force and Centers for Disease Control and Prevention recommend screening for chlamydia every year for sexually active women aged under 25 years and for older women with risk factors or high risk sexual behaviours (2)(4). They do not recommend routine screening for men because of lack of evidence, efficiency and cost-effectivness, but still suggest targeted screening in heterosexual men with high sexual activity, men in correctional facilities, adolescent and STD’s clinics (2)(4).

Annual screening for gonorrhea is recommended for women aged under 25 years and for other women with increased risk factors (4). Those risk factors could be, having new or multiiple sex partners, not using protection, drug use, engaing in commercial sew work or living in communities with high disease prevelance.

Targeted screening is important for persons showing symptoms of chlamydia and gonorrhea or persons or children victim of sex abuse, or persons having intercourse with partners having STDs.

  

#### Screening Barriers

Majority of doctors do not follow the recommended routine screening for teenage and young women for various reasons. The physician belief, work environment, gender, opinion, ideology and commitment, influence his or her decision to proceed with chlamydia and gonorrhea screening or not (5). All these factors, along with the patient's lack of awareness can present barriers to the recommended screening.

### Factors of higher risk of infection

In (2) Table 1 summarize some of History and Physical Examination Elements of Patients with Possible Chlamydia or Gonorrhea Infections, the following list summarizes the content of the table, these are the factors that can help determine the risk of infection:

-   Gender
    
-   Age under 25 and sexually active
    
-   Sexual contact with a person with an STD or STD related manifestation (symptoms)
    
-   Use of condoms
    
-   Number of sex partners in the past 60 days
    
-   New sex partners in the past 60 days
    
-   Environment with high STD diseases prevalence or not
    
-   Use of drugs
    
-   Exchange sex for drugs or money
    
-   Pain in joints or at sites of tendon insertions
    
-   Rash
    
-   Fever
    
-   Pharyngeal discomfort
    
-   Change in odor, amount, quality, color of vaginal discharge
    
-   Dysuria (painful or difficult urination)
    
-   Lower abdominal or pelvic pain
    
-   Pelvic pain with intercourse
    
-   Date of last menses
    
-   Pregnancy
    
-   Abnormal Intermenstrual bleeding
    
-   Urethral discharge, dysuria, testicular pain (for men)
    
-   Physical examination
    

-   Oral examination for lesions
    
-   Joint examination for tenderness and swelling
    
-   Rectal examination for mucosal friability, purulent discharge, perianal lesions
    
-   Inguinal, femoral, epitrochlear cervical nodes for swelling and/or tenderness
    
-   Pelvic speculum examination for vaginal pH, fluid characteristics, purulent discharge at the endocervix, cervical ectopy
    
-   Pelvic bimanual examination
    

The above mentioned factors can help decide whether or not to proceed with a screening for chlamydia and gonorrhea. Using this research overview, the above list and additional research if needed we will decide the factors that we will use in our application to determine whether or not to recommend a screening.

#### References
  

1.  Bébéar, C., & De Barbeyrac, B. (2009). Genital Chlamydia trachomatis infections. Clinical Microbiology and Infection, 15(1), 4-10.
    
2.  Workowski, K. (2013). Chlamydia and gonorrhea. Annals of internal medicine, 158(3), ITC2-1.
    
3.  Lyss, S. B., Kamb, M. L., Peterman, T. A., Moran, J. S., Newman, D. R., Bolan, G., ... & Ehret, J. (2003). Chlamydia trachomatis among patients infected with and treated for Neisseria gonorrhoeae in sexually transmitted disease clinics in the United States. Annals of internal medicine, 139(3), 178-185.
    
4.  Workowski, K. A., & Berman, S. M. (2011). Centers for Disease Control and Prevention sexually transmitted disease treatment guidelines. Clinical infectious diseases, 53(suppl_3), S59-S63.
    
5.  Cook, R. L., Wiesenfeld, H. C., Ashton, M. R., Krohn, M. A., Zamborsky, T., & Scholle, S. H. (2001). Barriers to screening sexually active adolescent women for chlamydia: a survey of primary care physicians. Journal of Adolescent Health, 28(3), 204-210.