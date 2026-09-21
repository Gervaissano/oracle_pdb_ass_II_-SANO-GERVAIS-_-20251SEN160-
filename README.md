# oracle_pdb_ass_II_-SANO-GERVAIS-_-20251SEN160-

# Oracle PDB Assignment II

## Student Information

- **Student ID:** [Student ID]
- **First Name:** [First Name]
- **Course:** [Course Name]
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
- **Operating System:** [Windows/Linux]
- **Oracle Tool:** SQL*Plus / SQL Developer
- **Oracle Enterprise Manager:** OEM
- **Container Database (CDB):** [CDB Name]
- **PDB:** [PDB Name]

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

`screenshots/pdb_creation/`

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

`screenshots/pdb_deletion/`

---

## 5. Task 3 – Oracle Enterprise Manager

Oracle Enterprise Manager (OEM) was used to access and monitor the Oracle database environment.

The dashboard provides information about the database environment and allows database administrators to monitor database components.

### Screenshots

The OEM screenshots are available in:

`screenshots/oem_dashboard/`

---

## 6. Challenges Faced and Solutions

### Challenge 1: SHOW PDBS command was not available

The `SHOW PDBS` command returned:

`SP2-0382: The SHOW PDBS command is not available`

This was solved by using the following SQL query:

```sql
SELECT CON_ID, NAME, OPEN_MODE
FROM V$PDBS;
