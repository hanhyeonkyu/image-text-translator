# Image Text Extract and Translation

## Overview

An application that allows a user to upload an image containing text. The text will be extracted, and translated to any selected language.

It is built using:

- Python Flask for the UI
- Event driven functions for the backend
- Google Cloud serverless components for hosting: i.e. Cloud Run and Cloud Functions
- Google pre-built ML APIs for the extraction and translation

## Repo Structure

```text
└── image-text-translator
    ├── docs/
    |
    ├── infra-tf/               - Terraform for installing infra
    |
    ├── scripts/                - For environment setup and helper scripts
    |   └── setup.sh            - Setup helper script
    |
    ├── app/                    - The Application
    │   ├── ui_cr/                - Browser UI (Cloud Run)
    │   │   ├── static/             - Static content for frontend
    |   |   ├── templates/          - HTML templates for frontend
    |   |   ├── app.py              - The Flask application
    |   |   ├── requirements.txt    - The UI Python requirements
    |   |   ├── Dockerfile          - Dockerfile to build the Flask container
    |   |   └── .dockerignore       - Files to ignore in Dockerfile
    |   |
    │   └── backend_gcf/          - Backend (Cloud Function)
    │       ├── main.py             - The backend CF application
    │       └── requirements.txt    - The backend CF Python requirements
    |
    ├── testing/
    │   └── images/
    |
    ├── requirements.txt          - Python requirements for project local dev
    └── README.md                 - Repo README
```

## Walkthrough and Detailed Guide

- How the solution is architected
- Design choices and rationale
- A walkthrough of how you can do the same, end-to-end, including:
  - Dev environment setup (including Google Cloud SDK, VS Code, Cloud Code)
  - Service accounts and roles
  - Application Default Credentials (ADC)
  - The coding for the UI (Python, Flask, Jinja templates) and backend (Python)
  - How to test locally
  - How to deploy to Google Cloud (using Google Artifact Registry and Cloud Build)
- Cost management tips
- Performance tips

## Todo

Some improvements I'll make soon...

- Captcha
- CI/CD
- IaC