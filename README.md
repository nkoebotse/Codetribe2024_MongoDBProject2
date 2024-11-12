MongoDB Project: Codetribe Database
This README file outlines the MongoDB shell commands used to create and manage the Codetribe database, which contains three collections: Facilitators, Trainees, and Projects. It also provides instructions on how to start the MongoDB shell (Mongosh) and interact with the database effectively.

Prerequisites
MongoDB installed on your system
Mongosh (MongoDB Shell) installed and available in your terminal
Starting the MongoDB Shell (Mongosh)
Open your terminal or command prompt.
Run the following command to start the MongoDB shell:

mongosh
This will open the MongoDB shell and connect to your MongoDB instance.
Steps to Create the Database and Collections
1. Create a Database: Codetribe
To create a new database named Codetribe, run the following command:

javascript

use Codetribe
This will create the Codetribe database if it doesn't already exist and switch the current context to that database.

2. Create the Collections: Facilitators, Trainees, and Projects
MongoDB creates collections automatically when you insert documents into them. To create the required collections, you will insert documents into each of them.

Collection 1: Facilitators
To create a collection named Facilitators and insert a document with the specified fields (Name, Location, Course), use the following command:

javascript

db.Facilitators.insertOne({Name:"elliot",Location:"Polokwane",Course:"IT"})
Collection 2: Trainees
To create a collection named Trainees and insert a document with the specified fields (Name, Location, Facilitator), use the following command:

javascript

db.Trainees.insertOne({Name:"monae",Location:"Polokwane",Facilitator:"elliot"})
Collection 3: Projects
To create a collection named Projects and insert a document with the specified fields (Name, Course, Lesson), use the following command:

javascript

db.Projects.insertOne({Name:"mongoDb",Course:"IT",Lesson:"2 activity 2"})
3. Verify Data Insertion
To confirm that the data was inserted successfully into each collection, you can run the following commands to view the documents in each collection:

For Facilitators:
javascript

db.Facilitators.find().pretty()
For Trainees:
javascript

db.Trainees.find().pretty()
For Projects:
javascript

db.Projects.find().pretty()
![mongoDb](https://github.com/user-attachments/assets/cdde9926-3569-430c-9fd5-310ffcc6f4d3)
