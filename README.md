# Deploy Directus On Railway

This example deploys a self-hosted version of [Directus](https://directus.io).

It uses a PostgreSQL database to store the data and local volume to store files (optionally from S3 - commented in directus.config.js + use template with good variables for S3 settings).

Templates can be edited from : https://railway.app/account/templates

Deploy on Railway with local storage - Refer to template named 'directus postgres local storage :
[![Deploy on Railway with local storage - Refer to template named 'directus postgres local storage'](https://railway.app/button.svg)](https://railway.app/template/L8Xgg-)

## Services deployed

- Directus
- Postgres

## Requirement

- Local volume for file storage or commented alternative to S3 bucket for file storage (persistence between deploys)

## How to use

- Click the Railway button 👆
- Add the environment variables
  - If you do not add the S3 related environment variables, your images/files will not be persisted between deploys.
  - Common variable values :
    - CONFIG_PATH : directus.config.js
    - STORAGE_S3_ENDPOINT : s3.amazonaws.com
- After your app is deployed, visit the `/admin` endpoint to login using the initial admin user you entered during config.

## Component versions

- Check package.json for deployed versions
- To alter versions :
  - Clone locally your github project created from "Deploy on Railway"
  - Update versions in package.json
  - Locally refresh "pnpm-lock.yam" using "pnpm" tool with "pnpm install" (pnpm can be install with "npm install -g pnpm")
  - Push new files' versions to your repo
  - Railway will start a new deployment

## Credit

Original repo : [https://github.com/freekrai/directus-railway](https://github.com/freekrai/directus-railway)
