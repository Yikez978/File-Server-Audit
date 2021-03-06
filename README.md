# File-Server-Audit
File Server Audit solves the problem of getting raw data to find what a user can access on a large file server by enumerating all NTFS (New Technology File System) ACLs (Access Control Lists) for all folders. With text utilities or SQL queries, the raw data can be turned into useful reports to find what a user has access to. The File Server View also can be used to help look at the output. File Server Audit will help someone else by allowing them to quickly create their own auditing process for their file servers. The code snippet is a sub to read Reads Discretionary Access Control Lists (ACLs). This helps when looking for who has access to folders.

### MSSQL Table Name: FileAudit

| Column Name           | Data Type     |
| --------------------- | ------------- |
| ID                    | int           |
| FolderPath            | nvarchar(MAX) |
| AccountSAMAccountName | nvarchar(MAX) |
| GroupSAMAccountName   | nvarchar(MAX) |
| ManagedBy             | nvarchar(MAX) |
| Inheritance           | nvarchar(MAX) |
| IsInherited           | nvarchar(MAX) |
| Rights                | nvarchar(MAX) |
| Owner                 | nvarchar(MAX) |
| Computer              | nvarchar(MAX) |
| RunDate               | bigint        |

### MySQL Table Name: FileAudit

| Column Name           |Data Type |
| --------------------- | -------- |
| ID                    | int      |
| FolderPath            | LONGTEXT |
| AccountSAMAccountName | LONGTEXT |
| GroupSAMAccountName   | LONGTEXT |
| ManagedBy             | LONGTEXT |
| Inheritance           | LONGTEXT |
| IsInherited           | LONGTEXT |
| Rights                | LONGTEXT |
| Owner                 | LONGTEXT |
| Computer              | LONGTEXT |
| RunDate               | bigint   |
