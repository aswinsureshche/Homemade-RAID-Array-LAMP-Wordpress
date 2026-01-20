# System Architecture

## Overview
This project implements a fault-tolerant storage layer using RAID Level 1 and hosts a WordPress web application on a LAMP stack (Linux, Apache, MariaDB, PHP). The architecture emphasizes redundancy, service separation, and reliable web hosting.

## Storage Architecture
- **RAID Type:** RAID 1 (Mirroring)
- **Tool Used:** mdadm
- **Purpose:** Provide disk redundancy and protect data against single-disk failure
- **Mount Point:** RAID array mounted to a dedicated directory used for web content storage

## Server Stack
- **Operating System:** Linux
- **Web Server:** Apache
- **Database Server:** MariaDB
- **Scripting Language:** PHP
- **Application:** WordPress

## Data Flow
1. Client sends HTTP request to Apache
2. Apache processes PHP files using PHP module
3. PHP communicates with MariaDB to retrieve or store data
4. WordPress generates dynamic content
5. Content is served back to the client

## Security and Permissions
- File permissions configured using `chmod`
- Web directories assigned appropriate ownership
- Database access restricted to WordPress service account

## Verification
Each major component (RAID, Apache, PHP, Database, WordPress) was validated through terminal output and application-level testing, documented via screenshots.
