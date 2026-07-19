# SQL Server Database Project Assignment

## Scenario
Design and implement a Hospital Management System database using SQL Server.
The system should manage patients, doctors, appointments, departments, medications, and prescriptions.

---

## Part 1 – Database Design (25 Marks)
Design the database from scratch.

### Required Tables
* Departments
* Doctors
* Patients
* Appointments
* Medications
* Prescriptions
* PrescriptionDetails
 
### Suggested Structure

**Departments**
* DepartmentId
* DepartmentName
* FloorNumber

**Doctors**
* DoctorId (PK)
* FullName
* Specialty
* Phone
* HireDate
* Salary
* DepartmentId

**Patients**
* PatientId
* FullName
* Gender
* BirthDate
* Phone
* Address

**Appointments**
* AppointmentId
* PatientId
* DoctorId
* AppointmentDate
* Status
* Notes

**Medications**
* MedicationId
* MedicationName
* UnitPrice
* Manufacturer

**Prescriptions**
* PrescriptionId
* AppointmentId
* PrescriptionDate

**PrescriptionDetails**
* PrescriptionDetailId
* PrescriptionId
* MedicationId
* Quantity
* Dosage
 
### Create all relationships.
The database should include:
* One Department → Many Doctors 
* One Doctor → Many Appointments 
* One Patient → Many Appointments 
* One Appointment → One Prescription 
* One Prescription → Many Prescription Details 
* One Medication → Many Prescription Details 

### Use:
* Primary Keys 
* Foreign Keys 
* Identity Columns 
* NOT NULL where appropriate
 
---

## Part 3 – Sample Data (10 Marks)
Insert realistic sample data.

**Minimum:**
* 5 Departments 
* 20 Doctors 
* 40 Patients 
* 80 Appointments 
* 30 Medications 
* 60 Prescriptions 
* 150 Prescription Details
 
---

## Part 4 – Stored Procedures (35 Marks)
Create stored procedures for CRUD operations.

**Department**
* InsertDepartment
* UpdateDepartment
* DeleteDepartment
* GetAllDepartments
* GetDepartmentById

**Doctor**
* InsertDoctor
* UpdateDoctor
* DeleteDoctor
* GetDoctorById
* GetAllDoctors

**Patient**
* InsertPatient
* UpdatePatient
* DeletePatient
* GetPatientById
* GetAllPatients

**Appointment**
* InsertAppointment
* UpdateAppointment
* DeleteAppointment
* GetAppointmentById
* GetAllAppointments

**Medication**
* InsertMedication
* UpdateMedication
* DeleteMedication
* GetMedicationById
* GetAllMedications
 
---

## Part 5 – Complex SELECT Stored Procedures (20 Marks)
The following procedures must use JOINs.

**1. Get Appointment Details**
Return:
* Appointment ID 
* Patient Name 
* Doctor Name 
* Department Name 
* Appointment Date 
* Status 

**2. Get Doctor Schedule**
Return all appointments for a given doctor ordered by date.

**3. Get Patient History**
Return:
* Patient 
* Doctor 
* Department 
* Appointment Date 
* Prescription Date 

**4. Get Prescription Details**
Return:
* Patient 
* Doctor 
* Medication 
* Quantity 
* Dosage 

---

## Part 6 – Reports Queries (20 Marks)
Create stored procedures for the following reports.

**Report 1**
Total appointments per doctor.
Output: `Doctor | Number Of Appointments`

**Report 2**
Total patients treated by each department.

**Report 3**
Average doctor's salary per department.

**Report 4**
Most prescribed medications.
Output: `Medication | Times Prescribed`

**Report 5**
Monthly number of appointments.
