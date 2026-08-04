# Windows Server Enterprise Infrastructure

Practical Windows Server infrastructure project completed as part of a Server Administration course.

The project involved designing, implementing and documenting a Windows Server 2025 environment for a simulated medium-sized organization. The infrastructure was designed around two logical sites with centralized authentication, file services, remote access, update management and backup.

## Environment

The infrastructure was virtualized using Proxmox and consisted of:

- 2 Windows Server 2025 Domain Controllers
- 1 Windows Server 2025 Server Core backup server
- 3 Windows 11 workstations
- Two logical Active Directory sites
- Active Directory Domain Services
- AD-integrated DNS
- Group Policy
- WSUS
- IIS and FTP
- Centralized file services

## Active Directory

Active Directory Domain Services was deployed across two Domain Controllers, with one Domain Controller assigned to each logical site.

The second Domain Controller was joined to the existing domain to provide replication and redundancy.

The Active Directory structure included Organizational Units for:

- Economy
- IT
- Production
- Management

Users were organized into the appropriate OUs and security groups were used for access control.

## DNS

DNS was installed on both Domain Controllers and integrated with Active Directory.

The configuration included:

- AD-integrated DNS
- Internal DNS zone
- Unique DNS names for all systems
- DNS recursion disabled
- DNS services available through both Domain Controllers

## Remote Workstations

Windows 11 virtual workstations were configured for remote access using Remote Desktop.

Access was controlled using Active Directory security groups:

- Economy users allowed
- IT users allowed
- Management users allowed
- Production users denied

## File Services

Centralized file services were implemented for domain users.

### Private Home Directories

Each user received a private home directory with:

- 100 MB storage quota
- Access restricted to the individual user
- Centralized storage on the server

### Shared Storage

A shared file area was configured for employees with:

- NTFS permissions
- Active Directory group-based access control
- FTP access using domain credentials

## Group Policy

Group Policy was used to centrally manage domain-joined computers and users.

Policies were used for areas including:

- WSUS configuration
- Software deployment
- Computer configuration
- Centralized administrative settings

## WSUS

Windows Server Update Services was deployed for centralized update management.

Clients and servers were configured through Group Policy to use the internal WSUS server rather than managing updates individually.

The configuration was verified using applied Group Policy and Windows registry settings.

## Backup and Recovery

A dedicated Windows Server Core machine was configured as the backup server.

The backup solution included:

- Dedicated backup storage
- Daily scheduled backups
- System state and shared file backups
- Backup job monitoring
- Backup integrity verification
- Test restores
- Recovery independent of the failed production server

The environment was designed so that services could be restored even if one of the production servers became unavailable.

## IIS Web Server

An internal IIS web server was deployed to publish system information and documentation.

The web server provided:

- Project information
- Access to the latest system documentation

## Administration and Maintenance

Administrative procedures were documented for:

- Creating new Active Directory users
- Assigning users to OUs and security groups
- Creating new virtual workstations
- Joining computers to the domain
- Deploying software through Group Policy
- Disabling and removing user accounts
- Managing WSUS
- Monitoring backups
- Troubleshooting Active Directory and DNS
- Reviewing Event Viewer logs
- Restoring data and virtual machines

## Skills Demonstrated

- Windows Server 2025 administration
- Active Directory Domain Services
- Active Directory replication
- Organizational Units and security groups
- Group Policy
- DNS administration
- Windows file services
- NTFS permissions
- Storage quotas
- Remote Desktop
- WSUS
- IIS
- FTP
- Windows Server Core
- Backup and disaster recovery
- Proxmox virtualization

## Project Context

This project was completed as a two-person group project together with Benjamin Poli as part of the Server Administration course at University West.

The infrastructure was designed, implemented, tested and documented collaboratively.
