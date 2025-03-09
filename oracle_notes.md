- `sudo docker start oracle-xe`                            # Starting the oracle container
  `sudo docker ps`
  `sqlplus system/oralce_pass@//localhost:1521/XE`

- `ALTER TABLE Student DROP COLUMN Grade;`
- `ALTER TABLE Student ADD Age number(3);`

- `DROP TABLE Student`		# Permanently delete the specific table

✔ Use TRUNCATE TABLE when you need to clear data quickly but keep the table structure.
✔ Use DROP TABLE when you want to remove the table completely.


alter table enrollement
add constraint student_id_fk foreign key(student_id) references student(student_id)




- `CREATE TABLE customer(`
  `cust_id number(10),`
  `cust_name varchar2(25),`
  `cust_mobile_no number(15),`
  `cust_dob data);`

- `SQL> INSERT INTO customer (cust_id, cust_name, cust_mobile_no, cust_dob)`
  `VALUES (1000, 'Ahmad', 03000241950, TO_DATE('09-03-2025', 'DD-MM-YYYY'));`

- `Select * from customer;`
- `DESC customer`

- `commit;`
- `rollback;`

- `ALTER TABLE customer MODIFY cust_mobile_no VARCHAR2(15);`

- `ALTER TABLE customer ADD cust_mobile_str VARCHAR2(15);  -- Step 1: Add new column`
- `UPDATE customer SET cust_mobile_str = TO_CHAR(cust_mobile_no);  -- Step 2: Copy data`
- `ALTER TABLE customer DROP COLUMN cust_mobile_no;  -- Step 3: Remove old column`
- `ALTER TABLE customer RENAME COLUMN cust_mobile_str TO cust_mobile_no;  -- Step 4: Rename column`













