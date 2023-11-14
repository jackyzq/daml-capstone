### I. Overview 
This project was created by using `empty-skeleton` template. It models a HR hiring system, with three Roles.
	- Applicant
	- Hiring Manager
	- Business Manager

Hiring Managers can create a Job template contract. Applicants can then create an Application contract apply for a job given the JD information provided by hiring managers. Hiring Managers can exercise ScreenApplication to either accept or reject the application based on the information provided the applicant. Upon getting accepted, Business Managers can then exercise GetScreenedApplicants to see all applicants. Business managers can then exercise AcceptApplication or RejectApplication to accept or reject the screened application.

### II. Workflow
  1. hrManager creates a Job contract as well as corresponding JD
  2. applicant Alice, Bob, Charlie all creates Application for a job given JD from hrManager
  3. hrManager exercises ScreenApplication to pass Alice's and Charlie's application and fail Bob's application
  4. businessManager uses GetScreenedApplicants to check all applicants who has passed the screening
  5. businessManager exercises RejectApplication to reject the job application of Alice
  businessManager exercises AcceptApplication to accept the job application of Charlie

### III. Compiling & Testing
To compile and test, run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```