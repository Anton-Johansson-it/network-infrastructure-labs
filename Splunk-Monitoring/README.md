# Splunk Network and System Monitoring

Group project completed as part of the Computer Engineering program at University West.

The project focused on implementing a centralized logging and monitoring solution using Splunk Enterprise in a mixed network environment.

## Project Environment

The lab environment included:

- Splunk Enterprise
- Splunk Universal Forwarder
- Windows 11
- Ubuntu Linux
- Cisco routers and switches
- FortiGate firewall
- Syslog
- Windows Event Logs

Logs and system data from the different devices were collected by a centralized Splunk server and used for monitoring and visualization.

## Splunk Architecture

Splunk Enterprise was deployed on an Ubuntu virtual machine and configured as the central log collection and monitoring server.

The environment collected data from:

- Windows clients using Splunk Universal Forwarder
- Linux clients using Splunk Universal Forwarder
- Cisco network devices using Syslog
- FortiGate firewall using Syslog

The collected data was indexed in Splunk and used to create dashboards for system, network and security monitoring.

## Monitoring and Dashboards

Dashboards were created to visualize:

- Active hosts
- Network interface status
- Windows CPU utilization
- Windows memory utilization
- Linux CPU utilization
- Linux memory utilization
- Successful login attempts
- Failed login attempts

These dashboards provided a centralized overview of system performance, network status and basic security-related events.

## My Contribution

This project was completed as a group project with four students.

My primary responsibilities included:

- Installing and configuring Splunk Enterprise
- Setting up the Splunk server environment
- Configuring Splunk Universal Forwarder on the Windows client
- Configuring Windows Event Log collection for Security, Application and System logs
- Connecting the Windows client to the Splunk server
- Creating Splunk dashboards for monitoring and visualization

Through this work, I gained practical experience with centralized logging, Windows event collection, Splunk administration, log analysis and dashboard creation.
