Neoitek Systems Automated Timesheet Management System
A complete web-based employee timesheet and HR management platform for Neoitek Systems

Project Overview

The Neoitek Systems Automated Timesheet Management System (ATMS) is a Django-powered web application designed to streamline employee time tracking and HR workflows.
The platform allows employees to log their working hours daily or weekly, view past submissions, and monitor project-level productivity.
Meanwhile, HR and management teams can review submissions, approve or reject timesheets, manage employee records, and generate performance insights.

Built with scalability and efficiency in mind, ATMS can evolve into a full-featured HR and workforce management suite for Neoitek Systems and its clients.

Tech Stack
Layer	Technology
Frontend	HTML, CSS, JavaScript
Backend	Python (Django Framework)
Database	SQLite (Local), PostgreSQL (Cloud)
Server	Gunicorn (for Production)
Hosting	Render
Version Control	Git + GitHub
Editor	PyCharm IDE

Setup Guide (From Scratch)
This guide explains how any team member (developer, tester, or admin) can set up and run the Neoitek ATMS project locally.

Step 1: Install Python
Visit https://www.python.org/downloads
Download the latest stable version (Python 3.11 or higher)
During installation:
Check “Add Python to PATH”
Then click Install Now

Verify installation:
python --version
You should see something like Python 3.11.9.

Step 2: Install PyCharm
Download from https://www.jetbrains.com/pycharm/download
Choose Community Edition (Free)
Complete the setup and open PyCharm after installation.

Step 3: Install Git
Download from https://git-scm.com/downloads
Install with default options.
Configure user identity:
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

Step 4: Clone the Project from GitHub

Visit the Neoitek Systems GitHub repo:  https://github.com/NeoitekSystems/Neoitek_Systems_Automated_Timesheets_Management_System.git
Copy the HTTPS clone link.

In PyCharm, click:
Get from VCS → paste the repo link → choose a local folder → Clone

Step 5: Create and Activate Virtual Environment
For Windows:
python -m venv .venv
.venv\Scripts\activate

For Mac/Linux:
python3 -m venv .venv
source .venv/bin/activate


You’ll know it’s active when your terminal shows:

(.venv)

Step 6: Install Dependencies
pip install -r requirements.txt


This installs Django, Gunicorn, and all necessary dependencies.

Step 7: Run the Project Locally
python manage.py runserver


Open your browser and visit:
http://127.0.0.1:8000/

You’ll now see the Neoitek Timesheet Portal running locally.

Step 8: Stop the Server

Press CTRL + C in your terminal to stop it.

Team Workflow
Branching Strategy
Neoitek follows a six-stage professional branching model to ensure clean CI/CD pipelines.

Branch	Purpose
feature	Developers build new features or bug fixes here
dev	Developer integration and testing branch
test	QA verification branch
cicd	Continuous Integration / Deployment verification
pre-prod	Final pre-production validation
main	Stable production-ready branch (connected to Render deployment)

Developer Flow
# Switch to latest dev
git checkout dev
git pull origin dev

# Create your new feature branch
git checkout -b feature-login-page

# Make your changes and test locally
python manage.py runserver

# Add and commit
git add .
git commit -m "Added new login page for Neoitek portal"

# Push to GitHub
git push -u origin feature-login-page

Then create a Pull Request (PR) → target the dev branch.
Once reviewed and approved → merged into dev.
QA / Testing Flow
git checkout test
git pull origin test

Validate features merged from dev
Report issues or confirm for merge
Once approved → ready for cicd testing

CI/CD Flow
The CI/CD engineer:
Merges from test → cicd
Verifies automated build/deploy pipelines
If stable → merges into pre-prod
After PM approval → merges into main

Automatic Deployment
Render is connected to the main branch.
Every time new code is merged into main, Render automatically:

Builds the Django project
Runs migrations
Collects static files
Deploys the live web application

Production URL:
https://neoitek-automated-timesheets.onrender.com

Common Commands
Task	Command
Create virtual environment	python -m venv .venv
Activate environment	.venv\Scripts\activate
Install dependencies	pip install -r requirements.txt
Run Django server	python manage.py runserver
Make migrations	python manage.py makemigrations
Apply migrations	python manage.py migrate
Collect static files	python manage.py collectstatic
Commit changes	git add . && git commit -m "message"
Push changes	git push origin branch-name

Team Roles
Role	Responsibilities
Developers	Build new features, fix bugs, create feature branches, and raise PRs to dev
Testers	Verify new features in test branch and confirm stability
CI/CD Engineer	Manage deployments and automated builds from cicd → pre-prod → main
HR / PM	Review progress, approve merges to production, and monitor overall system health

Summary
This documentation ensures every Neoitek Systems contributor — developer, tester, or CI/CD admin — can:
Set up the project locally
Follow a clean Git branching strategy
Safely deploy through CI/CD
Maintain the live production system seamlessly.

© 2025 Neoitek Systems Inc.
All rights reserved. Empowering digital innovation through technology.
