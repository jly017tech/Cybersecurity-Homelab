
---
HuskyTechSupport Enterprise Cybersecurity
---
 

## Introduction


<h2>List of virtual machines</h2>
<ul>
    <li>[project-x-dc]: Windows Server 2025</li>
    <li>[project-x-win-client]: Windows 11 Enterprise</li>
    <li>[project-x-linux-client]: Ubuntu Desktop</li>
    <li>[project-x-sec-work]: Security Onion</li>
    <li>[project-x-sec-box]: Ubuntu Desktop</li>
    <li>[project-x-corp-svr]: Ubuntu Server</li>
    <li>[project-x-attacker]: Kali Linux</li>
</ul>

<h1>Prerequisite </h1>

<img width="845" height="703" alt="image" src="https://github.com/user-attachments/assets/c81473d8-baa8-4402-9d4c-ff49352e7418" />

<p> I use oracle virtualbox, downloaded 6 ISO files, and change Network adapter to NAT Network. Before I install and create virtual machines, I open Oracle Virtualbox and create Nat Networks name [project-x-NAT], so when this is selected for all the virutal machines will communicate each this IP address, for example, 192.0.0.0 while connecting to the internet.</p>

<br>


<img width="1020" height="829" alt="Screenshot from 2026-02-13 10-33-19" src="https://github.com/user-attachments/assets/03dbd634-ee05-48cb-92a2-9025aa42a7e9" />



<h2>Step 1: Setting up Windows Server 2025 and Windows 11 Enterprise</h2>

<p>
    I created two different virtual machines: Windows Server 2025 and Windows 11 Enterprise. Windows Server 2025 is a domain controller where it handles Computers and Users in the Active Directory and Windows 11 Enterprise handle Windows 11 clients.
</p>

<br>


<br>

<img width="1620" height="855" alt="Screenshot from 2026-02-15 13-48-43" src="https://github.com/user-attachments/assets/bc9454cd-bae3-4fec-ae5d-e6d9fd8c13c7" />

<h2>Step 2: Setting up Ubuntu Desktop & Ubuntu Server </h2>

<p>
    After completing Windows 2025 Server and Windows 11 Enterprise, I create two Linux Distros: Ubuntu Desktop and Ubuntu 
    Server. I clone Ubuntu Desktop [project-x-linux-client] as a template twice for Corporate server and Security box.
</p>



<h2>Step 3: Creating alerts in Wazuh SIEM Dashboard</h2>


<img width="1622" height="835" alt="Screenshot from 2026-02-15 13-27-45" src="https://github.com/user-attachments/assets/cf4d2e3e-9662-4316-b60c-19b24a42dcaf" />




<p>In this step, we configure a dedicated monitor to track unauthorized access and modifications to high-value assets. By leveraging the Wazuh syscheck module, we monitor specific sensitive file paths—such as configuration files, password databases, or proprietary data folders—in real-time. When a user interacts with these files, the Wazuh agent captures the event metadata, including the user identity, the process used, and the specific nature of the change (such as a checksum mismatch or attribute shift). This data is then cross-referenced against the Wazuh rule engine; if a modification is detected, the system triggers a high-severity alert on the dashboard, providing security analysts with the "who, what, and when" necessary for a rapid incident response.</p>

<br>


<h2>Step 4: </h2>
<img width="780" height="782" alt="Screenshot from 2026-02-11 23-23-06" src="https://github.com/user-attachments/assets/6186de8e-6c92-48e8-a9db-0bcc949580ec" />


<h2></h2>

<img width="957" height="835" alt="Screenshot from 2026-02-15 13-59-49" src="https://github.com/user-attachments/assets/cf406585-5ecc-473e-a9e9-65bbcfc457ae" />


