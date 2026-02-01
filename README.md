Jenkins Continuous Integration Lab Project
Overview

This repository contains the implementation of a Continuous Integration (CI) setup using Jenkins, created as part of the Jenkins and Continuous Testing Lab Assignment.
The project demonstrates Jenkins installation, job configuration, multibranch pipelines, and plugin management.

The repository is integrated with Jenkins to automate builds and demonstrate CI workflows using both Freestyle Jobs and Multibranch Pipelines.

Technologies Used

Jenkins (LTS)

Java (JDK 17 / JDK 22)

Git & GitHub

Python

Jenkins Pipelines (Declarative)

Jenkins Plugins (Pipeline, SCM, Build Tools, Testing, Notification, Deployment)

Repository Structure
Devops-jobcreation/
├── Jenkinsfile
├── test.py
├── README.md

File Description

Jenkinsfile
Defines the declarative Jenkins pipeline with branch-based execution logic for:

main branch

feature/test branches

release/v1.0 branches

test.py
A simple Python script used in the Freestyle Jenkins job to demonstrate script execution during the build process.

README.md
Documentation for the GitHub repository.

Jenkins Jobs Configured
1. Freestyle Project

Connected to this GitHub repository using Git

Poll SCM enabled to check for changes every 5 minutes

Executes:

Windows batch commands

Python script (test.py)

Post-build actions:

Artifact archiving

Email notifications (documented)

JUnit test result publishing (documented)

2. Multibranch Pipeline

Automatically discovers branches from this repository

Uses a single Jenkinsfile for all branches

Branch-specific behavior:

main → Build, Test, Deploy

feature/test → Test only

release/v1.0 → Test and Security Scan

Branch indexing enabled for automatic job creation

Branches Used

main

feature/test

release/v1.0

These branches are used to demonstrate branch-based CI strategies using Jenkins Multibranch Pipelines.

Jenkins Plugin Usage

This project relies on Jenkins plugins from the following categories:

Pipeline and Blue Ocean plugins

SCM plugins (Git, GitHub, Subversion)

Build tools plugins (Maven, Gradle, Ant)

Testing plugins (JUnit, JaCoCo, Cobertura)

Notification plugins (Email Extension, Slack)

Deployment plugins (Docker, Kubernetes, SSH)

How This Repository Is Used in Jenkins

Jenkins connects to this GitHub repository

Source code is fetched automatically during builds

Jenkins executes jobs defined via UI (Freestyle) and code (Jenkinsfile)

Builds and pipelines are triggered automatically based on configuration

Academic Integrity

All configurations, scripts, and documentation in this repository are original and created solely for academic purposes as part of the CI Lab assignment.

Author

Anureet Kaur
CI Lab Assignment – Jenkins and Continuous Testing
