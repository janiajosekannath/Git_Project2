# CI/CD Pipeline Basics PROJECT 3

## Project Overview

This project was completed as part of the DecodeLabs DevOps Internship Program. The goal of the project is to understand the fundamentals of Continuous Integration and Continuous Deployment (CI/CD) by creating an automated workflow using GitHub Actions.

## Objectives

- Learn the concepts of CI/CD.
- Understand workflow automation.
- Create a GitHub Actions workflow.
- Automate tasks on code push events.
- Monitor and analyze workflow execution.

## Technologies Used

- Git
- GitHub
- GitHub Actions
- Ubuntu (WSL)

## Workflow Features

The workflow performs the following actions:

- Triggered automatically on push to the main branch.
- Checks out repository contents.
- Displays a confirmation message.
- Displays system date and time.
- Lists repository files and directories.

## Workflow File

Location:

```text
.github/workflows/ci.yml


SAMPLE WORKFLOW

name: CI Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Display Message
        run: echo "CI/CD Pipeline Executed Successfully"

      - name: Show Date
        run: date

      - name: List Files
        run: ls -la
