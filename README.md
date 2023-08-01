# Deploy Directus On Railway

This example deploys a self-hosted version of [Directus](https://directus.io).

It uses a PostgreSQL database to store the data and S3 to store files.

[![Deploy directus on Railway](https://railway.app/button.svg)](https://railway.app/template/y5trbj)

## Services deployed

- Directus
- Postgres

## Requirement

- S3 bucket for file storage (persistence between deploys)

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

Original repo : [Original repo](https://github.com/freekrai/directus-railway)
