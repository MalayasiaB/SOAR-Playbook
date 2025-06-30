<h1>Splunk SOAR Playbook Creation</h1>


<h2>Description</h2>
Project consists of a test playbook developed within a local instance of Splunk SOAR to demonstrate automation and task management capabilities. The playbook showcases how to assign workloads to specific users and track their completion in real time. Upon execution, the system displays KPIs related to task progress, helping visualize operational efficiency and response timelines within the SOAR platform.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Jira</b> 
- <b>Gmail</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (24H2)

<h2>Program walk-through:</h2>

<p align="center">
In SOAR I navigated to the playbook dropdown and began the creation of this playbook. Selected automation for playbook type. I want this playbook to automatically run when triggered. This setting will be utilized in completing my workloads: <br/>
<img src="https://github.com/user-attachments/assets/95eb503d-08e3-4b67-8bae-ea4ff6022a24" height="80%" width="80%" alt="Honeypot Steps"/>
<br />
<br />
A name was given in the input variable and my first action is an email alert, to serve as the initial means of notification. The input information can be seen at the bottom right:  <br/>
<img src="https://github.com/user-attachments/assets/f68c0964-e108-4666-8779-951ab4f3cc48" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Second action, utilizes Jira for ticket creation that will aid in incident management: <br/>
<img src="https://github.com/user-attachments/assets/619ed604-8d61-49c5-ab1c-996111f75a24" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A prompt is also added, another individual step from the start of the playbook. This prompt serves as a step within the workflow for the analyst to begin interacting with the playbook providing information, or gathering data. I set at parameter to complete in 10 minutes just for testing:  <br/>
<img src="https://github.com/user-attachments/assets/cf747fe9-14ee-495f-a054-3cb53c66617f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
A decision tree is added below the prompt to determine next steps in playbook completion based on conditions. Condition 1 is to list processes if severity is high:  <br/>
<img src="https://github.com/user-attachments/assets/6c40673b-1531-4f4c-97d3-b3f8521f95ee" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Condition 2 requires further investigation if the number of artifacts is greater than 4. A ticket will be created in Jira and the Analyst will send an email to team member(s) who handle escalation and this will mark the end of the playbook:  <br/>
<img src="https://github.com/user-attachments/assets/a2f1aa9d-e197-47b5-873b-0e2da0692f36" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Should condition 1 criteria be met, the next action is to list connections that may have taken place with an action below to block malicious IP's:  <br/>
<img src="https://github.com/user-attachments/assets/7aa3699b-5af3-4c46-972e-8d849125e475" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
From there another decision tree is added below the list connections action, to isolate the network if further action should be taken beyond blocking IP's. This also creates a ticket in Jira:  <br/>
<img src="https://github.com/user-attachments/assets/a9b28958-f048-43dd-acf4-870493b1fca7" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The action below network isolation, is to send a confirmation email. This step will finalize the playbook:  <br/>
<img src="https://github.com/user-attachments/assets/c4c033ad-eb86-493b-ae4c-71373d9f383d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Finalized Playbook:  <br/>
<img src="https://github.com/user-attachments/assets/89cb19d3-53a7-4625-ae33-290f96042d71" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here; I am showcasing events, KPI's before and after assigning a workload to myself:  <br/>
<img src="https://github.com/user-attachments/assets/fccadfb9-5521-467d-ad88-7e12da2edfe8" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Assigned workload:  <br/>
<img src="https://github.com/user-attachments/assets/a7d592c7-cca6-40e7-bef3-559e10d6ac12" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Completed workload and KPI's:  <br/>
<img src="https://github.com/user-attachments/assets/01dd01e2-d07a-4e5e-aada-edc39bdc10b3" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
