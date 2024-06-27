# Blood and Organs Donation System Project 🩸🫀

### Project Overview ✨
The Blood and Organ Donation System is an Oracle Database project aimed to creat an efficient system for managing blood and organ donations. This system ensures effective tracking and allocation of donations to patients in need.

### Objectives 🎯
The system is designed to:
- **Track Donations:** Efficiently record and monitor blood and organ donations.
- **Manage Inventory:** Keep accurate records of blood and organ quantities and their expiry dates.
- **Facilitate Treatments:** Assist doctors in managing patient treatments and scheduling appointments.
- **Ensure Traceability:** Maintain comprehensive logs of donations and withdrawals to address any future issues.

### Database Design 🏥

The project involves the creation of several relational tables to manage different aspects of blood and organ donation. Each table is meticulously designed with specific attributes to handle unique data elements related to donors, doctors, patients, blood banks, and organ inventories. Primary and foreign key relationships are defined to maintain data integrity and facilitate complex queries.

1. **Donor Table**
   - **Attributes:** Donorid (Primary Key), Firstname, Middlename, Lastname, Address, Email, Phone, Age, Weight, MedicalCondition, Sex.
   - **Relationships:** Links with blood bank and organs inventory to track donations.

2. **Doctor Table**
   - **Attributes:** Docid (Primary Key), Dname, Salary, Qualification, Phone, Department.
   - **Relationships:** Handles appointments and requests for blood and organs.

3. **Patient Table**
   - **Attributes:** PatientID (Primary Key), Firstname, Middlename, Lastname, Email, Address, Phone, BloodAmount, BirthDate.
   - **Relationships:** Connects with doctors for treatment records.

4. **Blood Bank Table**
   - **Attributes:** BloodID (Primary Key), BloodQuantityLiter, BloodType, BloodExpiryDate.
   - **Relationships:** Manages blood donations and requests, linking donors and doctors.

5. **Organs Inventory Table**
   - **Attributes:** OrganCode (Primary Key), OrganName, OrganQuantity, ExpiryDate, DoctorID (Foreign Key).
   - **Relationships:** Tracks organ donations and transplants, linking with donors and doctors.

6. **DonatesIn Table**
   - **Attributes:** BloodAmount, DonationDate.
   - **Relationships:** Tracks blood donations with references to donor and blood bank.

7. **Gives Table**
   - **Attributes:** DonationDate.
   - **Relationships:** Tracks organ donations with references to donor and organs inventory.

8. **Treats Table**
   - **Attributes:** PatientID (Primary Key), DoctorID (Primary Key), Appointment.
   - **Relationships:** Manages patient appointments and treatments by doctors.

9. **Orders Table**
   - **Attributes:** DocID (Foreign Key), BloodID (Foreign Key), Amount, OrderDate.
   - **Relationships:** Manages blood requests by doctors from the blood bank.

## Contributors ✍️

- Sana Shamma
- Salwa Shamma
- Samah Shamma
- Shatha Faraj
