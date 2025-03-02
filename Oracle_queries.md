- `sudo docker start oracle-xe`                            # Starting the oracle container
  `sudo docker ps`
  `sqlplus system/oracle_pass//localhost:1521/XE`

- `CREATE TABLE Students(`               # Creating a Table (database)
  `ID number(10),`
  `roll_no number(9),`
  `Name varchar2(25),`
  `Gender varchar2(10),`
  `Grade varchar2(5),`
  `Remarks varchar2(30));`

- `INSERT INTO Students(ID, Roll_no, Name, Gender, Grade)VALUES (1, 242332,'Ahmad', 'MALE', 'A+')`
- `ALTER TABLE your_table_name RENAME COLUMN Marks TO Grade;`       # Rename the field

- `ALTER TABLE Student DROP COLUMN Grade;`
- `ALTER TABLE Student ADD Age number(3);`

- `UPDATE student`
  `SET gender = 'Male'`
  `WHERE ID = 2;`

- `DESCRIBE Student;` 
- `Select * from Student`

- `COMMIT;`
- `ROLLBACK;`			    # Come back to the last commit.
- `SET AUTOCOMMIT ON;`		# For automatically storing the data, Not recommended


- `DROP TABLE Student`		# Permanently delete the specific table
