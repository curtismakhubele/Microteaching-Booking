# UNISA Micro-Teaching Booking App

A static HTML version of the rebuilt Micro-Teaching Booking app, packaged for GitHub and Azure Static Web Apps.

## Files

- `index.html` — the application entry point.
- `staticwebapp.config.json` — Azure Static Web Apps configuration for fallback routing and basic security headers.
- `.github/workflows/azure-static-web-apps.yml` — GitHub Actions workflow for deployment to Azure Static Web Apps.

## Deploy to GitHub

1. Create a new GitHub repository.
2. Extract this ZIP and upload/commit all files from this folder to the repository root. Include the hidden `.github` folder.
3. Commit and push to the repository's `main` branch (or update the workflow branch if you use another branch).

## Deploy to Azure Static Web Apps

1. In the Azure portal, create an **Azure Static Web App**.
2. Choose **GitHub** as the deployment source and connect the repository, or create the Azure resource first and configure the workflow below.
3. In the Azure Static Web App, copy its deployment token.
4. In GitHub, open **Settings → Secrets and variables → Actions → New repository secret**.
5. Name the secret `AZURE_STATIC_WEB_APPS_API_TOKEN` and paste the Azure deployment token as its value.
6. Ensure the GitHub Actions workflow is enabled. Push to `main` to trigger deployment.

The workflow uses `/` as the app location and no build output directory because this app is plain HTML/CSS/JavaScript and does not need a build step.

## Important security limitation

This is a static, browser-based app. User records and credentials are handled in browser storage, not a shared server database. The admin setup and login UI are suitable for a prototype/demo, but **are not secure production authentication**. Before using real student or university data, add a backend/API, server-side authentication, password hashing, authorization checks, and a shared database. Do not enter real or sensitive credentials into the prototype.
