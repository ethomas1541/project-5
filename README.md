Elijah Thomas ethomas7@uoregon.edu

CS 322 Project 5

From Project 4:

	Calculator for ACP Brevet open and close times based on:

		https://rusa.org/pages/acp-brevet-control-times-calculator

	Provides quick, refresh-less updates for each row in a table based on user input. The last 3 columns of the chart
	are extrapolated from user input. Requests are handled with AJAX and sent to a rudimentary Flask-based server.

	-	Frontend: 					brevets/templates/calc.html
	-	Web server: 				brevets/flask_brevets.py
	-	Backend:					brevets/acp_times.py

	Comments in each of these files provide much further detail.

New in Project 5:

	- MongoDB container, running in parallel, on port 27017
	- Two new AJAX requests present in the frontend and backend files from above
	- In essence, frontend has a sort of indirect, full-duplex communication system with a MongoDB database that stores its form data in a dictionary-like structure

	- Issues with "overflows" in my project 4 implementation have been solved, and unit tests have been updated, though they are not present in this repository

	- brevets/tests now contains a single Python file, test_db.py, that requires a running instance of MongoDB on port 27017, and passes all tests to the best of my knowledge. Granted, the tests are fairly pedestrian and demonstrate basic functionality

	- pymongo added to requirements.txt (obviously)