# Personalized Elastic SIEM Lab Setup
Hands-on, easy-to-make practical SOC environment


## Objective
* Create an Agent and successfully configure it with a specific host
* Generate simple security events to be registered in the SIEM
* Simple queries to analyze the logs
* Bonus: Alerting in SIEM

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

**Note:** To verify that the host has been successfully configured with agent, a message will say "Elastic Agent has been successfully installed"

<img width="550" alt="image" src="https://github.com/user-attachments/assets/4db6c101-aaad-4ca7-9992-12514983d154">



<img width="300" alt="image" src="https://github.com/user-attachments/assets/9008642e-384d-4d47-b0b2-53bb70b33060">


## Step 2: Generating Security Events - Kali Linux
2.1 Run some nmap scans on the Kali Linux machine. The idea here is to run a few scans with different syntaxes e.g `nmap -p- <ip>`  (you will see why in the later section)

<img width="560" alt="image" src="https://github.com/user-attachments/assets/b12bbc47-8c51-4a40-927a-3e4335ad24f7">



## Step 3: Security Event Querying in Elastic SIEM
3.1 Click on menu, then under the category "Observability" you will see "Logs"

<img width="150" alt="image" src="https://github.com/user-attachments/assets/c69d83c2-e3e4-4171-b5c3-4ca62758c933">


3.1.0 Since we want to effectively view our logs in real-time, we can use the view "stream" in Elastic. As shown in the image below, all security-related activities happening on kali is being monitored by Elastic. This is a strong indication that our Agent is truly working!

<img width="479" alt="image" src="https://github.com/user-attachments/assets/5fd64f70-f975-4878-aebf-422ce27327a1">




3.2 We will have to narrow down the search query to filter out the specific events performed in the previous step(s)

<img width="817" alt="image" src="https://github.com/user-attachments/assets/3b02717a-2ddb-4503-adf9-bb360d18f203">


3.3 By clicking on "view details", we can inspect deeper into each dataset. Here we can find heaps of interesting information about the event, in this case what was run on the system.

<img width="467" alt="image" src="https://github.com/user-attachments/assets/b57a0d19-3f78-4fdc-86d4-268aac9208cf">


## Bonus: Create an Alert

4.1 From the menu button, click on "Alerts" (under category Security). We will have to define new rules for the alert to... well actually alert! To do this, click on "Manage Rules"

<img width="946" alt="image" src="https://github.com/user-attachments/assets/b3ebaad1-8484-4e37-a9a6-92472aeca3c6">


4.2 Click on "Create new rule" at the top-right corner (again). Here you will be introduced to a bunch of different rule types; however as of this demo we will use "Custom Query"

<img width="410" alt="image" src="https://github.com/user-attachments/assets/0f1e6556-97f7-44fd-a745-5aab16d4a7a1">


4.2.1 Following up, we will have to enter a specific condition for the rule. We will use the Nmap query shown in the previous stage

<img width="356" alt="image" src="https://github.com/user-attachments/assets/91703edd-01f0-44cd-961e-f30e5232a343">

4.3 Under the next page "About rule", define name and its given description. Here you will also rank the alert based on its severity, which will prioritize alerts based on importance.

<img width="368" alt="image" src="https://github.com/user-attachments/assets/2328bcc2-c40a-4cfb-8fd4-cdf97050094f">

4.4 Skipping through to "Rule action", choose the action that will trigger the alert when the condition is met. 

<img width="371" alt="image" src="https://github.com/user-attachments/assets/20c0a40a-0517-4542-8ab0-0cd78f493b34">


4.5 When done, click on "Create and enable rule" to finalize the alert :)










