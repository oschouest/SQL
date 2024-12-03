# UGA Library Database Project

# Team Name:
Query Crew

## Team Members
1. Harsh Patel @03harshp
2. Oliver Schouest @oschouest 
3. Hormis Thaliath @Hormist
4. Kevin Yin @kwy58676
5. Ishaan Nassar @inn923

## Project Scenario

The UGA Library is modernizing its operations by creating a new database to efficiently track book inventory, student borrowing activities, staff operations, fines, and membership management. This system will streamline processes and provide valuable insights into resource usage and student needs.

### Key Entities:
- **Book**: Tracks ISBN, Title, Genre, Publication Date, and Associated Publisher.
- **Author**: Stores Author Details Including First Name, Last Name, and Date of Birth.
- **Student**: Captures Student ID, Name, and Major.
- **Publishers**: Branch ID, Branch Name, and location
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
Branches with Most Borrowed Books
Who are the Top Borrowers
Revenue Forecast by Membership Type
Feedback Analysis by Branch
Popular Genres by Borrowing

Query 1: Branches with Most Borrowed Books

This query shows all books that are overdue, including the book title, the student's name, and the return date. It helps the library track which books have not been returned on time and who has borrowed them.


Query 2: Who are the Top Borrowers

This query lists the most borrowed books in each genre. It helps the library understand which books are most popular with students, aiding in future acquisition decisions.

<img width="398" alt="Screenshot 2024-12-03 at 5 46 34 PM" src="https://github.com/user-attachments/assets/cf05232d-e71a-4974-96c5-7f2c8e077e03">

Query 3: Revenue Forecast by Membership Type

This query estimates potential revenue based on the number of Regular and Premium memberships. The memberships table provides the foundation for this calculation. With this data, we can see how different membership tiers contribute to overall revenue and target specific branches for membership campaigns. This is crucial for financial planning and identifying opportunities to boost membership-driven revenue.
<img width="383" alt="Screenshot 2024-12-03 at 5 46 49 PM" src="https://github.com/user-attachments/assets/2a899927-dabf-404d-b6a3-e4fe3a117358">

Query 4: Feedback Analysis by Branch

This query analyzes user feedback by branch and type (e.g., complaints, praise, or suggestions). It joins the feedback and branches tables.The results help pinpoint branches with higher complaint rates, allowing us to address specific issues.For example, a branch with many complaints about noise levels may need stricter quiet zone policies, while branches with high praise can serve as models for others.
<img width="304" alt="Screenshot 2024-12-03 at 5 47 01 PM" src="https://github.com/user-attachments/assets/16da4417-7908-4018-86b7-c8f893210774">

Query 5: Popular Genres by Borrowing

This query identifies the most borrowed book genres by joining the books, bookCategories, and borrowings tables. The results highlight popular genres, which helps optimize collection development. It ensures that the library invests in books that align with user preferences. This insight can also inform marketing efforts, such as genre-specific reading challenges or book club promotions.
<img width="285" alt="Screenshot 2024-12-03 at 5 47 13 PM" src="https://github.com/user-attachments/assets/e81ceffc-0566-4cf9-a61f-80b3cbefb48d">


Visualization 1:

Visualization 2:

Visualization 3:



## Database Information 

Name of the Database: cs_ots27622

Addional Informations: Each query listed above is marked in the database using stored procedures which can be called using the following format: cs_ots27622





