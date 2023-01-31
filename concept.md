# Concept

High level, we have quite a few project-based courses, with the risk of students submitting the same final project in more than one course or the projects not having consistent rigor/expectations/difficulty depending on who is teaching the course. This is especially a problem with our capstone course. A benefit of this project approval tool is that it requires sign-off from faculty with subject expertise on the student's project or who teach the courses the project leverages, like the web and mobile faculty have to sign off that it is not a project from the web or mobile courses if it is a web or mobile project. This is not something that exists as an available product currently. 

If we can have such a system, it would further strengthen the quality of our student projects and provide oversight over student projects to ensure no duplication of projects occurs before the student has already completed the project. The hope is such a system would be similar to the workflow of document signing or travel request approval systems in terms of the ease of its usage. 

## Tech Stack

* Client Side Options:
  * Flutter
    * Initially just Flutter for Web but if a PWA form of Flutter for Web isn't enough could have native apps long term. 
  * None
    * may not necessitate dynamic client side functionality
* Server Side Options:
  * Python-Based
    * Django
  * Go-Based
    * Revel
    * Gin
    * Chi
  * Rust-Based
    * Actix
    * Rocket

## Features

* Students
  * Authentication via Campus accounts
    * Google Auth or Shibboleth
  * Students can enroll in a given course
    * May want a feature to allow enrollment with a pin/passphrase but likely unnecessary. 
  * Students can see a form/mechanism to submit their project proposal. 
    * Students can add a faculty for approval should it be an extension of a previous project.
    * Student needs to tag the category of project so faculty associated with those topics are tagged to review. Limit of 1 review per proposal regardless of number of times tagged for a faculty member. 
  * Transparency for students of review process
    * Students should see where their project proposal is in the approval process, if returned due to issues/revisions needed will get notified. Also will get a notification when it's approved. 
* Faculty
  * Authentication via Campus accounts
    * Google Auth or Shibboleth
  * Create their course for an upcoming semester
    *  Ideally improved UI but functionally similar to what Turnin provides:
    *  <img width="876" alt="Screen Shot 2023-01-31 at 12 56 52 PM" src="https://user-images.githubusercontent.com/1179047/215881250-14422630-ad1c-471a-bf3a-3cf19e8bf4ed.png">
    *  Advanced feature, pull the data and match to faculty. Allowing them to enable their courses vs having to manually enter/create. See the discord bot feature as an example. 
  *  Faculty can create a proposal submission for their course. 
    * Submission could be uploading a PDF (or long term other office document)
    * Alternatively, provide the ability to create a multi-part form, like a google form with different components for their proposal requested by the faculty member. 
    * Ability to add a grading feedback/rubric potentially
  * Faculty Review Process
    * Should have an inbox of pending reviews, ideally also email notifications
    * Can open review and approve or send back with feedback/comments. Faculty could also suggest other faculty who need to review. The suggested faculty could be selected by area tag or directly. Need to limit it to only 1 review required for the proposal if they get double tagged. 
  * Dashboard of students/approval
    * Faculty should have a simple dashboard to see the submission/approval status of all their students at a glance. 
    * Ability to look into details for each student from here. 
