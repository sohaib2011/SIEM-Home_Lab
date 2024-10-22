# Elastic SIEM Lab Setup - Basic Security Monitoring.
Successfully set up and configured Elastic Stack SIEM in a home lab environment


## Objective
* Create an Agent and successfully configure it with a specific host
* Generate simple security events to be registered in the SIEM
* Simple queries to analyze the logs 

## Tools Needed For This Project
* VMware Workstation Pro
* Elastic Cloud console
* Kali Linux



## Step 1: Creating an Agent - Log Collector



1.1 Log in on your Elastic Instance, then select "Add Integrations" from the menu and find "Elastic Defend".
<img width="943" alt="image" src="https://github.com/user-attachments/assets/f74b7e34-a553-4935-bf95-7f4324ea7e68">

1.2 After adding the integration to Elastsic, follow the instructions to configure the Elastic Agent with host (in this case we will use Kali Linux)

<img width="340" alt="image" src="https://github.com/user-attachments/assets/38de58ea-f798-42a9-b18b-b8a6c7e3f9e6">

1.3 Run command in Kali Linux. 

Note: To verify that the host has been successfully configured with agent, a message will say "Elastic Agent has been successfully installed"

<img width="550" alt="image" src="https://github.com/user-attachments/assets/4db6c101-aaad-4ca7-9992-12514983d154">



<img width="300" alt="image" src="https://github.com/user-attachments/assets/9008642e-384d-4d47-b0b2-53bb70b33060">


## Step 2: Generating Security Events - Kali Linux
2.1 Run some nmap scans on the Kali Linux machine. The idea here is to run a few scans with different syntaxes e.g `nmap -p- <ip>`  (you will see why in the later section)

<img width="560" alt="image" src="https://github.com/user-attachments/assets/b12bbc47-8c51-4a40-927a-3e4335ad24f7">



## Step 3: Security Event Searching in Elastic SIEM
3.1 Click on menu, under category "Observability" you will see Logs"

<img width="150" alt="image" src="https://github.com/user-attachments/assets/c69d83c2-e3e4-4171-b5c3-4ca62758c933">


3.1.0 This view is showcasing everything monitored and managed by the Elastic Agent on machine kali. This is a strong indication that our agent is truly working!

<img width="550" alt="image" src="https://github.com/user-attachments/assets/4361b750-4845-42b7-bff7-fc463a7c938b">


3.2 We can narrow down our search to look for the specific nmap scans we did earlier. 



