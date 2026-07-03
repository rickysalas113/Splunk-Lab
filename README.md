# Splunk Lab

## Objective

The Active Directory/Splunk project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system (Splunk). The lab also included Kali Linux as our attacking machine, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen my understanding of how machines send data to Splunk, also what to look for while investigating.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Ability to install Splunk and have it up and running with users.
- Create an Active Directory from scratch with organizational units and users.
- Installed Splunk forwarder with Sysmon on my user machine.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Crowbar, which is a brute-forcing tool in Kali Linux used to crack password-protected services like SSH, VNC, RDP, and openVPN.

## Screenshots of my work

- Here I am on my Splunk server setting a static IP of 192.168.10.10/24.

![image](https://github.com/user-attachments/assets/c9c871cd-0194-4c1d-b7fb-4b103438a05f)

- I am able to reach Splunk at 192.168.10.10:8000 (Splunk listens on port 8000).

![image](https://github.com/user-attachments/assets/defb85fb-6c73-4aea-9fd4-74d7ced139b8)

- Here I am Installing Splunk Forwarder onto my target machine.
  
![image](https://github.com/user-attachments/assets/58061cde-cc1d-4a22-8e6a-914f7ded3b34)

- I have successfully installed sysmon as well.

![image](https://github.com/user-attachments/assets/f1e310d7-e409-4f43-afac-bf7d5efdeb61)


- These are instructions for my Splunk Forwarder to push events related to Application, Security, System, and Sysmon over to my Splunk Server.

![image](https://github.com/user-attachments/assets/18786956-4cdf-4dd2-8536-2e76a0477794)

- The following shows the index "Endpoint". This is where events happening on the machine will be sent too

![image](https://github.com/user-attachments/assets/d41594cf-7e0e-49a9-b76c-2487c3161542)

- Using the Tool Crowbar on Kali to brute-force into one of the users I created in my domain. As you can see it was successful.

![image](https://github.com/user-attachments/assets/eb683485-3e79-4cc1-aeb1-0217598512d8)

- On my Splunk server you can see that there were 4 Event Codes generated. Event code #4625 indicated failed log ons. This is significant because it showed that 1 out of the 21 passwords worked. Event code #4624 indicated a successful log on to a user account.

![image](https://github.com/user-attachments/assets/c22725c7-8e67-47b5-8470-7c50e3c125c2)

- Diving deeper into the investigation we can see the network information of the attacker. My workstation Kali and source IP address 192.168.10.250

![image](https://github.com/user-attachments/assets/dd7ab1b0-ecad-47e1-974f-4dc57af52328)

