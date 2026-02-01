Jenkins Continuous Integration Lab Project

Overview
This repository contains the implementation of a Continuous Integration (CI) setup using Jenkins, created as part of the Jenkins and Continuous Testing Lab Assignment.
The project demonstrates Jenkins installation, job configuration, multibranch pipelines, and plugin management.

Technologies Used
Jenkins (LTS)
Java (JDK 17 / JDK 22)
Git and GitHub
Python
Jenkins Pipelines (Declarative)

Repository Contents
Jenkinsfile – Defines the Jenkins pipeline with branch-based execution logic
test.py – Python script executed in the Freestyle Jenkins job
README.md – Repository documentation

Jenkins Jobs Configured

Freestyle Project
The Freestyle job is connected to this GitHub repository using Git.
It executes Windows batch commands and a Python script during the build process.
Post-build actions include artifact archiving, email notification configuration, and JUnit test result publishing (documented).

Multibranch Pipeline
The Multibranch Pipeline automatically discovers branches from this repository.
A single Jenkinsfile is used to define pipeline behavior.
Branch-specific execution is implemented as follows:
main branch – Build, Test, Deploy
feature branches – Test only
release branches – Test and Security Scan

Branches Used
main
feature/test
release/v1.0

Jenkins Plugins
This project uses Jenkins plugins from the following categories:
Pipeline plugins
SCM plugins
Build tools plugins
Testing plugins
Notification plugins
Deployment plugins

How This Repository Is Used
Jenkins connects to this GitHub repository to fetch source code automatically.
Jobs are executed using both Freestyle configuration and Jenkinsfile-based pipelines.

Academic Integrity
All configurations and scripts in this repository are original and created for academic purposes.

Author
Anureet Kaur
CI Lab Assignment – Jenkins and Continuous Testing
