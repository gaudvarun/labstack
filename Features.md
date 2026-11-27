# ACADENCE
## Complete Product Requirements Document (PRD) – Version 2.0

**Product Name:** ACADENCE  
**Full Name:** Academic Workflow & Submission Management System  
**Tagline:** Academic Work. Simplified.  
**Category:** Education Technology / Academic Workflow Management  
**Initial Target:** College IT Department  
**Future Target:** Entire college and multiple institutions  
**Platform:** Responsive Web Application  
**Document Type:** Product Requirements + UI/UX + Technical Specification + AI Development Blueprint  
**Version:** 2.0

---

# PART 1 — PRODUCT FOUNDATION

## 1.1 Product Overview

ACADENCE is a centralized academic workflow management platform designed to digitize and simplify the complete academic assignment and practical submission process in colleges.

It provides a common digital environment where students can submit academic work, faculty members can create assignments and evaluate submissions, and department administrators can monitor academic activities.

The system replaces fragmented processes involving:
- Physical assignment collection.
- Practical file registers.
- WhatsApp submission messages.
- Email attachments.
- Manually maintained spreadsheets.
- Individual student follow-ups.
- Manual submission reports.

ACADENCE brings all these processes into one organized platform.

### Core Product Workflow

**Faculty creates assignment → Student receives assignment → Student submits work → Faculty reviews submission → Faculty updates evaluation → Student receives feedback → System maintains academic records.**

## 1.2 Product Vision

To create a simple, reliable and centralized digital academic workspace that reduces repetitive administrative work for teachers and makes academic submissions transparent and trackable for students.

## 1.3 Primary Goals

1. Reduce faculty workload.
2. Digitize assignment and practical submissions.
3. Eliminate unnecessary manual registers.
4. Provide structured subject-wise management.
5. Simplify student submission tracking.
6. Enable faster evaluation.
7. Maintain permanent academic submission records.
8. Automate deadline monitoring.
9. Generate accurate academic reports.
10. Provide a scalable system for institutional deployment.

## 1.4 Target Users

| User | Primary Responsibility |
|---|---|
| Student | Submit and track academic work |
| Faculty | Create assignments and evaluate submissions |
| HOD | Monitor departmental academic activities |
| Administrator | Manage users and academic infrastructure |

## 1.5 Product Positioning

ACADENCE is not merely an assignment-uploading website.

It is a complete academic workflow management system that manages the entire lifecycle of academic work.

**Core value proposition:**

- Students: Know what to submit, when to submit and what has been checked.
- Faculty: Manage every assigned subject and student submission from one place.
- HOD: Monitor academic activities and generate reports without depending on manual registers.

---

# PART 2 — ACADEMIC STRUCTURE

## 2.1 Academic Hierarchy

The system must follow this exact academic hierarchy:

Institution → Academic Year → Department → Academic Year/Level → Semester → Subject → Assignment.

Example:

| Level | Example |
|---|---|
| Institution | Government Engineering College |
| Academic Year | 2026–27 |
| Department | Information Technology |
| Year | Second Year |
| Semester | Semester III |
| Subject | Database Management Systems |
| Assignment | Practical 01 – SQL Queries |

**Important architectural restriction:**

The college does not have divisions or sections.

Do not introduce division, section, class-group or section-allocation fields anywhere in the application, UI, database, filtering system or user workflows.

A year and its enrolled students form the relevant student cohort.

## 2.2 Subject Management

Each subject must have:
- Subject name.
- Subject code.
- Department.
- Academic year.
- Year.
- Semester.
- Enrolled student list.
- Assigned faculty members.

## 2.3 Faculty Subject Allocation

A faculty member may teach multiple subjects and multiple academic years.

Example:

| Faculty | Subject | Year | Semester |
|---|---|---|---|
| Faculty A | DBMS | SY IT | III |
| Faculty A | Java | FY IT | I |
| Faculty B | Mathematics | SY IT | III |

The system must support multiple faculty allocations without mixing academic records.

## 2.4 Workspace Separation

Every faculty member should have access to only their authorized teaching assignments.

Each subject workspace must maintain independent:
- Assignments.
- Student submissions.
- Evaluation records.
- Deadlines.
- Reports.
- Academic activities.

A teacher handling DBMS and Java must be able to switch between both subjects without seeing unrelated records.

---

# PART 3 — USER ROLES AND PERMISSIONS

## 3.1 Student Role

### Student Capabilities

- Register or access an administrator-created account.
- Log in securely.
- View academic profile.
- View department and current academic year.
- View enrolled subjects.
- View assignments.
- View practical tasks.
- Upload assignments.
- Submit homework and PPTs.
- Track submission status.
- Track evaluation status.
- View deadlines.
- Receive notifications.
- View teacher feedback.
- View marks.
- Download submission receipts.
- View submission history.
- Upload corrected versions when permitted.

### Student Restrictions

- Cannot modify roll number.
- Cannot change department independently.
- Cannot change academic year independently.
- Cannot access other students' private submissions.
- Cannot change teacher evaluation.
- Cannot modify assignment deadlines.
- Cannot view unauthorized faculty records.

## 3.2 Faculty Role

### Faculty Capabilities

