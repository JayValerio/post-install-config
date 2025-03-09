# post-install-config




<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTickets.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
<h2>Operating Systems Used </h2>

- Windows 10</b> Standard D2als v6 (2 vcpus, 4 GiB memory)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles, Departments, Teams
- Configure Users/Agents
- Configure Help Topics/SLA's


<p><h5>
Our first step is to configure our Departments, Teams and Roles,<br />
  We do this first to give us a much more structured foundation for later on when we configure Agents. 
</h5></p>
<p>
  <p>
     
  ____________________________________________________________________________________________________________________________
  </p>
  <br />
<h2>Configuring Roles</h2>
</p>
<br />

<p>
  To Configure Roles (for grouping permissions) go to ->
Admin Panel -> Agents -> Roles -> Add New Role

</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/96e91a5d-f7c4-49ad-af04-32cc30f83070)

</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/8d3295bf-0f28-4af6-aa40-ac2443bf4499)

</p>
<p>
Roles determine the permissions agents have in each department they access. Permissions can be toggled per role, and unlimited roles can be created and assigned across departments.
</p>

<p>
  For this Example we will be creating our own role "Supreme Admin" to showcase how it works.
</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/aa8bfa1e-e6f9-4d78-80dc-a100933c4eaf)

</p>

<p>
  The Permissions tab controls non-department-specific access within the help desk. It manages access to the User Directory, Organization, Knowledge Base, ticket metadata, email ban list, and staff statistics.
</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/d58049be-78b2-4b50-94c3-4524564cd0d7)

  ![image](https://github.com/user-attachments/assets/1bb99739-8eea-4044-aae8-61b7c40b8a84)

  ![image](https://github.com/user-attachments/assets/d5feb406-b8e0-4d63-8ebe-ff1c3650678b)


</p>

<p>
  Supreme Admin will have all access in this case.
</p>
<br />

<p>
  <h2>Configuring Departments</h2>
</p>

<p>To Configure Departments (Ticket Visibility, Mainenance vs Support vs System Administrators.)
go to -> Admin Panel -> Agents -> Departments -> Add New Department</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/1397434b-fbfe-4cf3-9a38-6d1135649588)

</p>

<p>
  Since tickets are routed through Departments in the help desk, there are many settings that can be set for each Department. For this example we will create our own Department "System Administrators" to see how it differs from other departments.
</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/58bbeab5-66ed-4ac9-86e3-adfb911cf59e)

  ![image](https://github.com/user-attachments/assets/13dc60d4-d20b-404b-89d2-8ca822a6c496)

</p>

<p>
 <p> osTicket Department Settings (Simplified)</p>
<p>Parent Department: If nested, agents with access to the parent can view tickets in child departments, but not vice versa.</p>
<p>Status: Determines if the department is active and can receive tickets.</p>
<p>Active: Available for ticket transfers.</p>
<p>Archived: No longer in use; reopened tickets create new ones under the default department.</p>
<p>Disabled: Cannot receive tickets; auto-routed tickets go to the default department.</p>
<p>Name & Type: Department name and visibility settings (Public or Private). Private departments hide assignments and signatures.</p>
<p>SLA & Schedule: Defines response time expectations and follows set schedules.</p>
<p>Manager: Assign a manager to receive special alerts.</p>
<p>Ticket Assignment: Restrict assignments to department members.</p>
<p>Claim on Response & Reopen Auto Assignment: Control auto-claim and ticket reassignment rules.</p>
<p>Outgoing Email Settings</p>
<p>Outgoing Email: Email used for agent responses.</p>
<p>Template Set: Email templates for auto-responses and alerts.</p>
<p>Auto-Responder Settings: Customize auto-replies for new tickets and messages.</p>
<p>Auto-Response Email: Email used only for auto-replies.</p>
</p>








<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

