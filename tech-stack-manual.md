# Tech Stack Manual

## 1. Run Questions

### 1a. Config Files

| Config File | Location                 | Config Value                 | What it's for                                                            | How it's used                                                                                                         |
| ----------- | ------------------------ | ---------------------------- | ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| .env        | learn-ops-api            | database connections strings | secret files                                                             | stores data used to configure a software system such as an application, a server or an operating system               |
| .gitignore  | learn-ops-api            | file name, folder names      | not pushing in github                                                    | store file name folder name such as application, aserver or an operating system                                       |
| Makefile    | learn-ops-infrastructure | settings veriables           | to automatically compile and build executable programs from source code. | stores settings veriables used to configure a software system such as an application, a server or an operating system |

### 1b. How to Start It

Makefile contents vary completely by project, the specific commands depend on your repository.
SHELL := /usr/bin/env bash

for system running the commands are setup, doctor, teardown, up, up-api, up-client-api, down, log, restart,
ps and reset

### 1c. Where to Access It

| Service.       | Port | URL                    |
| -------------- | ---- | ---------------------- |
| custom_logging | 8080 | https://api.github.com |
| messaging      | 8080 | https://api.github.com |
| monitoring.    | 8080 | https://api.github.com |

### 1d. Service Dependencies

| Service       | Depends On | Why                                  |
| ------------- | ---------- | ------------------------------------ |
| config        | database   | to get the secret settings           |
| custom_loggin | database   | to get the custom data               |
| notifications | API        | to read and write notification data. |

### 1e. Main Entry Points

| Service        | Startup File    | Routes / URL Config File |
| -------------- | --------------- | ------------------------ |
| config         | settings.py     | https://api.github.com   |
| custom_logging | log_retriver.py | https://api.github.com   |
| notifications  | notifier.py     | https://api.github.com   |

---

## 2. Services

| Service Name    | Tech Stack (including version) | Purpose                                   |
| --------------- | ------------------------------ | ----------------------------------------- |
| service-monarch |                                | for simply and Easier Debugging & Tracing |

---

## 3. System Overview

The Learning Platform is a full-stack Learning Management System (LMS) built specifically for Nashville Software School, a software development bootcamp. It solves the operational problem of running a cohort-based technical education program at scale: tracking where each student is in the curriculum, managing the structured groups (cohorts) they learn in, and automating the repetitive GitHub and Slack work that instructors would otherwise do by hand for every project. Without a system like this, instructors would need to manually create dozens of GitHub repositories, copy issue tickets across repos, and send individual Slack messages every time a new project phase begins — tasks that the platform automates end-to-end.

From a user's perspective, the platform centres on curriculum and cohort management. Instructors can create courses made up of books (curriculum modules) and projects, then assign those courses to cohorts of students. When a project is ready to begin, the platform automatically creates a GitHub repository for each student team, adds the students as collaborators, copies the project's issue tickets from the instructor's template repository into each team's repo via the Monarch service, and sends a Slack notification to the cohort channel — all triggered by a single action. Students log in using their existing GitHub account through OAuth, so there is no separate credential to manage. The platform also tracks student progress through assessments and provides instructors with a searchable view of where every student stands across the cohort.

The system has two distinct user roles that interact with it differently. Instructors are the primary power users: they manage the full lifecycle of a cohort, from setting up courses and books to creating student teams and monitoring progress. They have elevated permissions (`is_staff` and the Instructors group) and access to the Django admin panel as a back-office tool. Students interact with a narrower slice of the application — they can view their own progress, access course materials, and see their team's project details, but cannot create or modify cohort-level data. A superuser (local admin) also exists for system-level operations like running database management tasks directly through the Django admin interface.