- Log in securely.
- View assigned academic workspaces.
- Switch between subjects.
- View assigned student lists.
- Create assignments.
- Schedule assignments.
- Edit assignments.
- Upload reference materials.
- Select assignment recipients.
- View all submissions.
- Filter submissions.
- Search using roll number or name.
- Preview documents.
- Download documents.
- Bulk download submissions.
- Evaluate submissions.
- Add marks.
- Add remarks.
- Request resubmission.
- Mark submissions incomplete.
- Generate reports.
- View student submission history.
- Publish subject-specific announcements.

### Faculty Restrictions

- Cannot create unauthorized academic structures.
- Cannot modify student roll numbers.
- Cannot access unrelated subjects.
- Cannot access unauthorized student records.
- Cannot alter another faculty member's evaluation without appropriate permissions.
- Cannot modify system-wide administrator settings.

## 3.3 HOD Role

The HOD should have department-level oversight.

### Capabilities

- View department dashboard.
- Manage faculty accounts.
- Manage student accounts.
- Create academic years.
- Manage semesters.
- Manage subjects.
- Manage student enrollment.
- Allocate faculty to subjects.
- View department reports.
- Monitor pending submissions.
- Monitor faculty evaluation progress.
- View subject-wise analytics.
- Export academic reports.
- Manage department announcements.

## 3.4 System Administrator

The system administrator manages the platform infrastructure.

Capabilities:
- Create institutions.
- Configure institution settings.
- Create departments.
- Create HOD accounts.
- Configure platform-wide settings.
- Manage account permissions.
- Monitor system activity.
- Manage storage limits.
- Manage backups.
- Manage security settings.

The system administrator and department HOD should be separate permission levels.

---

# PART 4 — DETAILED FEATURE REQUIREMENTS

# MODULE 1: AUTHENTICATION AND ACCOUNT MANAGEMENT

## 1.1 Login Page

Create a premium, minimal login screen.

Fields:
- Email / College ID.
- Password.
- Remember me.
- Forgot password.
- Login button.

Provide role-aware redirection after authentication.

## 1.2 Registration

Students may register using approved college credentials.

Required fields:
- Full name.
- Enrollment number.
- Roll number.
- College email.
- Department.
- Academic year.
- Current year.
- Semester.

The registration process must verify the student's identity against an authorized student record or require administrator approval.

Faculty accounts should preferably be created or activated by HOD/admin.

## 1.3 Authentication Features

- Secure login.
- Logout.
- Password reset.
- Email verification.
- Session management.
- Role-based redirection.
- Profile updates.
- Account activation/deactivation.

---

# MODULE 2: FACULTY DASHBOARD

This is one of the most important areas of ACADENCE.

The faculty dashboard must be designed for fast academic task management.

## 2.1 Dashboard Layout

Top navigation:
- ACADENCE logo.
- Search.
- Notifications.
- User profile.
- Logout.

Sidebar:
- Overview.
- My Subjects.
- Assignments.
- Submissions.
- Calendar.
- Students.
- Reports.
- Settings.

## 2.2 Overview Statistics

Display the following cards:

1. Total Assigned Subjects.
2. Total Assigned Students.
3. Total Assignments Created.
4. Total Submissions Received.
5. Pending Evaluations.
6. Incomplete Submissions.

All statistics must be dynamically calculated from actual database records.

## 2.3 Recent Activity

Display:
- Recently submitted assignments.
- Recently evaluated work.
- New resubmissions.
- Upcoming deadlines.
- Recent assignment publications.

## 2.4 Assigned Subjects

Display each subject as a card.

Example:

**DBMS**
- Second Year IT.
- Semester III.
- 65 students.
- 8 assignments.
- 42 pending evaluations.

Actions:
- Open Workspace.
- View Assignments.
- View Submissions.

Another example:

**Java Programming**
- First Year IT.
- Semester I.
- 72 students.

The subject cards must be generated dynamically from faculty allocations.

## 2.5 Subject Switching

Faculty should be able to switch between assigned subjects through:
- Subject cards.
- Sidebar navigation.
- Subject selector.

Switching must preserve the correct subject context.

---

# MODULE 3: SUBJECT WORKSPACE

Each subject must have an independent workspace.

## 3.1 Subject Overview

Display:
- Subject name.
- Subject code.
- Academic year.
- Year.
- Semester.
- Number of enrolled students.
- Number of assignments.
- Total submissions.
- Pending evaluations.

## 3.2 Subject Navigation

The subject workspace should contain:

1. Overview.
2. Assignments.
3. Practicals.
4. Submissions.
5. Students.
6. Calendar.
7. Announcements.
8. Reports.

## 3.3 Students Section

Display all students enrolled in that subject.

Table fields:
- Roll number.
- Student name.
- Enrollment number.
- Email.
- Total assignments.
- Submitted assignments.
- Pending assignments.
- Checked assignments.

Search by name or roll number.

## 3.4 Subject Data Isolation

All operations must be scoped to the selected subject and its authorized academic context.

For example, when the faculty opens DBMS, the application must not show Java assignments or Java submissions.

---

# MODULE 4: ASSIGNMENT CREATION

Faculty must be able to create different types of academic tasks.

## 4.1 Assignment Categories

- Written Assignment.
- Practical File.
- Practical Journal.
- Homework.
- PPT Presentation.
- Mini Project.
- Major Project.
- Lab Record.
- Other Academic Work.

## 4.2 Assignment Creation Interface

Create a clean, multi-section form.

### Section A: Basic Information

