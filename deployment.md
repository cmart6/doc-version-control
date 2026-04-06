The frontend is deployed through Vercel using GitHub integration.

- Pushes to `main` trigger production deployment
- Pull requests can generate preview deployments

## Backend Deployment

The backend is deployed separately using Azure Functions.

## Required Environment Variables

- NEXT_PUBLIC_API_URL
- AZURE_FUNCTIONS_BASE_URL
- SQL_CONNECTION_STRING
- AZURE_STORAGE_CONNECTION_STRING

## Deployment Steps

1. Push code to GitHub
2. CI runs build validation
3. Vercel auto-deploys frontend from `main`
4. Azure backend remains hosted separately

## Rollback

Use Vercel deployment history to redeploy a previous successful version if needed.
