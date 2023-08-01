# Deploy Directus On Railway

This example deploys a self-hosted version of [Directus](https://directus.io). 

It uses a PostgreSQL database to store the data and S3 to store files.

[![Deploy directus on Railway](https://railway.app/button.svg)](https://railway.app/template/y5trbj?referralCode=8EB8ml)

## Services deployed

- Directus
- Postgres

## Requirement

- S3 bucket for file storage (persistence between deploys)

## Versions

- Check package.json for deployed versions

## How to use

- Click the Railway button 👆
- Add the environment variables
  - If you do not add the S3 related environment variables, your images/files will not be persisted between deploys.
  - Common variable values :
    -  CONFIG_PATH : directus.config.js
    -  STORAGE_S3_ENDPOINT : s3.amazonaws.com
- After your app is deployed, visit the `/admin` endpoint to login using the initial admin user you entered during config.

## Credit

Original from https://github.com/freekrai/directus-railway