- Assignment title.
- Assignment description.
- Category.
- Subject (automatically selected from current workspace).

### Section B: Academic Target

- Academic year.
- Department.
- Year.
- Semester.
- Entire enrolled class or selected students.

### Section C: Submission Requirements

- Allowed file formats.
- Maximum file size.
- Maximum number of files.
- Reference material.
- Additional instructions.

### Section D: Deadline Settings

- Publishing date.
- Submission deadline.
- Allow late submission.
- Allow resubmission.
- Resubmission deadline, if applicable.

### Section E: Evaluation Settings

- Maximum marks.
- Evaluation required.
- Feedback enabled.
- Physical verification required, if applicable.

### Section F: Publishing

Actions:
- Save Draft.
- Publish Now.
- Schedule Publication.

## 4.3 Assignment Management

Faculty should be able to:
- Edit assignments.
- Duplicate assignments.
- Extend deadlines.
- Close submissions.
- Cancel assignments.
- Archive assignments.
- View submission progress.

Important rules:
- Every assignment must have a unique ID.
- Published assignment changes must be logged.
- Deadline modifications must notify affected students.
- Existing submissions must never be silently deleted.
- Cancelled assignments must remain in academic history.

---

# MODULE 5: STUDENT DASHBOARD

The student dashboard should provide a simple overview of academic responsibilities.

## 5.1 Navigation

Sidebar:
- Dashboard.
- My Subjects.
- All Assignments.
- Practicals.
- Homework.
- PPTs.
- Upcoming Deadlines.
- My Submissions.
- Academic History.
- Notifications.
- Profile.

## 5.2 Dashboard Statistics

Display:
- Total Assigned Tasks.
- Pending Tasks.
- Submitted Tasks.
- Checked Tasks.
- Incomplete Tasks.
- Upcoming Deadlines.

## 5.3 Upcoming Assignments

Show the nearest upcoming deadlines.

Each assignment card should show:
- Assignment title.
- Subject.
- Category.
- Deadline.
- Submission status.
- Evaluation status.
- Action button.

## 5.4 My Subjects

Show subjects belonging to the student's academic enrollment.

Opening a subject displays all academic work related to that subject.

## 5.5 Assignment Details

The assignment details page should include:

- Title.
- Subject.
- Description.
- Instructions.
- Reference attachments.
- Publishing date.
- Deadline.
- Allowed formats.
- Maximum file size.
- Maximum marks.
- Submission status.
- Evaluation status.
- Previous submission information.

---

# MODULE 6: STUDENT FILE SUBMISSION

## 6.1 Upload Interface

Create a clean drag-and-drop file uploader.

Support:
- PDF.
- DOCX.
- PPTX.
- XLSX.
- JPG.
- JPEG.
- PNG.
- ZIP, where permitted.

## 6.2 Upload Workflow

1. Student opens assignment.
2. Reads instructions.
3. Selects file.
4. Uploads file.
5. System validates format and size.
6. Student reviews selected file.
7. Student adds optional comments.
8. Student confirms submission.
9. System stores file securely.
10. System creates submission record.
11. System generates a unique submission ID.
12. Student receives confirmation.

## 6.3 Submission Receipt

Display:
- Submission ID.
- Assignment title.
- Subject.
- Student name.
- Roll number.
- File name.
- Submission timestamp.
- Deadline comparison.
- Submission status.

Provide a receipt download option.

## 6.4 Submission Versioning

When resubmission is allowed:
- New uploads must create new versions.
- Previous files must remain available.
- Version timestamps must be maintained.
- Faculty must be able to compare previous and current versions.
- The system must identify the currently active version.

---

# MODULE 7: FACULTY SUBMISSION MANAGEMENT

This module should be inspired by e-commerce order management interfaces.

The teacher should receive all relevant submissions in an organized interface.

## 7.1 Submission Overview

Statistics:
- Total Submissions.
- Pending Review.
- Checked.
- Incomplete.
- Resubmission Required.
- Rejected.
- Late Submissions.
- Overdue Students.

## 7.2 Submission Views

Provide two views.

### Grid View

Each submission appears as an individual card.

### Table View

Each submission appears in a structured data table.

The teacher can switch between both views.

## 7.3 Submission Card

Display:

- Student name.
- Roll number.
- Assignment name.
- Subject.
- File name.
- Submission date and time.
- Deadline.
- Submission status.
- Evaluation status.
- Check button.

## 7.4 Advanced Filtering

Filters must support combined selection.

Available filters:

- Academic year.
- Department.
- Year.
- Semester.
- Subject.
- Assignment.
- Assignment category.
- Student name.
- Roll number.
- Submission status.
- Evaluation status.
- Submission date.
- Deadline.
- Late submission.
- Not submitted.

Example:

A teacher should be able to filter:

DBMS → SY IT → Practical 03 → Pending Review.

## 7.5 Search

Search by:
- Roll number.
- Student name.
- Assignment title.
- File name.
- Submission ID.

## 7.6 Sorting

- Roll number ascending.
- Roll number descending.
- Student name.
- Submission date.
- Deadline.
- Evaluation status.
- Marks.

## 7.7 Bulk Actions

Allow faculty to:
- Select multiple submissions.
- Download selected documents.
- Download all filtered documents as ZIP.
- Export records to Excel.
- Export records to PDF.
- Print submission lists.
- Send reminders to selected students.

