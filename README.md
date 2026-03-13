# DevOps Iniciante - GitHub Actions Lab: First Steps in CI/CD Automation

This repository contains the practical activities I performed to deepen my knowledge in **CI/CD pipelines**.
The goal of this lab was to understand how to automate the development workflow, from code checkout to the orchestration of multiple deploy stages (DEV, QA, HML, and PRD) via Yaml and GitHub Actions.

👉 Watch the free course by [Ieso Dias](https://www.linkedin.com/in/iesodias/) on Udemy: [DevOps para Iniciantes](https://www.udemy.com/course/devops-para-iniciantes-primeiros-passos-em-menos-de-2-horas/)

---

## Lab-01: GitHub Actions Overview

GitHub Actions is a **Continuous Integration (CI)** and **Continuous Delivery (CD)** platform that allows you to automate your development workflow directly within GitHub.

With it, you can:
* **Build** and **test** your code automatically.
* **Deploy** your applications to different environments.
* **Automate** routine tasks such as linting, code formatting, etc.

All of this from **YAML** files configured in your repository. Think of GitHub Actions as a "robot" that executes tasks for you whenever a condition (trigger) is met.

---

## Lab-02: First Workflow

In this lab, I created a basic workflow to understand the structure of a YAML file.

### Steps performed:
1. **Repository Creation:** `devops-iniciante`.
2. **Directory Structure:** Creation of the `.github/workflows/` folder.
3. **Workflow Configuration:** Creation of the files `mdc-workflow.yml` and `mdc-ci-cd-workflow.yml`.

---

## Lab-03: Multiple Stages (Jobs) and Dependencies
In this stage, the focus was on orchestration. I configured a pipeline that simulates a real software environment, where a job depends on the success of the previous one.

### What was implemented:
* Parallelism: The jobs `dev` and `qa` run at the same time after the build.
* Dependencies (needs): The `homologacao` job mandatorily waits for the success of `dev` AND `qa`.
* The `producao` job only starts after the completion of `homologacao`.

This lab is part of my learning path in DevOps practices and Platform Engineering.
