![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/d421be6e-1ac4-4c4d-8951-b6f2ba79a5be)

# osTicket- Prerequisites and Instillations
<p>This tutorial outlines the prerequisites and instillation of the open-source help desk ticketing system osTicket.</p> 
<h2>Video Demonstration</h2> 

[YouTube: How to Install osTicket with Prerequisites](https://github.com/Kalebrsims/os-ticket)

## Introduction

In this project, I build a ticketing system in Azure and install various resources into a virtual machine, which is then interpreted by Microsoft Windows 10 to build out osTicket. In this project I play the position of help desk support through problem solving various technical issues as well as System Administration, managing levels of access and defining SLA parameters. 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information System (IIS)

## Operating Systems Used
- Windows 10 (21H2)

## List of Prerequisites
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/b9e0d8f1-03bd-4d3f-81b9-ee2e7fe98efe)


- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
When creating the VM, allow it to create a new Virtual Network (Vnet)



## Instillation Steps
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/8239e9c9-a0ba-475e-b724-a6216607c330)
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/c199349f-c112-4315-b314-d61b3b963714)

## Post Instillation Steps
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/61a2d178-ffb7-4797-9460-42ef14e0264c)
Configure Roles
Admin Panel -> Agents -> Roles
Supreme Admin
Configure Departments
Admin Panel -> Agents -> Departments
System Administrators
Configure Teams
Admin Panel -> Agents -> Teams
Level I Support
Level II Support
Allow anyone to create tickets
Admin Panel -> Settings -> User Settings
Registration Required: Require registration and login to create tickets 
Configure Agents (workers)
Admin Panel -> Agents -> Add New
Jane
John
Configure Users (customers)
Agent Panel -> Users -> Add New
Karen
Ken
Configure SLA
Admin Panel -> Manage -> SLA
Sev-A (1 hour, 24/7)
Sev-B (4 hours, 24/7)
Sev-C (8 hours, business hours)
Configure Help Topics
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset


## osTicket: Ticket Lifecycle Examples
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/f98c2618-8b50-4d65-998d-68eff5f64bf3)
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/34ad2787-e1fe-47cd-b92a-197e844d1894)
![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/0bf16cd8-5a3b-4c39-ad1a-9bf5b2f410f7)
<p> Creating, triaging, and solving tickets. 
Ticket examples:
Sev-A (1 hour, 24/7) [entire mobile/online banking system is down] -> SysAdmins
Sev-B (4 hours, 24/7) [accounting department needs adobe upgrade, broken]
Sev-B/C (2 hours, business hours) </p>

## Attack Maps Before Hardening / Security Controls

```All map queries actually returned no results due to no instances of malicious activity for the 24 hour period after hardening.```

## Metrics After Hardening / Security Controls

The following table shows the metrics we measured in our environment for another 24 hours, but after we have applied security controls:
Start Time 2023-03-18 15:37
Stop Time	2023-03-19 15:37

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 8778
| Syslog                   | 25
| SecurityAlert            | 0
| SecurityIncident         | 0
| AzureNetworkAnalytics_CL | 0

## Conclusion

In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness.

It is worth noting that if the resources within the network were heavily utilized by regular users, it is likely that more security events and alerts may have been generated within the 24-hour period following the implementation of the security controls.
