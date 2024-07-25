# .NET Core Web APP CI/CD Pipeline

This pipeline builds and deploys a .NET Core Web APP using Azure DevOps.

## Pipeline Overview

1. **Use .NET Core SDK**: Ensures the required .NET Core SDK is used.
2. **NuGet Restore**: Restores NuGet packages.
3. **Build Solution**: Builds the .NET solution.
4. **Publish**: Publishes the build output.
5. **Deploy to Azure App Service**: Deploys the build artifact to Azure App Service based on the selected environment.

## Files
- `azure-pipelines.yml`: The pipeline configuration file.

## Setup Instructions

1. Ensure you have an Azure DevOps project.
2. Add the pipeline by linking `azure-pipelines.yml`.
3. Set up Azure service connections for both DEV and QA environments.
4. Update `azure-pipelines.yml` as necessary for your project structure.
