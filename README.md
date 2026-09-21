# oracle_pdb_ass_II_20252SEN346_kevin
# Oracle Pluggable Database (PDB) Assignment II

## Overview
This repository contains documentation and screenshot evidence for Oracle Pluggable Database administration tasks, including creation, user setup, deletion, and monitoring via Oracle Enterprise Manager (OEM).


## Explanation of Tasks

### Task 1: Create a New Pluggable Database
- Created PDB `ke_pdb_20252SEN346` using `CREATE PLUGGABLE DATABASE`.
- Created administrative user `kevin_plsqlauca_20252SEN346` inside the PDB.
- Verified PDB open mode (`READ WRITE`) and account existence in `dba_users`.

### Task 2: Create and Delete a PDB
- Created temporary PDB `ke_to_delete_pdb_20252SEN346`.
- Verified its existence in `v$pdbs`.
- Closed and dropped the temporary PDB using `DROP PLUGGABLE DATABASE ... INCLUDING DATAFILES`.
- Confirmed complete removal via `v$pdbs`.

### Task 3: Oracle Enterprise Manager (OEM)
- Accessed OEM Database Express dashboard via `https://localhost:5500/em`.
- Captured environment health, container overview, and logged-in `sys` session.

## Challenges Faced & Solutions
- **Issue (ORA-65005 / ORA-01276):** File name conversion conflicts occurred during `CREATE PLUGGABLE DATABASE`.
- **Solution:** Removed the `FILE_NAME_CONVERT` clause and let Oracle Managed Files (OMF) handle file placement automatically.

## Integrity Statement
I certify that this assignment is my own work and conforms to academic integrity guidelines.

## Submission Details Block
Repository Link: https://github.com/tuyisengekevin/oracle_pdb_ass_II_20252SEN346_kevin
PDB Name Created: ke_pdb_20252SEN346
Issues Encountered: Yes (Resolved OMF file name conversion error)
