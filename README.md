
```markdown
# School Database Project

This project involves creating and managing a School Database using SQLite. The database consists of two main tables: `Course` and `Student`, where the `Student` table has a foreign key relationship with the `Course` table. This project demonstrates essential database operations such as table creation, data insertion, and performing complex queries using SQL.

## Description

The purpose of this project is to provide hands-on experience with relational database concepts and SQL queries. By working through this task, you will learn how to:
- Design and create relational database tables.
- Establish relationships between tables using foreign keys.
- Insert data into tables.
- Execute SQL queries to retrieve specific information from the database.

## Why This is Important

Understanding relational databases and SQL is crucial for any developer because:
- Databases are the backbone of most applications, enabling efficient data storage, retrieval, and management.
- SQL is a powerful language used to interact with databases, and proficiency in SQL is a highly valuable skill in the tech industry.
- Knowledge of database design and normalization ensures data integrity and minimizes redundancy, leading to efficient and reliable applications.

## Files

- `create_course_table.sql` - Script to create the `Course` table and insert initial data.
- `create_student_table.sql` - Script to create the `Student` table and insert initial data.
- `machine_learning.sql` - Query to list the names and surnames of all students doing the DS03 course.
- `final_stage.sql` - Query to list the email addresses of all students who are doing a level 3 course.
- `easiest_courses.sql` - Query to list the first names of all students that achieve a mark of 70 or above, along with the course name that they got a mark of 70 or above in.
- `julia_python.sql` - Query to list the marks of all students who have been taught by Julia Python.

## Setup

1. Install SQLite.
2. Create the `School.db` database.
3. Run `create_course_table.sql` to create and populate the `Course` table.
4. Run `create_student_table.sql` to create and populate the `Student` table.

## Running Queries

- Use your preferred SQLite client or command-line interface to run the provided SQL query files.

## Example Queries

### machine_learning.sql

```sql
SELECT first_name, last_name
FROM Student
WHERE stu_subject_code = 'DS03';
```

### final_stage.sql

```sql
SELECT Student.email
FROM Student
INNER JOIN Course ON Student.stu_subject_code = Course.course_code
WHERE Course.course_level = 3;
```

### easiest_courses.sql

```sql
SELECT Student.first_name, Course.course_name
FROM Student
INNER JOIN Course ON Student.stu_subject_code = Course.course_code
WHERE Student.mark >= 70;
```

### julia_python.sql

```sql
SELECT Student.mark
FROM Student
INNER JOIN Course ON Student.stu_subject_code = Course.course_code
WHERE Course.teacher_name = 'Julia Python';
```

## License

This project is licensed under the MIT License.
```

### Steps to Add README.md on GitHub Directly:

1. **Go to Your GitHub Repository:**
   - Open your web browser and navigate to your GitHub repository page.

2. **Create a New File:**
   - Click on the `Add file` button and select `Create new file`.

3. **Name the File README.md:**
   - In the `Name your file...` field, type `README.md`.

4. **Copy and Paste the Content:**
   - Copy the content provided above.
   - Paste it into the text area provided for the new file.

5. **Commit the New File:**
   - Scroll down to the commit section.
   - Add a commit message like "Add README file".
   - Choose the option to commit directly to the `main` branch (or `master` if that's the default branch).
   - Click the `Commit new file` button.
