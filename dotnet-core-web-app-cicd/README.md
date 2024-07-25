# .NET Core Web APP CI/CD Pipeline

This pipeline contains an Azure DevOps pipeline configuration for building and deploying a .NET Core Web App. The pipeline supports deployment to both development (DEV) and quality assurance (QA) environments.

## Pipeline Overview

The pipeline performs the following tasks:
1. Checks out the code from the repository.
2. Sets up the .NET Core SDK.
3. Restores NuGet packages.
4. Builds the solution.
5. Publishes the build artifacts.
6. Deploys the published artifacts to an Azure Web App, based on the selected deployment environment.

## Parameters

- **Deployment_Environment**: Specifies the deployment environment. It can be set to either `DEV` or `QA`. The default value is `DEV`.

## Steps Description

### 1. Checkout

Checks out the source code from the repository to ensure the latest version is used.

### 2. Use .NET Core SDK

Sets up the .NET Core SDK to the specified version (8.x in this case).

### 3. NuGet Restore

Restores the required NuGet packages for the solution.

### 4. Build Solution

Builds the solution in the Release configuration. This step ensures that all code is compiled and ready for deployment.

### 5. Publish Artifacts

Publishes the build artifacts to a staging directory. These artifacts are the files that will be deployed to the Azure Web App.

### 6. Deploy to Azure Web App

Deploys the published artifacts to an Azure Web App. The deployment is controlled by the `Deployment_Environment` parameter:

- For **DEV** environment, it deploys to the DEV Web App.
- For **QA** environment, it deploys to the QA Web App.

## Usage

1. **Set Up Your Azure DevOps Pipeline**: Add the `azure-pipelines.yml` file to the root of your repository.
2. **Configure Azure Subscription**: Replace `<AzureSubscriptionName>` with your Azure subscription name or service connection.
3. **Configure Web App Names**: Replace `<YourDevWebAppName>` and `<YourQaWebAppName>` with the names of your Azure Web Apps for DEV and QA environments, respectively.
4. **Run the Pipeline**: Trigger the pipeline manually or by pushing changes to the repository.

