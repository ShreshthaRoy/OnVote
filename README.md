Online Voting Management System:

A database-driven Online Voting Management System developed using MySQL to manage voters, candidates, elections, and voting records efficiently. The project demonstrates how relational database concepts can be applied to create a structured and reliable voting system.

Project Overview:

The Online Voting Management System provides a simple database structure for conducting and managing elections digitally. It maintains information about registered voters, candidates, elections, and votes while using SQL constraints to maintain data consistency and prevent duplicate voting.

The system can be used as a foundation for applications such as student elections, organizational elections, association voting, and other controlled voting environments.

Objectives:
Maintain voter information in a structured database.
Store candidate details such as name, party, and symbol.
Manage multiple elections and their statuses.
Record votes securely using relational database constraints.
Prevent a voter from casting more than one vote.
Generate useful election reports using SQL queries.
Demonstrate practical use of primary keys, foreign keys, unique constraints, and SQL operations.
🛠️ Technologies Used
MySQL – Database management
SQL – Database creation, manipulation, and querying
phpMyAdmin / MySQL Workbench – Database interface


Database Structure:

The system consists of four main tables:

1. voters

Stores information about registered voters.

Column	Description
voter_id	Unique ID of the voter
name	Voter's name
age	Voter's age
email	Voter's email address
has_voted	Indicates whether the voter has voted
2. candidates

Stores information about election candidates.

Column	Description
candidate_id	Unique candidate ID
name	Candidate's name
party	Candidate's party
symbol	Candidate's election symbol
3. elections

Stores information about different elections.

Column	Description
election_id	Unique election ID
title	Election title
year	Election year
status	Current election status
4. votes

Stores the votes cast by voters.

Column	Description
vote_id	Unique vote ID
voter_id	ID of the voter
candidate_id	ID of the selected candidate
election_id	ID of the election

The votes table uses foreign keys to connect voters, candidates, and elections.

Database Constraints:

The project uses several SQL constraints to maintain data integrity:

Primary Keys uniquely identify records.
Foreign Keys establish relationships between tables.
UNIQUE constraint on voter_id prevents the same voter from being entered into the votes table more than once.
DEFAULT FALSE is used for has_voted, indicating that a voter has not voted initially.
AUTO_INCREMENT automatically generates unique IDs.
⚙️ How the System Works
Step 1: Create the Database

Create a database in MySQL or phpMyAdmin and execute the table creation queries.

Step 2: Add Voters

Voter records can be inserted into the voters table.

Step 3: Add Candidates

Candidate information is stored in the candidates table.

Step 4: Create an Election

An election can be added to the elections table with its title, year, and current status.

Step 5: Cast a Vote

When a voter casts a vote, their voter ID, selected candidate ID, and election ID are stored in the votes table.

The voter's has_voted status can then be updated to TRUE.

Step 6: Generate Reports

SQL queries can be used to determine:

Total votes received by each candidate.
Voters who have already voted.
Voters who have not yet voted.
Election participation information.
