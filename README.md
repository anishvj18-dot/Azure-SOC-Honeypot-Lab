# Azure SOC Honeypot Lab
Cloud-based honeypot SOC lab built on Microsoft Azure capturing 
real world RDP attacks and visualized using Microsoft Sentinel SIEM

## Overview
Deployed a Windows VM honeypot on Microsoft Azure intentionally 
exposed to the internet to capture and analyze real world 
cyberattacks. Used Microsoft Sentinel as the SIEM to collect, 
query and visualize live attack data from global threat actors.

## Architecture
- Windows VM exposed to internet as honeypot
- Network Security Group configured to allow all inbound traffic
- Log Analytics Workspace as central log repository
- Microsoft Sentinel as SIEM for analysis and visualization
- KQL Queries used to extract and enrich attack data
- GeoIP Watchlist with 55,000 rows used to map attacker locations

## Tools and Technologies Used
- Microsoft Azure
- Microsoft Sentinel (SIEM)
- Log Analytics Workspace
- KQL (Kusto Query Language)
- Network Security Groups (NSG)
- Windows Event Viewer
- Azure Virtual Networks
- GeoIP Geolocation Data

## What I Built
- Provisioned a Windows VM in Azure and deliberately exposed 
  it to the internet as a honeypot
- Configured NSG rules to allow all inbound traffic to attract 
  real world attackers
- Set up Log Analytics Workspace to collect Windows Security 
  Events from the VM
- Integrated Microsoft Sentinel as SIEM to analyze and 
  visualize attack data
- Wrote KQL queries to filter Event ID 4625 (failed RDP logins) 
  and enrich with geolocation data
- Uploaded a 55,000 row GeoIP watchlist to map attacker IP 
  addresses to real world locations
- Built a live attack map workbook in Sentinel visualizing 
  global attack origins

## Results
- Captured 67,400+ real RDP brute force attempts within hours 
  of deployment
- Attacks primarily originated from Jordanow, Poland
- Single malicious IP (185.156.73.169) attempted thousands of 
  brute force logins
- Built live attack map showing real world threat activity
- Identified attacker geolocation using KQL and GeoIP enrichment

## Screenshots

### Azure Resource Manager
<img width="975" height="504" alt="image" src="https://github.com/user-attachments/assets/6dd4dcd2-0a4a-40f8-a77b-29c482132fd8" />

### NSG Settings
<img width="975" height="501" alt="image" src="https://github.com/user-attachments/assets/3a44168e-600d-4444-8126-f95306231afc" />

### Log Analytics Workspace and KQL Results
<img width="975" height="473" alt="image" src="https://github.com/user-attachments/assets/1346ca9a-890a-4386-9f2a-e0fc5985a2e7" />

### Windows VM Attack Map
<img width="975" height="507" alt="image" src="https://github.com/user-attachments/assets/b76ff9f6-2cac-4742-98a0-a8071543bd55" />

## Skills Demonstrated
- Cloud infrastructure deployment and configuration
- SIEM deployment and management (Microsoft Sentinel)
- KQL (Kusto Query Language) query writing
- Network security configuration and management
- Threat detection and log analysis
- Geolocation data enrichment
- Attack visualization and mapping
- Real world incident analysis

## Key Learnings
- How attackers continuously scan the internet for exposed RDP ports
- How to use KQL to query and analyze security events at scale
- How to enrich raw log data with geolocation for threat intelligence
- How NSGs control inbound and outbound traffic in Azure
- How SIEM tools like Sentinel aggregate and visualize threat data