Bulk actions must show a confirmation screen before execution.

Bulk evaluation should only be available when the action is appropriate for all selected records.

## 7.8 Missing Submission Records

Teachers must also be able to view students who have not submitted an assignment.

These students must appear as records even though they have no uploaded files.

The teacher can:
- Filter by Not Submitted.
- Search by roll number.
- Send reminders.
- Export pending student lists.

---

# MODULE 8: EVALUATION AND CHECKING

## 8.1 Evaluation Screen

When a teacher clicks Check, open a dedicated evaluation workspace.

### Layout

Left panel:
- Student information.
- Roll number.
- Enrollment number.
- Subject.
- Assignment.
- Submission time.
- Deadline status.
- Previous submissions.

Center panel:
- Document preview.
- Page navigation.
- Zoom.
- Full-screen mode.
- Download original file.

Right panel:
- Marks.
- Teacher remarks.
- Evaluation status.
- Evaluation date.
- Resubmission instructions.

## 8.2 Evaluation Actions

1. Checked.
2. Incomplete.
3. Resubmission Required.
4. Rejected.
5. Physically Verified.

## 8.3 Evaluation Rules

**Checked:** The work has been successfully verified.

**Incomplete:** Some required content is missing.

**Resubmission Required:** Student must submit a corrected version.

**Rejected:** Submission is not accepted. A reason must be provided.

**Physically Verified:** Faculty has physically checked the work and recorded the verification digitally.

## 8.4 Marks and Feedback

Faculty may:
- Enter marks.
- Add feedback.
- Attach feedback documents.
- Provide correction instructions.
- Set a resubmission deadline.
- Save evaluation.

Marks must never exceed the assignment's maximum marks.

Evaluation changes must preserve previous evaluation history.

## 8.5 Student Notification

After evaluation:
- Update student dashboard.
- Send in-app notification.
- Send email notification if enabled.
- Show remarks.
- Show marks.
- Display resubmission instructions where applicable.

---

# MODULE 9: STATUS MANAGEMENT ENGINE

Maintain two independent status systems.

## 9.1 Submission Status

| Status | Meaning |
|---|---|
| Not Submitted | No submission exists |
| Submitted On Time | Uploaded before or at deadline |
| Submitted Late | Uploaded after deadline |
| Overdue | Deadline passed without submission |
| Closed | Submission window closed |

## 9.2 Evaluation Status

| Status | Meaning |
|---|---|
| Not Evaluated | Not yet reviewed |
| Pending Review | Waiting for teacher |
| Checked | Successfully verified |
| Incomplete | Work is insufficient |
| Resubmission Required | Student must correct work |
| Rejected | Not accepted |
| Physically Verified | Verified offline |

These statuses must not overwrite each other.

For example:

A student can have:
- Submission status: Submitted Late.
- Evaluation status: Checked.

This distinction is essential.

## 9.3 Deadline Automation

The system must calculate deadline states automatically.

Rules:
- Deadline not passed + no submission = Pending.
- Submission timestamp within deadline = Submitted On Time.
- Submission timestamp after deadline = Submitted Late.
- Deadline passed + no submission = Overdue.
- Closed assignment = Closed for new submissions.

Use Asia/Kolkata as the default institution timezone.

---

# MODULE 10: STUDENT ACADEMIC HISTORY

Every student must have a complete academic submission record.

Display:
- Subject.
- Assignment.
- Category.
- Submission date.
- Submission version.
- Submission status.
- Evaluation status.
- Marks.
- Faculty remarks.
- Resubmission history.

Students can access their own records.

Faculty can access records only within their authorized academic responsibilities.

Previous academic-year records must remain accessible according to institutional retention policies.

---

# MODULE 11: HOD / ADMIN MANAGEMENT

## 11.1 HOD Dashboard

Display:
- Total students.
- Total faculty.
- Total subjects.
- Total assignments.
- Total submissions.
- Pending evaluations.
- Department submission percentage.

## 11.2 Academic Structure Management

Admin can create and manage:
- Academic years.
- Departments.
- Years.
- Semesters.
- Subjects.
- Student enrollments.

## 11.3 Faculty Management

- Add faculty.
- Edit faculty profile.
- Activate/deactivate faculty.
- Assign subjects.
- Assign academic years.
- Assign classes.
- Modify allocations.

## 11.4 Student Management

- Add students.
- Edit student records.
- Import students through CSV/Excel.
- Update roll numbers through authorized actions.
- Promote students.
- Transfer students.
- Deactivate accounts.

## 11.5 Monitoring

HOD can monitor:
- Subject-wise assignments.
- Subject-wise submissions.
- Student completion.
- Pending evaluations.
- Faculty evaluation progress.
- Late submissions.

---

# MODULE 12: NOTIFICATION SYSTEM

## Student Notifications

- Assignment published.
- Deadline approaching.
- Deadline changed.
- Submission successful.
- Submission checked.
- Incomplete submission.
- Resubmission required.
- Marks published.
- Assignment cancelled.

## Faculty Notifications

- New submission.
- Late submission.
- Resubmission received.
- Upcoming deadline.
- Pending evaluations.

## HOD Notifications

- New faculty account.
- Allocation changes.
- Department-level alerts.

## Notification Channels

MVP:
- In-app notification center.
- Email notifications where configured.

Future:
- Browser push notifications.
- WhatsApp notifications through an authorized provider.

