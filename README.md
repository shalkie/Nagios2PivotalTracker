# Nagios2PivotalTracker
Script(s) used by Nagios to talk to PivotalTracker

# Goal
There is no native method of posting alerts to PivotalTracker from Nagios. With the broader adoption of PivotalTracker and similiar tools it may be worth creating a tool to communicate with them similiar to a "real" ticketing system like RT.

# Language
Initial writting will be bash. A rewrite in python or RoR may be a follow up.

# Architecture
The application should have the following attributes:

* It should be stateless

	- The script will be executed everytime there is a state change or notification and should not rely on tracking things itself. The only thing it should retain are credentials for the API.
* It should be simple

	- KISS
* It should be service agnostic

	- It should be written to use PivotalTracker, Trello or Ajira
* It should be Pluggable

	- It should be broken down to bite sized pieces

