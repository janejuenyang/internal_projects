# Project Outline

This repo is meant to provide a basic template to help organize code, data, reports related to a particular project.

This repo is set up to run as an app in a docker containter. It is currently set to `python` but you can change the language and the launch script.

## Project Checklist

Project Scope

* [ ] Overview
* [ ] Objectives
* [ ] Scope and Activities
* [ ] Deliverables and Timeframes
* [ ] Assumptions
* [ ] Stakeholders
* [ ] Revise, if needed

Jira Project

* [ ] Create Scrum Project
* [ ] Create Epics (think deliverables)
* [ ] Create Stories in backlog (think features, components)
* [ ] Create Tasks in backlog (think tasks to complete Stories)
* [ ] Create Sprint (1 week)
* [ ] Assign Stories and Tasks to sprint and team members (weekly)
* [ ] Run Sprints weekly, move incomplete items to a new sprint
* [ ] Document as part of the sprints, it'll make things easier
* [ ] Update status slide (weekly)

Meetings with Customer

* [ ] Have an agenda (if customer hosted, propose one)
* [ ] Take meeting notes
* [ ] Take note of actions for you/team and for customer
* [ ] Take note of completion dates for these actions

Project closeout

* [ ] Finalize Documentation
* [ ] Finalize Code
* [ ] Finalize Visualizations
* [ ] Finalize Reports
* [ ] Capture Lessons Learned
* [ ] Project Brief (if needed)
* [ ] Capture feedback through thought collector document and integrate to lessons learned
* [ ] Conduct internal retrospective discussion and integrate to lessons learned
* [ ] Make changes to this repo and projects based on lessons learned if any

## Requirements

To ensure app dependencies are ported from your virtual environment/host machine into your container, run:

```bash
pip install pipreqs
```

then:

```bash
pipreqs --ignore .venv --scan-notebooks --force
```

## Docker

I like running things in linux. Docker makes it standardized through configuration files like `.dockerignore`, `docker-compose.yml`, and `Dockerfile`.

### VSCode extension

Use the dockerextension to make it easy to change the programming language. Currently set as default for `python:3.12-slim`.

To change language version you can call the command pallete `CTRL + SHIFT + P` and select: `Docker: Add Docker Files to Workspace...`


### .dockerignore

This will ignore files and folders when building the container image.

### docker-compose

Use to build and execute the docker container from the image.

```bash
docker compose -f "docker-compose.yml" up -d --build
```

### Dockerfile

Contains all the necesary information to build a docker image.
