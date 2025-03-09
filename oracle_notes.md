- `sudo docker start oracle-xe`                            # Starting the oracle container
  `sudo docker ps`
  `sqlplus system/oralce_pass@//localhost:1521/XE`


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

UPDATE customer
SET cust_dob = TO_DATE('15-05-1998', 'DD-MM-YYYY')
WHERE cust_id = 1002;













