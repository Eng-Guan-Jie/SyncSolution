# User Journey — Singto

## Core Workflow

The core user journey describes how a group uses Singto to create an appointment, collect everyone's availability, identify a suitable date, and confirm the appointment.

**Call Singto → Create an Appointment → Share Availability → Find the Best Date → Confirm the Appointment**

---

## Step 1: Call Singto

**Actor:** Organizer

The organizer starts the scheduling process by interacting with Singto through a LINE group chat.

**User Action:**

* Call or interact with Singto in the LINE group.
* Select the option to create a new appointment.

**System Response:**

* Singto starts the appointment creation process.
* The organizer is directed to the web application when necessary.

---

## Step 2: Create an Appointment

**Actor:** Organizer

The organizer creates a scheduling session and provides the basic appointment information.

**User Action:**

* Enter the appointment title or details.
* Specify the dates or scheduling period.
* Create the appointment.

**System Response:**

* The system creates and stores the appointment.
* A scheduling link is generated for participants.

---

## Step 3: Share Availability

**Actor:** Organizer & Participants

The organizer shares the scheduling link through the LINE group. Participants use the link to submit their availability.

**User Action:**

* Participants open the shared link.
* Select the dates they are available.
* Submit their availability.

**System Response:**

* The system stores each participant's availability.
* The system updates the scheduling information as participants submit their responses.

---

## Step 4: Find the Best Date

**Actor:** System & Organizer

After collecting availability, Singto analyzes the submitted information to identify suitable dates.

**System Action:**

* Compare the availability of all participants.
* Identify common available dates.
* Generate suitable scheduling options.

**User Action:**

* Organizer reviews the availability summary.
* Organizer reviews the suggested dates.

**System Response:**

* Singto presents the most suitable options clearly to the organizer.

---

## Step 5: Confirm the Appointment

**Actor:** Organizer

The organizer selects the final date from the suggested options.

**User Action:**

* Select a suitable date.
* Confirm the appointment.

**System Response:**

* The system records the confirmed appointment.
* The confirmed appointment information is displayed or shared with participants.

---

## Journey Outcome

The group successfully reaches a scheduling decision without repeatedly asking each participant for their availability through the group chat.

The core journey is designed to reduce:

* Repeated scheduling discussions
* Manual comparison of availability
* Waiting for multiple rounds of responses
* Scattered scheduling information

The expected outcome is a faster and clearer process for reaching a confirmed appointment.

---

## Core Workflow Diagram

```text
┌───────────────┐
│  Call Singto  │
│    (LINE)     │
└───────┬───────┘
        ↓
┌─────────────────────┐
│ Create an           │
│ Appointment         │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Share Availability  │
│ Participants enter  │
│ available dates     │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Find the Best Date  │
│ Singto compares and │
│ suggests options    │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Confirm Appointment │
│ Organizer selects   │
│ final date          │
└─────────────────────┘
```