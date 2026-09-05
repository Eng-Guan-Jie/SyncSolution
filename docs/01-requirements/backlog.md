# Product Backlog — Singto

## 1. Product Overview

**Singto** is a LINE-integrated scheduling assistant designed to simplify group appointment coordination. It helps users create appointments, collect participants' availability, analyze common available dates, and confirm a suitable appointment.

The Product Backlog contains the features and user stories required to develop the core Singto scheduling workflow.

---

## 2. Product Backlog

| ID    | Epic                       | User Story                                                                                                                                                                      | Priority | Story Points |
| ----- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -----------: |
| PB-01 | Appointment Management     | As an organizer, I want to create an appointment with basic details so that I can start the scheduling process.                                                                 | High     |            3 |
| PB-02 | Appointment Management     | As an organizer, I want to specify a scheduling period so that participants can provide availability within the relevant dates.                                                 | High     |            2 |
| PB-03 | Participant Access         | As a participant, I want to access an appointment through a shared link so that I can join the scheduling process easily.                                                       | High     |            2 |
| PB-04 | Availability Collection    | As a participant, I want to select my available dates so that the system can compare my availability with other participants.                                         | High     |            5 |
| PB-05 | Availability Collection    | As an organizer, I want to view the availability submitted by participants so that I can see the group's scheduling information in one place.                                   | High     |            3 |
| PB-06 | Availability Analysis      | As a user, I want the system to compare everyone's availability so that common available dates can be identified automatically.                                       | High     |            5 |
| PB-07 | Date Suggestion            | As an organizer, I want the system to suggest suitable dates based on participants' availability so that I can make a scheduling decision more efficiently.           | High     |            5 |
| PB-08 | Availability Summary       | As a user, I want to see a clear summary of common availability so that I can easily understand the suggested scheduling options.                                               | High     |            3 |
| PB-09 | Appointment Confirmation   | As an organizer, I want to confirm the selected date so that the final appointment can be recorded and shared with participants.                                       | High     |            3 |
| PB-10 | LINE Integration           | As a user, I want to start the scheduling process through a LINE group so that I can coordinate appointments without switching to a completely separate communication platform. | High     |            5 |
| PB-11 | LINE Integration           | As a participant, I want to receive a link to the scheduling web application through LINE so that I can submit my availability easily.                                          | High     |            3 |
| PB-12 | Notifications              | As a participant, I want to receive scheduling reminders so that I do not forget to submit my availability or attend a confirmed appointment.                                   | Medium   |            3 |
| PB-13 | Responsive Web Application | As a user, I want the web application to work well on mobile devices so that I can complete scheduling conveniently from my phone.                                              | Medium   |            3 |
| PB-14 | Testing                    | As a development team, we want to test the core scheduling workflow so that the system functions correctly and reliably.                                                        | High     |            5 |
| PB-15 | User Evaluation            | As a development team, we want to evaluate the system with users so that we can determine whether Singto improves the group scheduling experience.                              | Medium   |            3 |

---

## 3. Core User Workflow

The main Singto workflow is:

**Call Singto → Create an Appointment → Share Availability → Find the Best Date → Confirm the Appointment**

The corresponding backlog items are:

1. **Create an Appointment** — PB-01, PB-02
2. **Share Availability** — PB-03, PB-04
3. **Find the Best Date** — PB-05, PB-06, PB-07, PB-08
4. **Confirm the Appointment** — PB-09
5. **LINE Integration** — PB-10, PB-11

---

## 4. Acceptance Criteria

### PB-01 — Create Appointment

* Organizer can create a new appointment.
* Organizer can enter the basic appointment details.
* The system successfully creates and stores the appointment.

### PB-02 — Specify Scheduling Period

* Organizer can define the dates or period available for scheduling.
* Participants can only submit availability within the defined scheduling period.

### PB-03 — Participant Access

* Participants can access the appointment through a shared link.
* Participants can view the relevant appointment information.
* Participants do not need to install a standalone mobile application.

### PB-04 — Submit Availability

* Participants can select available dates.
* Participants can submit their availability successfully.
* Submitted availability is stored in the system.

### PB-05 — View Availability

* Organizer can view participants' submitted availability.
* Availability information is presented in a clear and understandable format.
* The system identifies which participants have submitted their availability.

### PB-06 — Analyze Availability

* The system compares the availability of multiple participants.
* The system identifies dates that are available for the group.
* The analysis is based on the availability submitted by participants.

### PB-07 — Suggest Best Dates

* The system generates suitable date options based on the availability analysis.
* Suggested options are ranked or presented clearly.
* Users can review the suggested options before confirming an appointment.

### PB-08 — Availability Summary

* Users can view a summary of common available dates.
* The summary is easy to understand on a mobile device.
* Users can distinguish suitable options from unavailable options.

### PB-09 — Confirm Appointment

* Organizer can select one of the suggested options.
* The selected date is saved as the confirmed appointment.
* Confirmed appointment information can be displayed to participants.

### PB-10 — LINE Integration

* Users can interact with Singto through LINE.
* Singto can initiate or support the scheduling process through a LINE group.
* The system can direct users to the relevant web application.

### PB-11 — Share Web Application Link

* Singto can provide the scheduling link through LINE.
* Participants can open the link and access the relevant appointment.
* The link directs participants to the correct scheduling session.

### PB-12 — Notifications

* Participants can receive relevant scheduling reminders.
* Notifications are sent for defined scheduling events.
* Users are not required to manually check the system repeatedly for reminders.

### PB-13 — Responsive Web Application

* The web application is usable on smartphones.
* Core scheduling functions remain accessible on smaller screens.
* The interface is readable and easy to navigate.

### PB-14 — Testing

* Core user workflows have defined test cases.
* Functional and integration tests are performed.
* No critical error prevents users from completing the main scheduling workflow.

### PB-15 — User Evaluation

* Users can complete the main scheduling workflow during evaluation.
* User feedback is collected regarding usability and usefulness.
* Results are compared against the project's success criteria.
* The evaluation considers whether the system reduces scheduling effort and discussion rounds.

---

## 5. Priority Definition

| Priority   | Definition                                                                                             |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| **High**   | Essential for the core scheduling workflow or required for the system to achieve its main objectives.  |
| **Medium** | Useful for improving usability or overall experience but not essential for the minimum viable product. |
| **Low**    | Nice-to-have features that can be considered if time and resources allow.                              |

---

## 6. Out of Scope

The following items are intentionally excluded from the Product Backlog to maintain the project's scope:

* Standalone mobile application
* Full Google Calendar or Apple Calendar synchronization
* Automatic appointment decisions without user confirmation
* Venue, restaurant, or transportation booking
* Payment or financial transaction features
* Weather-based scheduling
* Advanced activity recommendation
* Complex recurring appointment management