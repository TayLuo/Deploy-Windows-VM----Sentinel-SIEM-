<h1>Honeypot - Sentinel - Automation</h1>


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
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

  
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
