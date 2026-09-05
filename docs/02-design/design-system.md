# Design System — Singto

## 1. Design Principles

The Singto design system follows these principles:

* **Simple:** Keep the scheduling process simple and avoid unnecessary steps.
* **Clear:** Present dates, availability, and appointment status in an easy-to-understand way.
* **Mobile-First:** Prioritize usability on smartphones because users commonly access scheduling links through mobile devices.
* **Consistent:** Use consistent components, spacing, typography, and interaction patterns throughout the application.
* **Efficient:** Help users complete scheduling tasks quickly with minimal manual coordination.

---

## 2. Design Tokens

Design tokens define the reusable visual values used throughout the Singto web application.

### 2.1 Colors

| Token            | Purpose                                    |
| ---------------- | ------------------------------------------ |
| `primary`        | Main brand color and primary actions       |
| `primary-hover`  | Hover or pressed state of primary actions  |
| `background`     | Main application background                |
| `surface`        | Cards, forms, and other content containers |
| `text-primary`   | Main text                                  |
| `text-secondary` | Supporting or less prominent text          |
| `border`         | Borders and dividers                       |
| `success`        | Confirmed or available states              |
| `warning`        | Pending or attention-required states       |
| `error`          | Errors and unavailable actions             |
| `disabled`       | Disabled elements                          |

Colors should provide sufficient contrast to maintain readability and distinguish important scheduling states.

### 2.2 Typography

| Token        | Purpose                            |
| ------------ | ---------------------------------- |
| `heading-1`  | Main page headings                 |
| `heading-2`  | Section headings                   |
| `heading-3`  | Card or component headings         |
| `body`       | Main body text                     |
| `body-small` | Supporting information             |
| `caption`    | Metadata and secondary information |
| `button`     | Button labels                      |

Typography should prioritize readability on mobile devices. Headings should provide a clear visual hierarchy, while body text should remain easy to read without excessive font variation.

### 2.3 Spacing

The system uses a consistent spacing scale:

```text
4px   — Extra small
8px   — Small
12px  — Compact
16px  — Default
24px  — Large
32px  — Extra large
48px  — Section spacing
```

Spacing should be used consistently between related elements, form fields, cards, and sections.

### 2.4 Border Radius

| Token         | Value | Usage                               |
| ------------- | ----: | ----------------------------------- |
| `radius-sm`   |   4px | Small controls and compact elements |
| `radius-md`   |   8px | Inputs, buttons, and cards          |
| `radius-lg`   |  12px | Large cards and main containers     |
| `radius-full` | 999px | Pills, tags, and status indicators  |

### 2.5 Shadows

Use subtle shadows to visually separate elevated components from the background.

* **Small:** Inputs and small interactive elements when necessary.
* **Medium:** Cards or important content containers.
* **Large:** Modals and dialogs.

Shadows should be used sparingly to maintain a clean and lightweight interface.

---

## 3. Component Rules

### 3.1 Buttons

Buttons should clearly communicate the action they perform.

**Primary Button**

* Used for the main action on a screen.
* Examples: `Create Appointment`, `Submit Availability`, `Confirm Appointment`.
* Only one primary action should normally be emphasized at a time.

**Secondary Button**

* Used for supporting actions.
* Examples: `Back`, `Edit`, `View Details`.

**Destructive Button**

* Used for actions that may remove or cancel information.
* Examples: `Cancel Appointment`, `Delete`.

**Button Rules**

* Use clear action-oriented labels.
* Buttons should have a sufficiently large touch target for mobile users.
* Avoid placing too many prominent buttons together.

---

### 3.2 Input Fields

Input fields are used when users need to provide appointment information.

Examples:

* Appointment title
* Appointment description
* Scheduling period

**Rules**

* Every input must have a clear label.
* Provide appropriate placeholder text when useful.
* Display validation feedback near the relevant field.
* Required fields should be clearly identified.
* Avoid unnecessary input fields to minimize user effort.

---

### 3.3 Date Selector

The date selector is a core scheduling component.

**Rules**

