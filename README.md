# Pet Shelter Application

A full-stack pet shelter application with a React frontend and AWS serverless backend.

## Project Structure

- `pet-shelter-client/` - React frontend application
- `pets-backend-working/` - AWS SAM serverless backend

## Frontend (pet-shelter-client)

React application built with Vite for managing pet adoptions.

### Setup
```bash
cd pet-shelter-client
npm install
npm run dev
```

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