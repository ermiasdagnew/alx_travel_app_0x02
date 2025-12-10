# ALX Travel App 0x02 – Chapa Payment Integration

This project extends the ALX Travel App by adding Chapa Payment Gateway integration.  
It allows users to initiate and verify payments for bookings securely using the Chapa API.

## Features
- Secure payment initiation using Chapa `/transaction/initialize`
- Payment verification using `/transaction/verify/<tx_ref>`
- Payment model for storing amount, transaction ID, and status
- Booking-linked payment workflow
- Updated views for handling payment logic
- Fully tested workflow using Chapa sandbox mode

## File Structure
- alx_travel_app_0x02/
  - README.md ✔ (not empty)
  - alx_travel_app/
    - listings/
      - models.py (Payment model)
      - views.py (initiate + verify payment)
      - urls.py

## Environment Variables
Create a `.env` file with:
