# Use Case Model

**Author**: Cranky Euler

## 1 Use Case Diagram

![Use Case Diagram](https://drive.google.com/uc?export=view&id=18Fx0OKexsdR236HLQBwb-KyokFWT6KuG)

## 2 Use Case Descriptions

### 2.1 User Login

* _Requirements_: This use case must allow a provider to log in to the application with a unique user ID.
* _Pre-conditions_: The user must have launched the application and already have an existing user ID on the local instance of the application.
* _Post-conditions_: The user will be logged into the application and will be redirected to the main landing page.
* _Scenarios_:
  * 2.1.1: The user has logged and is taken to a main landing screen, where he can choose to view existing screening recommendations for existing patients or generate a new screening recommendation record.

### 2.2 Generate Screening Recommendation

* _Requirements_: This use case must allow a provider to generate a chlamydia/gonorrhea screening recommendation from existing patient health records and manually-entered data.
* _Pre-conditions_:
  * The user must have launched the application.
  * The user must be logged in to the application.
* _Post-conditions_:
  * A new screening recommendation record will be created for a given patient and written to the application instance database.
  * The existing recommendation records list will be updated.
* _Scenarios_:
  * 2.2.1 _Create New Recommendation Records(s)_
    * The user will navigate to the "generate new recommendation screen".
    * On this screen, the user will need to enter patient details, including but not limited to:
      * Full name
      * Personal details
      * Sexual history
      * Other relevant information for chlamydia/gonorrhea screening purposes
    * Once the user is done editing the inputs listed aboved, he can submit the information, which will create a new record in the application's database instance.
    * In addition to using the manually-entered data, the application will query the external FHIR API to get additional medical history for a given patient, which will be used to generate a patient recommendation.
    * After the screening recommendation has been successfully saved and updated in the application's database instance, a confirmation message containing the unique ID of the newly created recommendation record will be displayed. Furthermore, the screen will also display the following details:
      * Likeliness of a patient to have chlamydia or gonorrhea.
      * Recommendation for whether they should get screened for chlamydia/gonorrhea or not.
      * Recommendation for frequency of screenings.

### 2.3 View Patient Records

* _Requirements_: This use case must allow a player to choose a cryptogram to choose a cryptogram from a list of available cryptograms, save/submit a solution to a chosen cryptogram, and see previously solved cryptograms.
* _Pre-conditions_:
  * The user must have launched the application.
  * The user must be logged in to the application.
  * At least one patient recommendation record must exist on the application database instance.
* _Post-conditions_:
  * The application will display a list of available patient recommendation records.
  * The application database instance will be updated when a record is deleted.
* _Scenarios_:
  * 2.3.2 _Query Patient Data_
    * The application will display a list of existing recommendation records, which the user can use to select a particular record to get additional information for that record.
    * Once a given record has been selected, it will redirect it to a page that displays the following information for that patient recommendation record:
      * Patient details e.g. full name, personal details.
      * Recommendation information e.g. frequency of screenings, likeliness to have chlamydia or gonorrhea, screening recommendation (yes/no).
  * 2.3.2 _Delete Existing Recommendation Records(s)_
    * On a particular patient recommendation record's information page, the user will have the ability to delete the record by clicking the "Delete" button/
    * This will prompt the user with a confirmation prompt - if the user selects "Yes", the record will be removed from the application database instance and the user will be redirected back to the main page, which lists all existing recommendation records.
