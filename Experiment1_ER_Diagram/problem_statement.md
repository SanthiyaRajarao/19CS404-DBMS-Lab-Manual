# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# EX:1 ER Diagram 
## NAME: SANTHIYA R
## REG.NO:212223230192

## Scenario Chosen:
Hospital

## ER Diagram:
<img width="1536" height="1024" alt="hospital_er" src="https://github.com/user-attachments/assets/9f8f1c50-6559-496b-a79b-98341e6085e7" />


# Entities and Attributes:
Department:
Dept_ID (Primary Key)

Name

Head

Doctor:
Doctor_ID (Primary Key)

Name

Contact_No

Email

Specialization

Work_Schedule

Patient:
Patient_ID (Primary Key)

Name

DOB

Gender

Address

Contact_No

Email

Work_Schedule

Appointments:
App_ID (Primary Key)

Date

Time

Reason

Add_Notes

Medical Records:
Med_Rec_ID (Primary Key)

Diagnosis

Medications

Treatment

Test Results

# Relationships and Constraints:
Specialized (Department → Doctor):
One Department can have many Doctors.

A Doctor belongs to one Department. (1:N cardinality)

Assigned (Doctor → Appointments):
One Doctor can be assigned to multiple Appointments.

An Appointment is assigned to one Doctor. (1:N cardinality)

Book (Patient → Appointments):
One Patient can book multiple Appointments.

Each Appointment is booked by one Patient. (1:N cardinality)

Contain (Patient → Medical Records):
One Patient can have multiple Medical Records.

Each Medical Record belongs to one Patient. (1:N cardinality)

Check (Doctor → Medical Records):
One Doctor can check multiple Medical Records.

Each Medical Record is checked by one Doctor. (1:N cardinality)

Extension (Prerequisite / Billing):
Billing (Extension Idea):
Billing could be modeled by adding a new entity called Billing with attributes like Bill_ID, Amount, Payment_Method, and Payment_Status. It would have relationships with Appointments (each appointment generates a bill) and Patients (patients are billed for their appointments).

# Design Choices:
I chose the main entities such as Doctor, Patient, Appointments, Department, and Medical Records because they represent the core operations of a hospital.

Relationships like Specialized, Assigned, Book, and Contain were added to represent the real-world interaction between these entities.

I assumed that each appointment is uniquely identified and linked to one doctor and one patient.

Work schedules for both doctors and patients are stored to manage availability.

Medical records are detailed to include diagnosis, medications, treatment, and test results for better patient history tracking.

# Result:
Thus, the ER diagram for the hospital management system was successfully designed, and the entities, relationships, and constraints were clearly represented.
