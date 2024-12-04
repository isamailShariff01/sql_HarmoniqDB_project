# sql_HarmoniqDB_project


HarmoniqDB 🎵
A MySQL-based database project designed to manage and analyze data for a music business. HarmoniqDB provides insights into employee performance, customer behavior, and regional revenue generation using SQL queries.

📋 Table of Contents
About the Project
Features
Technologies Used
Database Schema
Setup and Installation
Usage
Contributing
License
Contact



💡 About the Project
HarmoniqDB is a relational database system designed to handle music-related data, such as albums, artists, customers, invoices, and playlists. The project demonstrates database design and querying skills while providing actionable insights for the business.

✨ Features
Analyze employee hierarchy and seniority.
Identify countries with the highest number of invoices.
Determine cities with the most revenue.
Identify top customers based on spending.
Fetch top 3 highest-value invoices.


🛠️ Technologies Used
Database: MySQL
Tools: MySQL Workbench, phpMyAdmin
Language: SQL


🗂️ Database Schema
Main Tables:
Album: Stores album details.
Artist: Information about artists.
Customer: Customer details, including contact info and location.
Employee: Employee records, including hierarchy levels.
Genre: Music genres available.
Invoice: Purchase records with amounts and billing details.
Media_Type: Types of media formats available.
Playlist: Information about playlists.
Playlist_Track: Links tracks to playlists.


🚀 Setup and Installation
Prerequisites
Install MySQL Server.
Optionally, use MySQL Workbench for easier interaction.
Steps
Clone the repository:

bash
Copy code
git clone https://github.com/username/harmoniqdb.git  
Navigate to the project directory and open the SQL file.

Run the following commands in your MySQL client:

sql
Copy code
CREATE DATABASE HarmoniqDB;  
USE HarmoniqDB;  
Import the sql_harmoniqDB_project.sql file to populate the database.

📘 Usage
Example Queries
Use these queries to extract meaningful insights from the database:

Find the senior-most employee:

sql
1.Copy code
SELECT * FROM employee  
ORDER BY levels DESC;  
Country with the most invoices:

sql
2.Copy code
SELECT COUNT(*) AS invoice_count, billing_country  
FROM invoice  
GROUP BY billing_country  
ORDER BY invoice_count DESC;  
Top 3 highest invoice values:

sql
3.Copy code
SELECT TOP 3 total  
FROM invoice  
ORDER BY total DESC;  
City with the highest revenue:

sql
4.Copy code
SELECT TOP 1 SUM(total) AS invoice_total, billing_city  
FROM invoice  
GROUP BY billing_city  
ORDER BY invoice_total DESC;  
Best customer:

sql
5.Copy code
SELECT customer_id, SUM(total) AS total_spent  
FROM invoice  
GROUP BY customer_id  
ORDER BY total_spent DESC  
LIMIT 1;  


🤝 Contributing
Contributions are welcome! Follow these steps to contribute:

Fork the repository.
Create a new branch:
bash
Copy code
git checkout -b feature-name  
Commit your changes:
bash
Copy code
git commit -m "Add new feature"  
Push to the branch:
bash
Copy code
git push origin feature-name  
Open a pull request.

📞 Contact
Email : ismailshariff0103@gmail.com
GitHub: ismailshariff1
