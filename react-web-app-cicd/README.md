# Azure DevOps Pipeline for Building and Deploying React Web App

This repository contains an Azure DevOps pipeline configuration designed to build and deploy a react web application. The pipeline runs on a Windows environment and supports deployment to both development (DEV) and quality assurance (QA) environments.

## Pipeline Overview

The pipeline performs the following tasks:
1. **Install Node.js**: Sets up Node.js to the specified version.
2. **Install Dependencies and Build**: Installs necessary npm dependencies, builds the application, and prepares the build artifacts.
3. **Archive Build Artifacts**: Archives the build output into a ZIP file.
4. **Deploy to Azure App Service**: Deploys the ZIP file to an Azure Web App. The deployment target is determined by the specified environment (DEV or QA).

## Parameters

- **Deployment_Environment**: Specifies the environment to which the application will be deployed. It can be set to either `DEV` or `QA`. The default value is `DEV`.

## Steps Description

### 1. Install Node.js

Installs the specified version of Node.js required for building the application.

### 2. Install Dependencies and Build

Performs the following:
- Clears the npm cache.
- Installs dependencies with `npm install`.
- Installs the latest version of TypeScript.
- Builds the application using `npm run build`.

### 3. Archive Build Artifacts

Archives the build output directory into a ZIP file, which will be used for deployment.

### 4. Deploy to Azure App Service

Deploys the archived build artifacts to an Azure Web App. The deployment is based on the `Deployment_Environment` parameter:
- For **DEV**: Deploys to the development environment.
- For **QA**: Deploys to the quality assurance environment.

## Usage

1. **Set Up Your Azure DevOps Pipeline**: Add the `azure-pipelines.yml` file to the root of your repository.
2. **Configure Azure Subscription and Web App**: Replace placeholders in the pipeline configuration with your Azure subscription and Web App names.
3. **Run the Pipeline**: Trigger the pipeline manually or by pushing changes to the repository. Set the `Deployment_Environment` parameter as needed to deploy to either DEV or QA.
