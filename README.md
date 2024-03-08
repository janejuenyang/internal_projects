# Project Template

This is a Template. On GitHub, click **Use this template** at the top right to create your own project based on this one.

This template repo is meant to provide a basic structure to help organize code, data, and reports related to a particular project for the ACF Data Surge Team.

This repo is set up to run as an app in a docker containter, although not required. It is currently set to `python` but you can change the language and the launch script.

## Project Checklist

Below is a checklist of items to work on for a project. This is to help you reference, stay organized and on top of the work. There's some upfront lift needed to scope and set up the project but the intent is that it flows smoothly and predictable for you afterwards.

Copy this checklist to a suitable location for your use. You can also edit the markdown file to check the individual boxes.

**Project Scoping Document Outline**

* [ ] Title
* [ ] Overview
* [ ] Objectives
* [ ] Scope and Approach
* [ ] Partnership Model
* [ ] Deliverables
* [ ] Timeline
* [ ] Assumptions
* [ ] Roles
* [ ] Revise, as needed

**Jira Project**

* [ ] Create Scrum Project
  * [ ] Use the following project title nomenclature: `ACF - <project name in ACF Confluence>`
  * [ ] For the Key, start with ACF and use the remainder of the first letters for each word on the title. Example: `ACFDS`
* [ ] Create Epics in timeline (think deliverables)
* [ ] Create Stories in backlog (think features/components of the deliverable)
* [ ] Create Tasks in backlog (think the tasks to complete Stories)
* [ ] Create Sprint (1 week)
* [ ] Create code review Tasks, as needed
* [ ] Assign Stories and Tasks to sprint and team members (weekly basis)
* [ ] Run Sprints weekly, move incomplete items to a new sprint
* [ ] Document as part of the sprints, it'll make things easier later
* [ ] Update status slide by Close of Business Thursdays (weekly)

**Meetings with Customers**

* [ ] Have an agenda (if customer hosted, propose one)
* [ ] Take meeting notes
* [ ] Take note of actions for you/team and for the customer
* [ ] Take note of completion dates for these actions
* [ ] Paste notes into Project Confluence page

**Project closeout**

* [ ] Finalize Documentation
* [ ] Finalize Code
* [ ] Finalize Visualizations
* [ ] Finalize Reports
* [ ] Capture Lessons Learned
* [ ] Project Brief, if needed
* [ ] Capture feedback through thought collector document and integrate to lessons learned
* [ ] Conduct internal retrospective discussion and integrate to lessons learned
* [ ] Provide Deliverables to customer
* [ ] Validate that all Deliverables are accepted by the customer
* [ ] Make changes to this repo and projects based on lessons learned, if any

## Coding Standards

Reference the [ACF Data Surge Team coding standards](https://github.com/HHS/acf-datasurge-standards/tree/feat/standards-version-1) for further details on coding practices.

## Requirements

To ensure app dependencies are ported from your virtual environment/host machine into your container, run the following command:

```bash
pip install pipreqs
```

Then run:

```bash
pipreqs --ignore .venv --scan-notebooks --force
```

If you encounter issues with connecting to pipy, you can change the server by adding the following: `--pypi-server <url>`

## Docker

I like running things in linux. Docker makes it standardized through configuration files like `.dockerignore`, `docker-compose.yml`, and `Dockerfile`.

You can delete the docker files along with the .vscode folder containing launch.json and tasks.json if they're not needed for the project.

### VSCode extension

Use the dockerextension to make it easy to change the programming language. Currently set as default for `python:3.12-slim`.

To change language version you can call the command pallete `CTRL + SHIFT + P` and select: `Docker: Add Docker Files to Workspace...`

### .dockerignore

This will ignore files and folders when building the container image.

### docker-compose

Use the following command to build and execute the docker container:

```bash
docker compose -f "docker-compose.yml" up -d --build
```

### Dockerfile

Contains all the necesary information to build a docker image with the application inside.
