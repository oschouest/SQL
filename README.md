# UGA Library Database Project

# Team Name:
Query Crew

## Team Members
1. Harsh Patel
2. Oliver Schouest
3. Hormis Thaliath
4. Kevin Yin
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

Our database supports tracking of student and staff information, book inventory, borrowing history, and fines, all linked to library branches and feedback for continuous improvement.

![Data Model](data_model.png)

## Data Dictionary
<img width="694" alt="Screenshot 2024-10-11 at 1 46 25 PM" src="https://github.com/user-attachments/assets/c4c5ac1d-df87-4e6b-81e1-7c2ed5c99416">
<img width="694" alt="Screenshot 2024-10-11 at 1 51 23 PM" src="https://github.com/user-attachments/assets/653ff6b9-ce2b-4a3b-a8b0-ea76aa6cae66">


## SQL Queries
Total fines collected by each branch

SELECT m.Branch_Name, SUM(f.Amount) AS Total_Fines 
FROM Fines f 
JOIN Student s ON f.Student_ID = s.Student_ID 
JOIN Memberships m ON s.Student_ID = m.Student_ID 
WHERE f.Status = 'Paid' 
GROUP BY m.Branch_Name 
ORDER BY Total_Fines DESC;

Authors who have the most books borrowed

SELECT a.First_Name, a.Last_Name, COUNT(b.ISBN) AS Total_Borrowed 
FROM Authors a 
JOIN Book_Authors ba ON a.Author_ID = ba.Author_ID 
JOIN Book b ON ba.ISBN = b.ISBN 
JOIN Borrowing br ON b.ISBN = br.ISBN 
GROUP BY a.Author_ID, a.First_Name, a.Last_Name 
ORDER BY Total_Borrowed DESC;

Most borrowed books by genre

SELECT bc.Genre, bk.Title, COUNT(br.Borrowing_ID) AS Borrow_Count 
FROM Borrowing br 
JOIN Book bk ON br.ISBN = bk.ISBN 
JOIN Book_Category bc ON bk.ISBN = bc.Book_ID 
GROUP BY bc.Genre, bk.Title 
ORDER BY bc.Genre, Borrow_Count DESC;

Average fine amount per student

SELECT s.Student_ID, s.First_Name, s.Last_Name, AVG(f.Amount) AS Average_Fine 
FROM Student s 
JOIN Fines f ON s.Student_ID = f.Student_ID 
GROUP BY s.Student_ID, s.First_Name, s.Last_Name 
ORDER BY Average_Fine DESC;

