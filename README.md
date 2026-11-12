# Self-Hosted Private Cloud Storage Using Nextcloud, Docker, Ngrok and WebDAV

## Overview

This project demonstrates the implementation of a self-hosted private cloud storage system using Nextcloud on personal hardware.

The system uses a Windows 11 laptop with a 512 GB SSD as the storage host. Nextcloud and MariaDB are deployed using Docker and Docker Compose, providing centralized file storage and management.

Remote access is configured using Ngrok, while PowerShell and WebDAV are used to automate file processing. Windows Task Scheduler executes the automation script at scheduled intervals.

The project provides practical experience in containerization, cloud storage, networking, storage management and automation.

## Architecture

The system consists of the following components:

- **Client Layer:** Web browser and Nextcloud mobile application.
- **Application Layer:** Nextcloud Server 27 running inside Docker.
- **Database Layer:** MariaDB 10.6 for application database management.
- **Storage Layer:** Local SSD storage mapped into the Docker containers.
- **Networking Layer:** Ngrok HTTPS tunnel for remote access.
- **Automation Layer:** PowerShell, WebDAV and Windows Task Scheduler.

## Technologies Used

| Technology | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Docker Desktop | Containerization |
| Docker Compose | Service management |
| Nextcloud Server 27 | Cloud storage platform |
| MariaDB 10.6 | Database |
| Ngrok | Remote access |
| WebDAV | File management and transfer |
| PowerShell | Automation scripting |
| Windows Task Scheduler | Scheduled execution |

## Key Features

- Self-hosted cloud storage using personal hardware.
- Docker-based deployment of Nextcloud and MariaDB.
- Local SSD storage integration.
- Individual user accounts and separate file spaces.
- Remote access through an HTTPS tunnel.
- External storage configuration using Nextcloud.
- Automated file processing using WebDAV.
- PowerShell-based file management.
- Scheduled automation using Windows Task Scheduler.
- Mobile access and automatic photo uploads.

## Implementation

### 1. Docker Deployment

- Installed Docker Desktop on Windows 11.
- Created Docker Compose configuration.
- Deployed Nextcloud Server 27 and MariaDB 10.6.
- Configured persistent storage using Docker volume mappings.

### 2. Storage Configuration

- Created a local storage directory on the host system.
- Mounted the directory inside the Nextcloud container.
- Enabled External Storage Support.
- Configured the mounted directory as local external storage.

### 3. Multi-User Configuration

- Created separate Nextcloud user accounts.
- Configured individual user storage spaces.
- Verified separate user directories within the Nextcloud data directory.

### 4. Remote Access

- Configured Ngrok to expose the local Nextcloud service.
- Established HTTPS-based remote connectivity.
- Updated Nextcloud trusted domain configuration.

### 5. File Automation

- Configured WebDAV access to Nextcloud.
- Developed a PowerShell script to process files in the cloud inbox.
- Implemented file listing, copying and deletion operations.
- Configured Windows Task Scheduler for automatic execution.

### 6. Mobile Integration

- Connected the Nextcloud mobile application.
- Configured automatic uploads from a selected mobile folder.
- Verified uploaded files in Nextcloud storage.

## Project Results

The implementation successfully demonstrated:

- Deployment of a private cloud storage platform.
- Integration of local storage with Nextcloud.
- Containerized application and database services.
- Multi-user storage management.
- Remote access using Ngrok.
- Automated file processing using WebDAV and PowerShell.
- Scheduled execution and mobile file uploads.

## Challenges and Solutions

| Challenge | Solution |
|---|---|
| External storage not appearing in Nextcloud | Enabled External Storage Support and configured local storage. |
| Remote access to local server | Configured Ngrok HTTPS tunnelling. |
| Untrusted domain error | Updated Nextcloud trusted domain configuration. |
| Repetitive manual file processing | Developed PowerShell automation using WebDAV. |
| Manual script execution | Configured Windows Task Scheduler. |

## Learning Outcomes

- Docker and containerized application deployment.
- Cloud storage architecture and administration.
- Persistent storage and volume mapping.
- Database integration.
- User management and storage isolation.
- Remote networking and HTTPS tunnelling.
- WebDAV protocol and PowerShell automation.
- Windows task scheduling.

## Documentation

Detailed project documentation, including implementation steps and screenshots, is available in:

**[Nextcloud Project Documentation (PDF)] : Documentation.pdf**

## Conclusion

This project demonstrates how a private cloud storage environment can be implemented using open-source technologies and personal hardware. By integrating Nextcloud, Docker, MariaDB, Ngrok and WebDAV automation, the system provides centralized file management, remote access and automated storage workflows without depending on third-party cloud storage providers.

---

**Technologies:** Nextcloud | Docker | Docker Compose | MariaDB | Ngrok | WebDAV | PowerShell | Windows 11