---

# MODULE 13: ACADEMIC CALENDAR

## Student Calendar

Show:
- Upcoming assignments.
- Practical deadlines.
- Homework deadlines.
- Resubmission deadlines.
- Completed tasks.

## Faculty Calendar

Show:
- Scheduled assignments.
- Submission deadlines.
- Pending evaluations.
- Academic announcements.

Calendar views:
- Daily.
- Weekly.
- Monthly.

Calendar events must be connected to actual assignments rather than manually duplicated records.

---

# MODULE 14: REPORTS AND ANALYTICS

## Faculty Reports

- Total assignments.
- Total submissions.
- Pending submissions.
- Checked submissions.
- Incomplete submissions.
- Late submissions.
- Not submitted students.
- Average marks.
- Assignment completion percentage.

## Student Reports

- Total assignments.
- Completed submissions.
- Pending work.
- Late submissions.
- Marks.
- Feedback history.

## HOD Reports

- Department-wide statistics.
- Subject-wise completion.
- Year-wise completion.
- Faculty-wise evaluation progress.
- Semester-wise statistics.
- Academic-year comparisons.

## Export Options

- Excel.
- CSV.
- PDF.

Reports must reflect actual database records.

---

# PART 5 — COMPLETE USER JOURNEYS

## USER JOURNEY 1: FACULTY LOGIN

1. Open ACADENCE.
2. Enter credentials.
3. Authentication succeeds.
4. Faculty dashboard opens.
5. Assigned subjects appear.
6. Faculty selects DBMS.
7. DBMS workspace opens.
8. Faculty views subject activities.

## USER JOURNEY 2: CREATE ASSIGNMENT

1. Open assigned subject.
2. Click Create Assignment.
3. Enter title.
4. Enter instructions.
5. Select category.
6. Confirm academic year and semester.
7. Select entire class or individual students.
8. Add reference files.
9. Configure submission rules.
10. Set deadline.
11. Configure marks.
12. Publish or save draft.
13. Students receive notifications.

## USER JOURNEY 3: STUDENT SUBMISSION

1. Student logs in.
2. Opens dashboard.
3. Selects subject.
4. Opens assignment.
5. Reads instructions.
6. Uploads file.
7. Reviews file.
8. Confirms submission.
9. System records submission.
10. Student receives receipt.
11. Faculty dashboard updates.

## USER JOURNEY 4: FACULTY EVALUATION

1. Faculty opens subject.
2. Clicks Submissions.
3. Views all submission records.
4. Searches or applies filters.
5. Opens a particular student submission.
6. Previews file.
7. Checks the document.
8. Adds marks and remarks.
9. Selects evaluation status.
10. Saves evaluation.
11. Student receives notification.

## USER JOURNEY 5: RESUBMISSION

1. Teacher requests resubmission.
2. Teacher adds correction instructions.
3. Student receives notification.
4. Student opens the assignment.
5. Student reviews feedback.
6. Uploads corrected version.
7. System preserves previous version.
8. Faculty receives notification.
9. Faculty checks the new version.
10. Evaluation record is updated.

## USER JOURNEY 6: HOD ALLOCATES SUBJECT

1. HOD logs in.
2. Opens Faculty Management.
3. Selects faculty member.
4. Selects academic year.
5. Selects department.
6. Selects year and semester.
7. Selects subject.
8. Confirms allocation.
9. Faculty workspace updates automatically.

---

# PART 6 — COMPLETE UI/UX DESIGN SYSTEM

## 6.1 Overall Design Direction

ACADENCE must have a premium, modern SaaS aesthetic.

Visual inspiration:
- Linear for clean navigation.
- Notion for organized content.
- Stripe for polished dashboard components.
- Modern education SaaS products for academic workflows.

Do not copy another product's branding or layout directly.

The design must be original.

## 6.2 Brand Identity

Brand name: ACADENCE

Tagline: Academic Work. Simplified.

Logo direction:
- Minimal geometric symbol.
- Abstract letter A.
- Subtle reference to academic progress and connected workflows.
- Modern typography.
- No generic graduation-cap illustration.

## 6.3 Color Palette

Primary:
- Deep Navy: #172554
- Indigo: #4338CA
- Secondary Indigo: #6366F1

Background:
- Main: #F8FAFC
- Surface: #FFFFFF
- Subtle Surface: #F1F5F9

Typography:
- Primary Text: #0F172A
- Secondary Text: #64748B

Status:
- Success: #16A34A
- Warning: #D97706
- Error: #DC2626
- Information: #2563EB

Use status colors consistently.

## 6.4 Typography

Primary font: Inter.

Use:
- Semibold for headings.
- Medium for labels.
- Regular for descriptions.
- Tabular numbers for statistics and reports.

## 6.5 Design Language

- Clean layouts.
- Rounded corners.
- Subtle shadows.
- Thin borders.
- Consistent spacing.
- Clear visual hierarchy.
- Professional icons.
- Minimal gradients.
- No excessive glassmorphism.
- Avoid unnecessary animations.

## 6.6 Desktop Layout

Use a consistent application shell.

**Left Sidebar:**
- Logo.
- Navigation.
- Main modules.
- Collapsible behavior.

**Top Navigation:**
- Breadcrumbs.
- Global search where relevant.
- Notifications.
- Profile menu.

