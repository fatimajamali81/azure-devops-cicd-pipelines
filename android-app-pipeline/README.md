# Azure DevOps Pipeline for Building and Deploying Android App with Fastlane

This repository contains an Azure DevOps pipeline configuration for building and deploying an Android app using Fastlane. The pipeline runs on macOS and publishes the generated APK as a build artifact.

## Pipeline Overview

The pipeline performs the following tasks:
1. Sets up the Ruby environment.
2. Installs Fastlane using Bundler.
3. Builds the APK using Fastlane.
4. Publishes the APK as a build artifact.

## Fastlane Overview

The Fastfile contains a lane that builds and packages the Android APK. Fastlane simplifies Android development tasks by automating the build process.

## Pipeline Configuration

### 1. Pool

Specifies the VM image to use for the pipeline. In this case, macOS 13.

### 2. Variables

Defines the Fastlane version to use.

### 3. Steps

#### Set up Ruby Environment

Sets up the Ruby environment with the specified version.

#### Install Fastlane

Installs Bundler and Fastlane, and sets up the Fastlane environment.

#### Build APK

Uses Fastlane to build the APK.

#### Publish APK Artifact

Publishes the generated APK as a build artifact.

## Fastfile Configuration

The Fastfile defines the build process for the Android APK using Fastlane.

### Platform

Specifies the default platform as Android.

### Lane

Defines the `build_apk` lane, which:
1. Installs npm dependencies.
2. Runs the Gradle `assembleRelease` task to build the APK.

## Usage

1. **Set Up Your Azure DevOps Pipeline**: Add the `azure-pipelines.yml` file to the root of your repository.
2. **Configure Ruby and Fastlane**: Ensure the specified Ruby version (`>= 2.6`) and Fastlane version (`2.200.0`) are compatible with your environment.
3. **Run the Pipeline**: Trigger the pipeline manually or by pushing changes to the repository.
