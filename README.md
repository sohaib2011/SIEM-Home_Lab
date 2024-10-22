# Elastic SIEM Lab Setup - Basic Security Monitoring.
Successfully set up and configured Elastic Stack SIEM in a home lab environment

Overview
What is SIEM?

## Objective
..

Tools used
Virtualbox or VMware (in this scenario the demonstration is simulated on virtualbox)
Elastic Cloud console
Kali Linux



## Step 1: Creating an Agent - Log Collector



1.1 Log in on your Elastic Instance, then select "Add Integrations" from the menu and find "Elastic Defend".
<img width="943" alt="image" src="https://github.com/user-attachments/assets/f74b7e34-a553-4935-bf95-7f4324ea7e68">

1.2 After adding the integration to Elastsic, follow the instructions to configure the Elastic Agent with host (in this case we will use Kali Linux)

<img width="340" alt="image" src="https://github.com/user-attachments/assets/38de58ea-f798-42a9-b18b-b8a6c7e3f9e6">

1.3 Run command in Kali Linux. 

Note: To verify that the host has been successfully configured with agent, a message will say "Elastic Agent has been successfully installed"

<img width="450" alt="image" src="https://github.com/user-attachments/assets/4db6c101-aaad-4ca7-9992-12514983d154">



<img width="211" alt="image" src="https://github.com/user-attachments/assets/9008642e-384d-4d47-b0b2-53bb70b33060">


## Step 2: Generating Security Events - Kali Linux
2.1 Run several nmap scans on localhost. The idea here is to run a few more scans with different syntaxes e.g `nmap -p- <ip>`  (you will see why in later section)

<img width="400" alt="image" src="https://github.com/user-attachments/assets/32bd3f04-9969-4cb2-9237-9a0ef5475f75">


## Step 3: Security Event Searching in Elastic SIEM




