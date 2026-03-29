# Pet Shelter Application
A full-stack pet shelter application with a React frontend and AWS serverless backend.

**DISCLAIMER: This project is proprietary educational content from Amazon Cloud Institute (ACI) and is part of a structured learning program. This code is for educational purposes only and should not be redistributed or used commercially.**


## Project Tree

```
aci-pet-shelter-learning/
│
├── pet-shelter-client/          # React Frontend (Vite)
│   ├── public/
│   ├── src/
│   │   ├── assets/              # Images & static files
│   │   ├── components/
│   │   │   ├── Home.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── AboutUs.jsx
│   │   │   ├── Pets.jsx
│   │   │   ├── AdoptionForm.jsx
│   │   │   ├── Applications.jsx
│   │   │   └── ApplicationDetail.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── .env
│   ├── package.json
│   └── vite.config.js
│
└── pets-backend-working/        # AWS SAM Serverless Backend (Python)
    ├── handlers/
    │   ├── get_pets/            → GET /pets
    │   ├── create_adoption/     → POST /adoptions
    │   ├── get_adoption/        → GET /adoptions/{id}
    │   ├── get_adoptions/       → GET /adoptions
    │   ├── generate_presigned_url/ → S3 image upload
    │   ├── create_report/       → trigger report generation
    │   ├── generate_report_data/
    │   └── generate_html/       → HTML report rendering
    ├── scripts/                 # DB seeding & S3 bucket setup
    ├── template.yaml            # SAM infrastructure definition
    └── samconfig.toml           # SAM deploy config

    Key relationships:

The React frontend calls the Lambda handlers via API Gateway

DynamoDB stores pets, adoptions, and interest data

S3 handles pet images (via presigned URLs) and generated reports

SAM (template.yaml) defines and deploys all backend infrastructure
```

## Architecture

![Architecture Diagram](Pets%20Shelter%20Application%20MVP%20Architecture.png)

## Project Structure

- `pet-shelter-client/` - React frontend application
- `pets-backend-working/` - AWS SAM serverless backend

## Frontend (pet-shelter-client)

React application built with Vite for managing pet adoptions.

### Running the React frontend application
```bash
cd pet-shelter-client
npm install
npm run dev
```

![Running the React frontend application](images/Running%20the%20React%20frontend%20application.png)
# Access the frontend application by following the link at the right of  ➜  Local:

## Backend (pets-backend-working)

AWS SAM application with Lambda functions for pet and adoption management.

### Setup
```bash
cd pets-backend-working
sam build
sam deploy
```

## Features

- Pet listing and management
- Adoption application system
- Report generation
- Image management with S3

## Technologies

- Frontend: React, Vite
- Backend: AWS Lambda, DynamoDB, S3
- Infrastructure: AWS SAM