**Main Workspace:**
- Page heading.
- Descriptive subtitle.
- Primary actions.
- Dashboard cards.
- Tables or cards.
- Filters.

## 6.7 Mobile Layout

The entire application must be responsive.

Requirements:
- Mobile-friendly navigation.
- Collapsible sidebar or drawer.
- Responsive cards.
- Horizontal scrolling only where necessary.
- Mobile file upload.
- Touch-friendly controls.
- Responsive tables.
- Properly sized modal windows.

Do not create a separate inferior mobile experience.

## 6.8 Component Library

Create reusable components:

- Button.
- Input.
- Select.
- Date picker.
- Modal.
- Dropdown.
- Status badge.
- Data table.
- Search field.
- Filter panel.
- Pagination.
- Subject card.
- Assignment card.
- Submission card.
- Statistics card.
- File uploader.
- Document preview.
- Notification item.
- Empty state.
- Loading skeleton.
- Confirmation dialog.

Use consistent design tokens.

---

# PART 7 — SCREEN-BY-SCREEN DESIGN SPECIFICATION

## Screen 1: Login

Design:
- Split layout on desktop.
- Branding and short product description on one side.
- Login form on the other.
- Minimal design.
- Responsive single-column layout on mobile.

## Screen 2: Student Dashboard

Display:
- Welcome message.
- Summary statistics.
- Upcoming deadlines.
- Recent assignments.
- Recent submissions.
- Recent feedback.

Primary action: View Pending Work.

## Screen 3: Faculty Dashboard

Display:
- Welcome message.
- Statistics.
- Assigned subject cards.
- Recent submissions.
- Pending evaluations.
- Upcoming deadlines.

Primary action: Open Subject Workspace.

## Screen 4: Subject Workspace

Display:
- Subject heading.
- Academic year.
- Year.
- Semester.
- Student count.
- Navigation tabs.
- Recent activity.
- Assignment overview.

Primary actions:
- Create Assignment.
- View Submissions.

## Screen 5: Assignment Creation

Use a structured multi-section form.

Include:
- Basic details.
- Academic target.
- Recipient selection.
- File settings.
- Deadline.
- Evaluation settings.
- Publish controls.

Use clear validation.

## Screen 6: Student Assignment Listing

Use assignment cards with:
- Title.
- Subject.
- Category.
- Deadline.
- Status.
- Action.

Allow filtering by:
- Subject.
- Category.
- Status.
- Deadline.

## Screen 7: Submission Upload

Display:
- Assignment information.
- Instructions.
- Reference documents.
- File upload area.
- Selected files.
- Submission comments.
- Confirm button.

## Screen 8: Faculty Submission Management

Use an e-commerce-inspired management interface.

Top:
- Submission statistics.

Below:
- Search.
- Filters.
- Grid/Table switch.
- Bulk actions.

Main content:
- Submission cards or data table.

The teacher should be able to inspect hundreds of submissions efficiently.

## Screen 9: Evaluation Screen

Use a three-panel desktop layout.

Left: Student information.

Center: Document viewer.

Right: Evaluation controls.

On smaller screens, use a stacked layout or collapsible panels.

## Screen 10: Student History

Display a chronological academic history grouped by:
- Academic year.
- Semester.
- Subject.
- Assignment.

## Screen 11: HOD Dashboard

Display:
- Department statistics.
- Student count.
- Faculty count.
- Subject count.
- Submission analytics.
- Evaluation progress.
- Recent activity.

## Screen 12: Faculty Management

Display:
- Faculty list.
- Search.
- Account status.
- Assigned subjects.
- Allocation management.

## Screen 13: Student Management

Display:
- Student list.
- Roll number.
- Enrollment number.
- Name.
- Academic year.
- Department.
- Account status.

Support bulk import.

## Screen 14: Reports

Display:
- Filters.
- Charts.
- Tables.
- Export options.

---

# PART 8 — DATABASE ARCHITECTURE

Use PostgreSQL through Supabase.

Recommended tables:

| Table | Purpose |
|---|---|
| institutions | Institution information |
| profiles | User profiles |
| departments | Department records |
| academic_years | Academic years |
| semesters | Semester records |
| academic_levels | FY, SY, TY, etc. |
| subjects | Subject information |
| student_enrollments | Student academic enrollment |
| faculty_allocations | Faculty-subject allocations |
| assignments | Assignment information |
| assignment_recipients | Entire class or selected students |
| assignment_attachments | Teacher reference files |
| submissions | Submission records |
| submission_files | Uploaded file information |
| submission_versions | Version history |
| evaluations | Evaluation history |
| notifications | User notifications |
| announcements | Academic announcements |
| activity_logs | Audit history |

## Important Relationships

- One institution has multiple departments.
- One department has multiple subjects.
- One academic year has multiple academic levels.
- One academic level can have multiple semesters.
- One subject can have many students.
- One subject can have multiple faculty allocations.
- One faculty member can have multiple allocations.
- One assignment belongs to one subject.
- One assignment can target an entire enrolled class or selected students.
- One assignment can receive many submissions.
- One submission can contain multiple files if allowed.
- One submission can have multiple versions.
- One submission can have multiple evaluation records.

Do not store repeated student or subject information unnecessarily in multiple tables.

Use proper relational constraints.

## Important Historical Data Rule

When a student's enrollment or academic year changes, previous submissions must remain associated with their original academic context.

