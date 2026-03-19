
---
HuskyTechSupport Enterprise Cybersecurity:
---
 

<img width="731" height="336" alt="image" src="https://github.com/user-attachments/assets/f5619764-8648-48fc-a0ee-fe0918cf3b54" />


## Introduction

<p> I use oracle virtualbox, downloaded 6 ISO files, and change Network adapter to NAT Network. Before I install and create virtual machines, I open Oracle Virtualbox and create Nat Networks name [project-x-NAT], so when this is selected for all the virutal machines will communicate each this IP address, for example, 192.0.0.0 while connecting to the internet.</p>

<br>

<h1>Prerequisite </h1>

<hr>

<h2>List of virtual machines</h2>
<ul>
    <li>Windows Server 2025</li>
    <li>Windows 11 Enterprise</li>
    <li> Ubuntu Desktop</li>
    <li> Security Onion</li>
    <li>Ubuntu Desktop</li>
    <li> Ubuntu Server</li>
    <li>Kali Linux</li>
</ul>


<h2>Changing IP Addresses for each virtual machines</h2>

<img width="845" height="703" alt="image" src="https://github.com/user-attachments/assets/c81473d8-baa8-4402-9d4c-ff49352e7418" />


<p>
In my homelab environment, I configured and changed IP addresses for each virtual machine to ensure proper network organization 
and communication between systems. I assigned static IP addresses to critical servers such as the domain controller and services 
like DHCP and DNS to maintain consistency, while allowing other machines to use dynamic addressing where appropriate. 
This process helped me understand how IP management works in an enterprise setting, including subnetting, avoiding IP conflicts, 
and ensuring reliable connectivity between systems. I also verified configurations using network troubleshooting tools and 
tested connectivity between virtual machines to confirm everything was properly set up.
</p>


<br>


<h2>Step 1: Setting up Windows Server 2025 and Windows 11 Enterprise</h2>
<img width="1020" height="829" alt="Screenshot from 2026-02-13 10-33-19" src="https://github.com/user-attachments/assets/03dbd634-ee05-48cb-92a2-9025aa42a7e9" />



<p>
    I created two different virtual machines: Windows Server 2025 and Windows 11 Enterprise. Windows Server 2025 is a domain controller where it handles Computers and Users in the Active Directory and Windows 11 Enterprise handle Windows 11 clients.
</p>

<br>


<br>

<h2>Step 2: Setting up Ubuntu Desktop & Ubuntu Server </h2>
<img width="1620" height="855" alt="Screenshot from 2026-02-15 13-48-43" src="https://github.com/user-attachments/assets/bc9454cd-bae3-4fec-ae5d-e6d9fd8c13c7" />


<p>
    After completing Windows 2025 Server and Windows 11 Enterprise, I create two Linux Distros: Ubuntu Desktop and Ubuntu 
    Server. I clone Ubuntu Desktop [project-x-linux-client] as a template twice for Corporate server and Security box.
</p>



<h2>Step 3: Creating alerts in Wazuh SIEM Dashboard</h2>


<img width="1622" height="835" alt="Screenshot from 2026-02-15 13-27-45" src="https://github.com/user-attachments/assets/cf4d2e3e-9662-4316-b60c-19b24a42dcaf" />


<br>

<p>In this step, we configure a dedicated monitor to track unauthorized access and modifications to high-value assets. By leveraging the Wazuh syscheck module, we monitor specific sensitive file paths—such as configuration files, password databases, or proprietary data folders—in real-time. When a user interacts with these files, the Wazuh agent captures the event metadata, including the user identity, the process used, and the specific nature of the change (such as a checksum mismatch or attribute shift). This data is then cross-referenced against the Wazuh rule engine; if a modification is detected, the system triggers a high-severity alert on the dashboard, providing security analysts with the "who, what, and when" necessary for a rapid incident response.</p>

<br>


<h2>Step 4: Installing Linux Onion Security </h2>
<img width="780" height="782" alt="Screenshot from 2026-02-11 23-23-06" src="https://github.com/user-attachments/assets/6186de8e-6c92-48e8-a9db-0bcc949580ec" />

<p></p>

<br>


<h2>Step 5: Setting up Email Server on Ubuntu</h2>

<img width="957" height="835" alt="Screenshot from 2026-02-15 13-59-49" src="https://github.com/user-attachments/assets/cf406585-5ecc-473e-a9e9-65bbcfc457ae" />

<hr>

<p>
In this step, I set up a functional email server on an Ubuntu system as part of my homelab environment. 
I installed and configured key services such as Postfix for handling outgoing mail (SMTP) and Dovecot 
for managing incoming mail (IMAP/POP3). I also worked on configuring domain and DNS records like MX, SPF, 
and DKIM to ensure proper email delivery and reduce the chances of emails being marked as spam. 
To improve security, I implemented SSL/TLS encryption and configured basic firewall rules. 
This setup allowed me to better understand how email systems operate in real-world environments 
and gave me hands-on experience with server configuration and troubleshooting.
</p>


<h2>Real-Life Scenario: Data Exfiltration</h2>

<img width="1355" height="954" alt="Screenshot from 2026-03-18 19-20-59" src="https://github.com/user-attachments/assets/33aa99bd-4761-4e65-98f7-de5235425f38" />

<hr>

<p>
Data exfiltration refers to the unauthorized transfer of sensitive information from a system, network, or device. 
In my understanding and practice, this can happen through various methods such as malware, phishing attacks, 
misconfigured systems, or even insider threats. Attackers may attempt to move data out of an environment using 
protocols like HTTP, FTP, DNS tunneling, or encrypted channels to avoid detection. 

From a security perspective, I focus on identifying and preventing data exfiltration by implementing monitoring 
tools, reviewing logs, and applying security controls such as data loss prevention (DLP), encryption, and strict 
access management. Understanding how data exfiltration works has helped me better recognize suspicious activity 
and strengthen overall system security in both real-world scenarios and my homelab environment.
</p>
