# Selected Use Case Descriptions - Hospital Management System

The following tables describe the four major use cases selected for detailed sequence modeling: Book Appointment, Diagnostic Test Request and Result Review, Prescription and Medication Dispensing, and Billing and Payment.

---

## UC1: Book Appointment

| Field | Description |
|---|---|
| **Use Case Name** | Book Appointment |
| **Primary Actor** | Patient |
| **Goal** | Allow a patient to book an appointment with a doctor through the hospital system. |
| **Preconditions** | Patient is registered/authenticated. Doctor schedule exists in the system. |
| **Main Flow** | 1. Patient selects the book appointment option. <br> 2. Patient enters appointment details such as doctor/specialty, date, and time. <br> 3. System validates patient information. <br> 4. System checks doctor availability. <br> 5. System saves the appointment record. <br> 6. System sends an appointment confirmation notification. <br> 7. Patient receives booking confirmation. |
| **Alternative Flow** | If the selected slot is unavailable, the system displays alternative available slots and asks the patient to choose another time. |
| **Postcondition** | Appointment is saved in the centralized database and confirmation is sent to the patient. |

---

## UC2: Diagnostic Test Request and Result Review

| Field | Description |
|---|---|
| **Use Case Name** | Diagnostic Test Request and Result Review |
| **Primary Actor** | Doctor |
| **Supporting Actor(s)** | Laboratory Staff / Radiology Staff |
| **Goal** | Allow the doctor to request diagnostic tests and review uploaded lab or radiology results. |
| **Preconditions** | Patient medical record exists. Doctor is authorized to access the patient record. |
| **Main Flow** | 1. Doctor opens the patient medical record. <br> 2. System retrieves and displays the patient record. <br> 3. Doctor requests a diagnostic test. <br> 4. System saves the test request. <br> 5. System forwards the request to laboratory or radiology staff. <br> 6. Laboratory/radiology staff uploads the diagnostic result. <br> 7. System saves the result in the patient medical record. <br> 8. System notifies the doctor that results are available. <br> 9. Doctor reviews the diagnostic results. |
| **Alternative Flow** | If diagnostic results are not uploaded yet, the system displays the test status as pending. |
| **Postcondition** | Diagnostic results are stored in the patient medical record and become available for doctor review. |

---

## UC3: Prescription and Medication Dispensing

| Field | Description |
|---|---|
| **Use Case Name** | Prescription and Medication Dispensing |
| **Primary Actor** | Doctor |
| **Supporting Actor(s)** | Pharmacist |
| **Goal** | Allow the doctor to write a prescription and allow the pharmacist to process and dispense medication. |
| **Preconditions** | Patient has been examined. Patient medical record exists. |
| **Main Flow** | 1. Doctor writes a prescription through the system. <br> 2. System saves the prescription in the patient record. <br> 3. Pharmacist views the prescription. <br> 4. System retrieves prescription details. <br> 5. Pharmacist processes the prescription. <br> 6. System updates the prescription status. <br> 7. Pharmacist dispenses the medication. <br> 8. System records the dispensing status. |
| **Alternative Flow** | If medication is unavailable, the pharmacist updates the prescription status as unavailable. |
| **Postcondition** | Prescription and dispensing status are updated in the centralized database. |

---

## UC4: Billing and Payment

| Field | Description |
|---|---|
| **Use Case Name** | Billing and Payment |
| **Primary Actor** | Billing Officer |
| **Supporting Actor(s)** | Patient |
| **Goal** | Allow the billing officer to generate invoices and record payments, and allow the patient to view billing details. |
| **Preconditions** | Patient has received hospital services such as appointment, treatment, test, or prescription. |
| **Main Flow** | 1. Billing officer generates an invoice. <br> 2. System retrieves billing data from the centralized database. <br> 3. System saves the invoice. <br> 4. System sends a billing notification to the patient. <br> 5. Billing officer records payment details. <br> 6. System updates payment status. <br> 7. Patient views billing details through the portal. <br> 8. System displays invoice and payment information. |
| **Alternative Flow** | If payment is partial, the system records the payment as partially paid. If no billing record exists, the system displays that no billing information is available. |
| **Postcondition** | Invoice and payment status are saved in the centralized database and can be viewed by the patient. |