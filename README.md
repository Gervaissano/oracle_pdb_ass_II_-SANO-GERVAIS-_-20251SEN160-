# oracle_pdb_ass_II_-SANO-GERVAIS-_-20251SEN160-

# Oracle PDB Assignment II

## Student Information

- **Student ID:** 20251SEN160
- **First Name:** SANO GERVAIS
- **Course:** PL AND SQL
- **Database:** Oracle Database 21c

---

## 1. Overview of Tasks

This assignment focuses on creating, managing, monitoring, and deleting an Oracle Pluggable Database (PDB).

The main tasks completed were:

1. Creating a new Pluggable Database.
2. Verifying the created PDB.
3. Opening and managing the PDB.
4. Creating and deleting a PDB according to the required naming convention.
5. Confirming that the PDB was completely deleted.
6. Accessing and demonstrating Oracle Enterprise Manager (OEM).
7. Documenting the work using screenshots.

---

## 2. Oracle Environment Used

The assignment was completed using:

- **Database:** Oracle Database 21c
- **Operating System:** Windows
- **Oracle Tool:** SQL*Plus 
- **Oracle Enterprise Manager:** OEM
- **Container Database (CDB):** CDB$ROOT
- **PDB:** SA_PDB_20251SEN160

---

## 3. Task 1 – PDB Creation

A new Pluggable Database was created from the CDB root using the `CREATE PLUGGABLE DATABASE` command.

### Main steps

1. Connected to Oracle as SYSDBA.
2. Verified that the current container was `CDB$ROOT`.
3. Created the PDB using the required naming convention.
4. Verified that the PDB was created successfully.
5. Opened the PDB in `READ WRITE` mode.
6. Saved the PDB state so that it can automatically open after database restart.

### Screenshots

The screenshots demonstrating PDB creation are available in:

[SCREEN OF TASK1: PDB creation command, PDB open state, User created inside PDB (username clearly visible)](https://github.com/Gervaissano/oracle_pdb_ass_II_-SANO-GERVAIS-_-20251SEN160-/blob/test-1/CREATING%20OF%20PDB%20AND%20USER_NAME%20INSIDE%20PDB.PNG)

---

## 4. Task 2 – PDB Deletion

A PDB was created using the required naming convention for deletion.

The PDB was verified before deletion and then completely removed from the Oracle database.

### Main steps

1. Created the required temporary PDB.
2. Verified that the PDB existed.
3. Closed the PDB before deletion.
4. Deleted the PDB completely.
5. Verified that the PDB no longer existed.

### Screenshots

The screenshots demonstrating PDB deletion are available in:

[TASK 2 SCREEN OF DROPPING OF PDB_DELETION](Task2.png)

---

## 5. Task 3 – Oracle Enterprise Manager

Oracle Enterprise Manager (OEM) was used to access and monitor the Oracle database environment.

The dashboard provides information about the database environment and allows database administrators to monitor database components.

### Screenshots

The OEM screenshots are available in:

[TASK 3 screenshots/oem_dashboard/](TASK3.PNG)


## 6. Challenges Faced and Solutions

### Challenge 1: SHOW PDBS command was not available

The `SHOW PDBS` command returned:

`SP2-0382: The SHOW PDBS command is not available`

This was solved by using the following SQL query:

```sql
SELECT CON_ID, NAME, OPEN_MODE
FROM V$PDBS;
