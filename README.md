# Azure DevOps Pipelines Collection

This repository contains a collection of Azure DevOps yaml pipelines, most of which are cicd pipelines for different types of applications:
1. **Android Mobile Application** - Using Fastlane for APK build and Azure DevOps for CI/CD.
2. **React Web Application** - Using Node.js for build and Azure DevOps for CI/CD.
3. **.NET Core Web API** - Using .NET Core SDK for build and Azure DevOps for CI/CD.

## Directory Structure
- `android-app-pipeline`: Contains the pipeline for building and deploying an Android application.
- `react-web-app-cicd`: Contains the pipeline for building and deploying a React web application.
- `dotnet-core-web-app-cicd`: Contains the pipeline for building and deploying a .NET Core Web API.

Each directory has its own detailed `README.md` with setup instructions and pipeline details.

## How to Use
1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/azure-devops-cicd-pipelines.git
    cd azure-devops-cicd-pipelines
    ```
2. Navigate to the desired pipeline directory and follow the instructions in the `README.md` file for setting up and using the pipeline.

## License
This project is licensed under the MIT License.
