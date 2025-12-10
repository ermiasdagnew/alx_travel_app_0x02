# Chapa Payment Integration – alx_travel_app_0x02

This project integrates the Chapa payment gateway into the Django travel booking app.

## Features
- Initiate payments through Chapa API
- Verify payments after checkout
- Store payments in the Payment model
- Automatic status updates (Pending → Completed/Failed)

## Setup

### 1. Install dependencies
pip install requests django djangorestframework

### 2. Environment Variables
Create:
CHAPA_SECRET_KEY=your_secret_key

### 3. Run Migrations
python manage.py makemigrations
python manage.py migrate

### 4. API Endpoints

#### Initiate Payment
POST /payment/initiate/

body:
{
  "amount": "1200",
  "booking_reference": "booking123"
}

#### Verify Payment
GET /payment/verify/<transaction_id>/

### 5. Testing
Use Chapa sandbox mode to simulate transactions.

Logs and screenshots should be included in your submission.