Historical records must not be overwritten.

---

# PART 9 — TECHNICAL STACK

Recommended stack:

| Layer | Technology |
|---|---|
| Frontend | React |
| Language | TypeScript |
| Build Tool | Vite |
| Styling | Tailwind CSS |
| UI Components | shadcn/ui |
| Icons | Lucide |
| Backend | Supabase |
| Database | PostgreSQL |
| Authentication | Supabase Auth |
| File Storage | Supabase Storage |
| Server Functions | Supabase Edge Functions |
| Charts | Recharts |
| Forms | React Hook Form |
| Validation | Zod |
| Deployment | Vercel |
| Version Control | GitHub |

Use environment variables for all secrets.

Never expose Supabase service-role credentials in frontend code.

---

# PART 10 — SECURITY REQUIREMENTS

Security must be implemented at the backend and database level, not just by hiding frontend buttons.

## 10.1 Row Level Security

Enable RLS on all sensitive tables.

### Student Access

Students can:
- Read their own profile.
- Read their own submissions.
- Create submissions for eligible assignments.
- Read their own evaluations.
- Read their own notifications.

Students cannot:
- Access other students' private documents.
- Modify evaluation records.
- Access faculty-only data.

### Faculty Access

Faculty can:
- Access authorized subjects.
- Create assignments for allocated subjects.
- View submissions for authorized assignments.
- Evaluate eligible submissions.
- Access relevant student records.

### HOD Access

HOD can access authorized departmental records.

### Administrator Access

System administrators have platform-level management permissions.

## 10.2 File Security

- Use private storage buckets.
- Generate signed URLs.
- Validate file extensions.
- Validate MIME types.
- Restrict file sizes.
- Prevent unauthorized downloads.
- Sanitize filenames.
- Consider malware scanning.
- Do not trust client-side file validation alone.

## 10.3 Audit Logs

Maintain records for:
- Assignment creation.
- Assignment modification.
- Deadline changes.
- Submission creation.
- Resubmission.
- Evaluation.
- Marks modification.
- Faculty allocation changes.
- Account changes.

---

# PART 11 — BUSINESS RULES AND EDGE CASES

1. A student cannot submit an assignment they are not authorized to access.
2. A student cannot submit after the deadline if late submission is disabled.
3. Late submissions must preserve the actual submission timestamp.
4. A deadline extension must preserve the previous deadline in the audit log.
5. Previous submission files must remain accessible according to permissions.
6. Evaluation history must never be silently overwritten.
7. A cancelled assignment must preserve its academic history.
8. A student transferred to another academic cohort must retain historical records.
9. Faculty allocation changes must not delete previous evaluations.
10. A failed file upload must not create a successful submission record.
11. Duplicate submission requests must be handled safely.
12. Marks must not exceed maximum marks.
13. Only authorized faculty can evaluate a submission.
14. An overdue record must be calculated from the assignment deadline and submission data.
15. No-submission records must be generated for eligible students.
16. A resubmission must create a new version.
17. A faculty member must not access unauthorized subject workspaces.
18. Assignment recipients must be recalculated carefully if student enrollment changes; historical assignment eligibility must be preserved.
19. All timestamps must be stored consistently and displayed using the institution timezone.
20. Important destructive actions must require confirmation.

---

# PART 12 — NON-FUNCTIONAL REQUIREMENTS

## Performance

- Fast initial page loading.
- Server-side pagination.
- Efficient search and filtering.
- Lazy-loaded document previews.
- Optimized dashboard queries.
- Avoid downloading unnecessary files.

## Reliability

- No lost submission records.
- Secure upload confirmation.
- Database backups.
- Recovery strategy.

## Scalability

The application should support:
- Multiple academic years.
- Increasing student counts.
- Multiple subjects.
- Multiple faculty members.
- Large submission volumes.

## Accessibility

- Keyboard navigation.
- Readable text.
- Accessible form labels.
- Sufficient contrast.
- Clear validation errors.

## Maintainability

- Modular architecture.
- Reusable components.
- Typed database models.
- Centralized validation.
- Consistent error handling.
- Documented database policies.

---

# PART 13 — MVP DEVELOPMENT ROADMAP

Build ACADENCE incrementally.

## Phase 1: Project Foundation

- Set up React + TypeScript.
- Set up Tailwind CSS.
- Build brand identity.
- Create reusable components.
- Connect Supabase.
- Configure authentication.
- Implement role-based navigation.

## Phase 2: Academic Management

- Create institution.
- Create department.
- Create academic years.
- Create academic levels.
- Create semesters.
- Create subjects.
- Add students.
- Add faculty.
- Configure faculty allocations.

## Phase 3: Faculty Workspace

- Faculty dashboard.
- Assigned subject cards.
- Subject workspace.
- Student list.
- Assignment creation.

## Phase 4: Student Workspace

- Student dashboard.
- Subject listing.
- Assignment listing.
- Assignment details.
- File upload.
- Submission receipts.

## Phase 5: Submission Management

- Submission dashboard.
- Grid view.
- Table view.
- Search.
- Filters.
- Sorting.
- Individual document preview.
- Bulk downloads.

## Phase 6: Evaluation

- Evaluation screen.
- Status management.
- Marks.
- Feedback.
- Resubmission.
- Version history.

## Phase 7: Administration and Reports

