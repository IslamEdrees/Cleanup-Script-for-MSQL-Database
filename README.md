# Cleanup-Script-for-MSQL-Database


## Overview
This Bash script helps to clean up old records (older than 6 months) from specific tables in the MYSQL database. It first counts the records, prompts the user for confirmation, deletes the old records, and then repairs the affected tables to optimize performance.

## Features
- Connects to MySQL database.
- Checks and counts old records before deletion.
- Prompts for user confirmation before deleting data.
- Repairs tables after deletion.
- Displays progress indicators during execution.

## Requirements
- MySQL server installed and accessible.
- User with sufficient privileges to delete records and repair tables.
- Bash shell environment.

## Installation
1. Clone this repository or download the script.
2. Ensure you have execute permissions:
   ```bash
   chmod +x cleanup_script.sh
   ```

## Configuration
Modify the following database parameters in the script before running:
```bash
DB_HOST="your_database_host"
DB_USER="your_database_user"
DB_PASS="your_database_password"
DB_NAME="your_database_name"
```

## Usage
Run the script using:
```bash
./cleanup_script.sh
```
The script will:
1. Count records older than 6 months for each table.
2. Ask for confirmation before deleting records this is for normal version but for the Auto version no.
3. Delete records and repair tables if confirmed.

## Tables Affected
The script checks and cleans up the following tables:
- `datamart_queue_details`
- `datamart_call_details`
- `datamart_cmp_call_list_details`
- `datamart_agent_details`
- `datamart_agent_sessions`
- `datamart_inbound_call_resume`
- `datamart_not_ready_reason`
- `datamart_queue_resume`
- `datamart_queue_resume_event`
- `datamart_agent_sales`
- `datamart_call_extradata`
- `xxx_xxx`
- add name of tables as you like 

## Safety & Precautions
- **Backup your database** before running the script.
- Ensure that the records being deleted are not required for compliance or reporting.
- Run the script during off-peak hours to minimize impact on live operations.
- For Backup you can check the Back Repo also 



