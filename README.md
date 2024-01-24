![image](https://github.com/Kalebrsims/osticket-prereqs/assets/155590792/d421be6e-1ac4-4c4d-8951-b6f2ba79a5be)

# osTicket- Prerequisites and Instillations
<p>This tutorial outlines the prerequisites and instillation of the open-source help desk ticketing system osTicket.</p> 
<h2>Video Demonstration</h2> 

[YouTube: How to Install osTicket with Prerequisites](https://github.com/joshmadakor1/Algorithms-Practice)

## Introduction

In this project, I build a ticketing system in Azure and install various resources into a virtual machine, which is then interpreted by Microsoft Windows 10 to build out osTicket. In this project I play the position of help desk support through problem solving various technical issues as well as System Administration, managing levels of access and defining SLA parameters. 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information System (IIS)

## Operating Systems Used
- Windows 10 (21H2)

## List of Prerequisites
![Architecture Diagram](https://i.imgur.com/YQNa9Pp.jpg)

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

## Instillation Steps
![NSG Allowed Inbound Malicious Flows](https://i.imgur.com/1qvswSX.png)<br>
![Linux Syslog Auth Failures](https://i.imgur.com/G1YgZt6.png)<br>
![Windows RDP/SMB Auth Failures](https://i.imgur.com/ESr9Dlv.png)<br>

## Metrics Before Hardening / Security Controls

The following table shows the metrics we measured in our insecure environment for 24 hours:
Start Time 2023-03-15 17:04:29
Stop Time 2023-03-16 17:04:29

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent            | 19470
| Syslog                   | 3028
| SecurityAlert            | 10
| SecurityIncident         | 348
| AzureNetworkAnalytics_CL | 843

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
