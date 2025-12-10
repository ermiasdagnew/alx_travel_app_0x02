# ALX Travel App 0x02 – Chapa Payment Integration

This project extends the ALX Travel App by adding secure payment processing using the **Chapa API**.  
It includes payment initiation, verification, transaction tracking, and integration with bookings.

---

## 📌 Features Implemented

### ✔ Chapa API Integration
- Initiate payment requests using Chapa’s `/transaction/initialize` endpoint
- Redirect users to the secure Chapa checkout page
- Verify payments using `/transaction/verify/<tx_ref>`

### ✔ Payment Model
A `Payment` model tracks:
- booking
- amount
- transaction ID (tx_ref)
- status (`Pending`, `Completed`, `Failed`)

### ✔ Payment Workflow
1. User creates a booking  
2. App sends payment initiation request to Chapa  
3. Chapa returns a **checkout_url**  
4. After the user pays, the app verifies the transaction  
5. Payment status updates in the database  
6. Confirmation email (via Celery – optional)

---

## 📁 Project Structure