- HOD dashboard.
- Student management.
- Faculty management.
- Faculty allocations.
- Analytics.
- Excel/PDF exports.

## Phase 8: Testing and Deployment

- Role permission testing.
- Database security testing.
- File upload testing.
- Deadline testing.
- Mobile testing.
- Performance testing.
- Production deployment.

---

# PART 14 — ACCEPTANCE CRITERIA

The MVP is ready for pilot deployment when:

1. Students can log in securely.
2. Faculty can log in securely.
3. HOD can manage academic structure.
4. Faculty sees only assigned subjects.
5. Faculty can switch between subjects.
6. Every subject has an independent workspace.
7. Faculty can create assignments.
8. Faculty can target the entire class or selected students.
9. Students can view eligible assignments.
10. Students can upload supported documents.
11. Every submission receives a unique ID.
12. Submission timestamps are recorded correctly.
13. Faculty can see all relevant submissions.
14. Faculty can filter by student, roll number, subject and assignment.
15. Faculty can preview and download documents.
16. Faculty can mark work as checked.
17. Faculty can mark work incomplete.
18. Faculty can request resubmission.
19. Students can see teacher feedback.
20. Previous submission versions are preserved.
21. Overdue students are identified automatically.
22. Teachers can export submission reports.
23. HOD can view departmental statistics.
24. Unauthorized access is prevented.
25. The application works properly on desktop and mobile.

---

# PART 15 — VIBE CODING IMPLEMENTATION INSTRUCTIONS

This section is specifically intended for an AI-powered development environment.

## 15.1 Overall Development Instruction

Build ACADENCE as a production-oriented, functional academic workflow management application.

Do not build a static UI prototype.

All primary interactions must be connected to real application state and backend functionality.

Use React, TypeScript, Tailwind CSS, shadcn/ui and Supabase.

The system must have:
- Functional authentication.
- Role-based dashboards.
- Real database integration.
- Secure file storage.
- Working assignment workflows.
- Working submission workflows.
- Working evaluation workflows.
- Functional search and filtering.
- Dynamic analytics.

## 15.2 Strict Academic Structure Instruction

The college does not have divisions or sections.

Do not create:
- Division fields.
- Section fields.
- Division dropdowns.
- Section filters.
- Division-wise reports.
- Division allocation tables.

Use:
- Academic Year.
- Department.
- Year.
- Semester.
- Subject.
- Student.

## 15.3 Design Instructions

Create a premium SaaS interface.

The design must be:
- Professional.
- Minimal.
- Consistent.
- Responsive.
- Clean.
- Information-rich.
- Easy to navigate.

Use deep navy, indigo, white and subtle grey surfaces.

Use Lucide icons.

Use realistic empty states, loading states, error states and confirmation dialogs.

Do not use excessive gradients, giant typography or unnecessary animations.

Do not create generic dashboard designs with decorative statistics that do not connect to actual data.

## 15.4 Functional Development Rules

- Build reusable components.
- Keep student, faculty and HOD modules separated.
- Use typed data models.
- Use proper validation.
- Implement server-side authorization.
- Use database transactions where appropriate.
- Implement secure file uploads.
- Add pagination for large datasets.
- Preserve submission history.
- Maintain activity logs.
- Avoid unnecessary database duplication.
- Never use hardcoded mock records as production functionality.

Seed demo data may be used for development, but must be clearly separated from real institutional data.

## 15.5 Important Implementation Principle

Do not attempt to build every feature in one uncontrolled generation.

Build in phases.

After completing each phase:
1. Verify the feature.
2. Test the database integration.
3. Test role permissions.
4. Check responsive design.
5. Fix errors.
6. Continue to the next phase.

Do not replace existing working functionality when adding a new module.

Maintain consistent database relationships and component architecture throughout development.

---

# PART 16 — INITIAL DEMONSTRATION DATA

For development and testing, create clearly labelled sample records.

Institution: Demo Engineering College.

Department: Information Technology.

Academic Year: 2026–27.

Students:
- Rahul Sharma – Roll No. 24.
- Amit Patil – Roll No. 31.
- Priya Deshmukh – Roll No. 18.

Faculty:
- Faculty A – DBMS.
- Faculty A – Java Programming.

Subjects:
- DBMS – SY IT – Semester III.
- Java Programming – FY IT – Semester I.

Sample assignment:
- DBMS Practical 03.
- Category: Practical.
- Maximum Marks: 10.
- Deadline: Configurable.

Use these records only for demonstration and testing.

---

# PART 17 — FINAL PRODUCT DEFINITION

ACADENCE is a digital academic workflow management platform that brings students, teachers and department administrators into one organized academic environment.

Its core capabilities include:

**For Students:**
- View assignments.
- Submit academic work.
- Track deadlines.
- Track checking status.
- View feedback.
- Maintain academic history.

**For Faculty:**
- Manage multiple assigned subjects.
- Create assignments.
- Receive submissions.
- Filter student records.
- Check documents.
- Award marks.
- Request corrections.
- Generate reports.

**For HODs:**
- Manage academic infrastructure.
- Allocate faculty.
- Manage students.
- Monitor submissions.
- Generate departmental reports.

The platform transforms the traditional academic submission process into a centralized, transparent and trackable digital workflow.

# ACADENCE

**Academic Work. Simplified.**

*One platform. Every submission. Complete academic visibility.*

---

END OF PRD – VERSION 2.0
