# Elastic SIEM Lab Setup - Basic Security Monitoring.
Successfully set up and configured Elastic Stack SIEM in a home lab environment

Overview
What is SIEM?

Objective

Tools used
Virtualbox or VMware (in this scenario the demonstration is simulated on virtualbox)
Elastic Cloud console
Kali Linux

## Contents:
1. [Prerequisites and Installation](./setup/README.md)
2. [Configuring Logstash](./logstash/README.md)
3. [Configuring Elasticsearch](./elasticsearch/README.md)
4. [Setting up Kibana](./kibana/README.md)
5. [SIEM Usage](./usage/README.md)


**Step 1: In order to set up an Elastic SIEM Instance, we have to create an agent to collect logs**


1.1 Login on your Elastic Instance, then select "Add Integrations" from the menu and find "Elastic Defend".
<img width="943" alt="image" src="https://github.com/user-attachments/assets/f74b7e34-a553-4935-bf95-7f4324ea7e68">

1.2 After adding the integration to Elastsic, follow the instructions to configure the Elastic Agent with host (in this case, Kali Linux)

<img width="340" alt="image" src="https://github.com/user-attachments/assets/38de58ea-f798-42a9-b18b-b8a6c7e3f9e6">