* Users should be able to select available dates easily.
* Selected states must be visually distinct.
* Unavailable or invalid dates should be clearly distinguishable.
* The interface should remain usable on mobile screens.
* Users should be able to review their selections before submitting.

---

### 3.4 Availability Grid

The availability grid summarizes participants' available dates.

**Rules**

* Display participant availability in a structured and easy-to-scan format.
* Clearly distinguish between:

  * Available
  * Unavailable
  * No response
* Common available periods should receive stronger visual emphasis.
* The layout should remain understandable when multiple participants are included.
* On small screens, the grid may use horizontal scrolling or an alternative mobile-friendly layout.

---

### 3.5 Suggested Date Card

Suggested Date Cards display dates identified by Singto as suitable options.

Each card should include:

* Date
* Number of available participants or relevant availability information
* Primary action to select the option

**Rules**

* The most suitable options should be easy to identify.
* Information should be concise.
* Avoid displaying unnecessary details that make comparison difficult.

---

### 3.6 Status Indicators

Status indicators communicate the current state of scheduling information.

Examples:

| Status      | Meaning                                    |
| ----------- | ------------------------------------------ |
| Available   | Participant is available                   |
| Unavailable | Participant is not available               |
| Pending     | Participant has not submitted availability |
| Confirmed   | Appointment has been confirmed             |
| Cancelled   | Appointment has been cancelled             |

Status should not rely on color alone. Use text, icons, or other visual indicators to ensure the meaning remains clear.

---

### 3.7 Cards

Cards are used to group related information.

Examples:

* Appointment information
* Participant information
* Suggested dates
* Availability summaries

**Rules**

* Each card should represent one clear group of information.
* Maintain consistent padding and spacing.
* Avoid excessive nesting of cards.

---

### 3.8 Navigation

Navigation should remain simple because the application focuses on a small number of scheduling tasks.

**Rules**

* Prioritize the current scheduling task.
* Avoid unnecessary navigation options.
* Provide a clear way to return to the previous step when appropriate.
* Maintain consistent navigation patterns throughout the application.

---

### 3.9 Notifications and Feedback

The system should provide immediate feedback when users perform important actions.

Examples:

* Availability submitted successfully.
* Appointment created successfully.
* Appointment confirmed.
* Invalid information.
* Submission failed.

**Rules**

* Feedback should clearly explain what happened.
* Error messages should explain how users can correct the problem.
* Success messages should not interrupt the workflow unnecessarily.

---

## 4. Responsive Design Rules

Singto follows a **mobile-first** design approach.

### Mobile

* Primary target for the web application.
* Use touch-friendly controls.
* Keep forms and interactions simple.
* Avoid unnecessarily wide layouts.
* Make important actions easy to reach.

### Desktop

* Support larger screens without changing the core workflow.
* Use additional screen space to improve information visibility.
* Availability tables or grids may use wider layouts when appropriate.

The core functionality and information hierarchy should remain consistent across screen sizes.

---

## 5. Accessibility Rules

The interface should be designed to support a wide range of users.

* Maintain sufficient text and background contrast.
* Do not use color as the only way to communicate information.
* Use descriptive labels for buttons and inputs.
* Provide clear error and success feedback.
* Ensure interactive elements have adequate touch targets.
* Maintain a logical reading and interaction order.

---

## 6. Component Consistency Rules

All components should follow these rules:

1. Use design tokens instead of arbitrary visual values whenever possible.
2. Reuse existing components rather than creating visually similar components with different styles.
3. Maintain consistent spacing and typography.
4. Use consistent interaction states such as default, hover, active, disabled, loading, and error where applicable.
5. Keep component behavior predictable across different screens.
6. Prioritize simplicity and clarity over decorative elements.

---

## 7. Core UI Components

The following components are considered essential for the Singto MVP:

* Appointment Form
* Date Selector
* Availability Grid
* Participant Status
* Availability Summary
* Suggested Date Card
* Confirmation Dialog
* Primary and Secondary Buttons
* Notification / Feedback Messages
* Responsive Layout

These components directly support the core workflow:

**Create Appointment → Submit Availability → Find the Best Date → Confirm Appointment**