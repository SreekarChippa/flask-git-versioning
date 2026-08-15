# Flask Voting Application

## Project Title and Description

This project is a simple voting application built with Python and Flask. Users can
vote for candidates by visiting a URL, and the application keeps track of the votes.
The current voting results can be viewed at any time. The application also provides
a reset feature that clears all stored votes.

The project was developed using Git version control with separate `dev` and `main`
branches. New features were developed and tested on `dev` before being released
to the stable `main` branch.


## Installation and Setup

1. Clone the repository

Open a terminal and run:
git clone https://github.com/SreekarChippa/flask-git-versioning.git

2. Move into the project directory
cd flask-git-versioning

3. Install Flask
python -m pip install flask

4. Run the application
python app.py

The application will start on: http://localhost:5000

# API Endpoint Reference
Endpoint	Method	Description	Example Response
/	        GET	    Displays the welcome message.	Welcome to the App
/health	    GET	    Checks whether the application is running.	App is running
/vote/<name>GET	    Records one vote for the specified candidate.	Vote recorded for Alice
/results	GET	    Returns the current vote counts for all candidates in JSON format.	{"Alice": 2, "Bob": 1}
/reset  	GET	    Clears all stored vote counts.	Votes have been reset


# Git Workflow

This project uses two Git branches:
dev - Used for development and testing.
main - Used only for stable and working code.

All new development was performed on the dev branch. Once a feature was completed
and tested successfully, the changes were merged into main.
# The workflow was:
                 +----------------+
                 |      dev       |
                 | Development    |
                 +-------+--------+
                         |
                         | Develop feature
                         | Test feature
                         |
                         v
                 +----------------+
                 | Feature works  |
                 +-------+--------+
                         |
                         | Merge
                         v
                 +----------------+
                 |      main      |
                 | Stable release |
                 +----------------+

# The same process was followed for each version

# Version 1
dev
 ↓
Develop Flask application
 ↓
Test / and /health
 ↓
Merge dev → main
 ↓
Version 1 released

# Version 2

dev
 ↓
Add voting functionality
 ↓
Test voting and results
 ↓
Add reset functionality
 ↓
Test reset
 ↓
Merge dev → main
 ↓
Version 2 released

## This workflow ensured that the main branch contained stable and working code only.


# Version	Features
Version 1	Created the basic Flask application with / and /health endpoints. Set up Git version control using dev and main branches.
Version 2	Added the voting functionality with /vote/<name> and /results. Added /reset to clear all stored votes.

# Attached the screenshots for reference

# Project Structure 
flask-git-versioning/
│
├── app.py
├── README.md
└── screenshots/
    ├── browser.png
    ├── appHealth.png
    ├── voting.png
    ├── results.png
    ├── reset.png
    └── resultsAfterReset.png