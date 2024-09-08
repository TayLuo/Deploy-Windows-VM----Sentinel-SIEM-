<h1>Windows VM  - Sentinel(SIEM) - Automation</h1>


![Sentinel 3](https://github.com/TayLuo/Honeypot---Sentinel/assets/104034830/02d278da-e22a-42c5-9eca-f7f95fc7a7dd)

  - [Diagram of Configuration Process](https://github.com/TayLuo/Honeypot---Sentinel/blob/main/Diagram%20of%20Configuration%20Process)



<h2>Prerequisites</h2>

- <b>Create Resource Group</b> 
- <b>Virtual Machine</b>
- <b>Log Analystic Workspace</b>
- <b>Microsoft Sentinel</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Microsoft Sentinel</b>

- [Introduction of the Project](https://github.com/TayLuo/Deploy-Windows-VM----Sentinel-SIEM-/blob/main/The%20purpose%20of%20the%20Project)


<p align="center">
Create Recource Group: <br/>
<img src="https://imgur.com/731vDl5.png" height="80%" width="80%" >
<br />
<br />
<h2>Create Windows Virtual Machine</h2>
Steps to create a VM:  <br/>
Go to Virtual Machine > Create Virtual Machine.
Choose a new Resource Group, set the region (e.g., West US3), and configure the VM details.

<img src="https://imgur.com/m2t3cI1.png" height="80%" width="80%">
<br />
<br />
<img src="https://imgur.com/NapHG6s.png" height="80%" width="80%">
<br />
<br />
<img src="https://imgur.com/gHmPVxV.png" height="80%" width="80%">
<br />
<br />
<b>Security Group Configuration</b> <br /> <br />
1. Choose Advanced Security Group. <br />
2. Remove existing rules and add an inbound rule:
— Destination: Any
— Source: Any
— Source Port: All
— Priority: 100
<br />
<img src="https://imgur.com/e1XAsIO.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/KdVvnfy.png" height="80%" width="80%"/>
<br />
<br />

<img src="https://imgur.com/aL3jo6d.png" height="80%" width="80%" />
<br />
<br />
<h2>Log Analytics Workspace Setup:</h2>
1. Go to Log Analytics Workspace > Create.  <br/>
<img src="https://imgur.com/R0e1Eks.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/IN7nNV8.png" height="80%" width="80%"/>
</p>
2. Provide a name, set the region (e.g., West US3), and create the deployment.<br/><br/>
<img src="https://imgur.com/eApoGtE.png" height="80%" width="80%" />
<br />
<br />

<img src="https://imgur.com/16WCsHb.png" height="80%" width="80%" />
<br />
<br />
<h2>Microsoft Defender for Cloud Configuration</h2>
1. Navigate to Microsoft Defender for Cloud > Environment Settings <br/>
<img src="https://imgur.com/QOWGX6y.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/yih9FCp.png" height="80%" width="80%" />
<br />
<br />
2. Configure Honeypot Defender plans, SQL servers, and foundational CSPM settings.<br/>
<img src="https://imgur.com/X12mGJJ.png" height="80%" width="80%"/>
<br />
<br />

<h2>Data Collection Configuration</h2>
1. Under Data Collection, enable events like Windows Security and App Locker events. <br/>
<img src="https://imgur.com/xjG1G8W.png" height="80%" width="80%" />
<br />
<br />
<h2>Connect VM to Log Analytics Workspace:</h2>
1. Go to Virtual Machines > Honeypot > Connect to Log Analytics Workspace. <br/>
Confirm your selection:  <br/>
<img src="https://imgur.com/nWPCY57.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/BDMg9rt.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/Te5DEn9.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/SCC0a7C.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/tEiBRKk.png" height="80%" width="80%" />
<br />
<br />
<h2>Microsoft Sentinel Integration</h2>
1. In Microsoft Sentinel, create a new Sentinel for the Honeypot. <br/>

<img src="https://imgur.com/gQBVkkv.png" height="80%" width="80%"/>
<br />
<br />
Click “create”. <br/>
<img src="https://imgur.com/iyA2Cvx.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/u1Gd8xz.png" height="80%" width="80%" />
<br />
<br />
2. Retrieve the public IP address of the VM from Virtual Machines > Honeypot. <br/>

<img src="https://imgur.com/6Ub5J1s.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/gqCs6qi.png" height="80%" width="80%" />
<br />
<br />
<img src="https://imgur.com/A0wGnQy.png" height="80%" width="80%" />
<br />
<br />

Access Window VM with RDP<br/>

<img src="https://imgur.com/bcIGVSK.png" height="80%" width="80%" />
<br />
<br />

Enter the Public IP address in the Computer column, Username and password (Recall the username and password used when creating the Virtual machine).<br/><br/>
After being successfully logged in, search for “Event Viewer” and open the program, Click on “Security”. You will get to see some of the security events generated in the log during the duration of the VM running. <br /> <br />

<h2>Filter logs in Microsoft Sentinel</h2>
Open Logs in Microsoft Sentinel and remember to select our Log Analytics Workspace. <br/>
<img src="https://imgur.com/SFbcGzr.png" height="80%" width="80%" />
<br />
<br />
Sentinel uses Kusto Query Language to perform query on Logs. Lets perform some queries on our log from VM <br/>
<img src="https://imgur.com/KDTdD5W.png" height="80%" width="80%"/>
<br />
<br />


<h2>Creating Analytic Rules for Microsoft Sentinel and setting up alerts</h2>
select “Analytics” under configuration<br/>

<img src="https://imgur.com/TQCdjuq.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://imgur.com/hObY9Ot.png" height="80%" width="80%"/>
<br />
<br />

<img src="https://imgur.com/CilFj1S.png" height="80%" width="80%"/>
<br />
<br />

<img src="https://imgur.com/xEAjvya.png" height="80%" width="80%" />
<br />
<br />

<img src="https://imgur.com/LGOy8se.png" height="80%" width="80%" />
</p>


