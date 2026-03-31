# SmartParcel — NET_214 Project

## Student Information
- Name: Ahmad Aljanahi
- Student ID: 20210001364
- Email: 20210001364@students.cud.ac.ae
- AWS Account ID: 362586210312

## Project Overview
SmartParcel is a cloud-native parcel tracking system built for the NET_214 Network Programming project.

It supports:
- Parcel creation
- Parcel status tracking
- Role-based API access
- Delivery proof photo upload to S3
- Parcel storage in DynamoDB
- Status notification pipeline using SQS, Lambda, and SNS
- Health monitoring endpoint
- Concurrent request handling using Gunicorn

## Tech Stack
- Python
- Flask
- Gunicorn
- AWS EC2
- AWS DynamoDB
- AWS S3
- AWS SQS
- AWS Lambda
- AWS SNS
- AWS CloudWatch

## API Endpoints
- `GET /health`
- `POST /api/parcels`
- `GET /api/parcels/<parcel_id>`
- `PUT /api/parcels/<parcel_id>/status`
- `GET /api/parcels`
- `DELETE /api/parcels/<parcel_id>`
- `POST /api/parcels/<parcel_id>/photo`

## Authentication
API uses the `X-API-Key` header.

Example keys:
- Admin: `key-admin-001`
- Driver: `key-driver-001`
- Customer: `key-customer-001`

## Run Locally on EC2
```bash
source ~/smartparcel/venv/bin/activate
cd ~/smartparcel
python app.py
