# React + Vite

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
```

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
