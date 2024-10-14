# UGA Library Database Project

# Team Name:
Query Crew

## Team Members
1. Harsh Patel 
2. Oliver Schouest 
3. Hormis Thaliath
4. Kevin Yin @kwy58676
5. Ishaan Nassar 

## Project Scenario

The UGA Library is modernizing its operations by creating a new database to efficiently track book inventory, student borrowing activities, staff operations, fines, and membership management. This system will streamline processes and provide valuable insights into resource usage and student needs.

### Key Entities:
- **Book**: Tracks ISBN, Title, Genre, Publication Date, and Associated Publisher.
- **Author**: Stores Author Details Including First Name, Last Name, and Date of Birth.
- **Student**: Captures Student ID, Name, and Major.
- **Staff**: Tracks Employee ID, Name, and Position.
- **Borrowing**: Monitors Student Borrowing History, Book Borrowed, and Return Date.
- **Fines**: Manages Student Fines, Including Amounts and Status (Paid or Unpaid).
- **Library Branch**: Locations of Library Branches.
- **Feedback**: Gathers Feedback From Students and Staff.
- **Membership**: Manages Membership Details Including Type, Start/End Dates, and Renewal Status.

## Data Model
<img width="394" alt="Screenshot 2024-10-13 at 10 42 08 PM" src="https://github.com/user-attachments/assets/1f45254a-7fcb-4b41-96b0-e63ab1d5f465">

## Data Dictionary
<img width="694" alt="Screenshot 2024-10-13 at 10 55 58 PM" src="https://github.com/user-attachments/assets/c97e804d-f758-4950-9cef-782adc3e966c">
<img width="639" alt="Screenshot 2024-10-13 at 10 57 10 PM" src="https://github.com/user-attachments/assets/23cc0e2d-7219-4509-8f09-fd44793fb0a6">

## SQL Queries

<img width="758" alt="Screenshot 2024-10-13 at 11 04 48 PM" src="https://github.com/user-attachments/assets/a69bd477-cc1e-4b1a-a680-e22afb198f7a">


Summary of the Queries' Complexity:
Complex Queries:
Most Borrowed Book by Genre,
Authors with the Most Books Borrowed,
Books Borrowed the Least Amount of Times,
Student Who Borrows the Most Books,
Overdue Books (Moderate),
Total Fines Collected by Each Branch (Moderate)

Simple Queries:
Total Fines Owed by Each Student,
Average Fine Amount per Student,
Number of Times Each Book Has Been Borrowed,
Number of Books Published by Each Publisher

Query 1: Overdue Books
This query shows all books that are overdue, including the book title, the student's name, and the return date. It helps the library track which books have not been returned on time and who has borrowed them.

<img width="633" alt="Screenshot 2024-10-13 at 10 46 09 PM" src="https://github.com/user-attachments/assets/b1ec084c-cb5c-462f-a369-d2c9cf171df3">

Query 2: Most borrowed book by genre
This query lists the most borrowed books in each genre. It helps the library understand which books are most popular with students, aiding in future acquisition decisions.

<img width="623" alt="Screenshot 2024-10-13 at 10 46 46 PM" src="https://github.com/user-attachments/assets/1d5f1d2c-4a90-412b-a206-ee08ab02e4e3">

Query 3: Total fines owed by each student
This query calculates the total unpaid fines for each student. It shows the student's name and the total amount they owe. This helps the library keep track of outstanding fines and follow up on them.

<img width="625" alt="Screenshot 2024-10-13 at 10 47 24 PM" src="https://github.com/user-attachments/assets/90afa6d5-cb12-486a-9c97-ce2c57c46cfd">

Query 4: Total fines collected by each branch
This query calculates the total amount of fines collected by each library branch. It helps the library track how much revenue is generated from fines at different locations, providing insight into usage patterns and payment behavior across branches.

<img width="625" alt="Screenshot 2024-10-13 at 10 47 53 PM" src="https://github.com/user-attachments/assets/8e06cb30-1599-481f-a177-b0db5558f381">

Query 5: Authors who have the most books borrowed
This query identifies the authors whose books have been borrowed the most. The library can use this information to understand which authors are most popular among students and readers.

<img width="624" alt="Screenshot 2024-10-13 at 10 48 23 PM" src="https://github.com/user-attachments/assets/3f4deba4-a5a1-4e75-b7b6-c4f589b06096">

Query 6: Average fine amount per student
This query calculates the average fine amount per student, providing insight into borrowing and returning behaviors. This information can help the library identify trends, such as frequent late returns, and design initiatives like reminders or extended return policies to minimize overdue fines and improve student satisfaction.

<img width="625" alt="Screenshot 2024-10-13 at 10 48 50 PM" src="https://github.com/user-attachments/assets/73e3ae9c-5e4c-4be4-9077-70c5bf175b83">

Query 7: Books borrowed the least amount of times
This query identifies the books that have been borrowed the fewest number of times. It counts how many times each book's ISBN appears in the borrowing table and returns the books with the lowest borrowing count. This helps the library keep track of what books are the least popular so they can make sure not to overstock certain books, or replace them with more popular titles. 

<img width="627" alt="Screenshot 2024-10-13 at 10 49 22 PM" src="https://github.com/user-attachments/assets/f1071b1a-f210-416f-9741-1cfeab4f4041">

Query 8: Student who borrows the most books
This query finds the student who has borrowed the most books. This information can be useful for understanding the interests and needs of frequent borrowers, offering them personalized recommendations, or targeting specific programs or events to highly active library users.

<img width="625" alt="Screenshot 2024-10-13 at 10 50 01 PM" src="https://github.com/user-attachments/assets/cf351d0b-2763-4d9f-807d-163c971cc3fc">

Query 9: Amount of times each book has been borrowed 
This query shows how many times each book has been borrowed by counting the number of times each book's ISBN appears in the borrowing table. It provides a ranked list of books based on their borrowing frequency, which can be used to guide purchasing decisions for additional copies, ensure availability of popular items, and help the library cater to trends in user interests.

<img width="625" alt="Screenshot 2024-10-13 at 10 50 30 PM" src="https://github.com/user-attachments/assets/f3e3c1e3-ec8d-4014-9f1f-a392765ba365">

Query 10: Number of books published by each publisher
This query calculates the total number of books in the library's collection that are associated with each publisher. It helps the library assess the contribution of different publishers to its collection and the diversification of materials from various publishing houses to meet the needs of the library’s users.

<img width="626" alt="Screenshot 2024-10-13 at 10 51 10 PM" src="https://github.com/user-attachments/assets/6511ff30-886a-43a5-bc11-c313541e6045">


## Database Information 

Name of the Database: cs_ots27622

Addional Informations: Each query listed above is marked in the database using stored procedures which can be called using the following format: cs_ots27622





