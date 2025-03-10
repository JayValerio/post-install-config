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
  To Configure Roles (for grouping permissions)<br />
  go to ->
Admin Panel -> Agents -> Roles -> Add New Role

</p>

<p>
  
  ![image](https://github.com/user-attachments/assets/96e91a5d-f7c4-49ad-af04-32cc30f83070)

</p>

<p>
  
![image](https://github.com/user-attachments/assets/19de8c40-88fb-480b-a74f-e701b449ed3b)


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

<p>To Configure Departments (Ticket Visibility, Mainenance vs Support vs System Administrators.)<br />
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
 <p><h3>osTicket Department Settings (Simplified)</h3></p>
<p><h5>Parent Department:</h5> If nested, agents with access to the parent can view tickets in child departments, but not vice versa.</p>
<p><h5>Status:</h5> Determines if the department is active and can receive tickets.</p>
<p><h5>Active:</h5> Available for ticket transfers.</p>
<p><h5>Archived:</h5> No longer in use; reopened tickets create new ones under the default department.</p>
<p><h5>Disabled:</h5> Cannot receive tickets; auto-routed tickets go to the default department.</p>
<p><h5>Name & Type:</h5> Department name and visibility settings (Public or Private). Private departments hide assignments and signatures.</p>
<p><h5>SLA & Schedule:</h5> Defines response time expectations and follows set schedules.</p>
<p><h5>Manager:</h5> Assign a manager to receive special alerts.</p>
<p><h5>Ticket Assignment:</h5> Restrict assignments to department members.</p>
<p><h5>Claim on Response & Reopen Auto Assignment:</h5> Control auto-claim and ticket reassignment rules.</p>
<p><h3>Outgoing Email Settings</h3></p>
<p><h5>Outgoing Email:</h5> Email used for agent responses.</p>
<p><h5>Template Set:</h5> Email templates for auto-responses and alerts.</p>
<p><h5>Auto-Responder Settings:</h5> Customize auto-replies for new tickets and messages.</p>
<p><h5>Auto-Response Email:</h5> Email used only for auto-replies.</p>
<p>The "Access" tab allows us add memebers to this department. </p>
</p>

<p>
  <h2>Configuring Teams</h2>
</p>


<p>
  Configure Teams(Pull Agents from different Departments)<br />
got to -> Admin Panel -> Agents -> Teams -> Add New Team

</p>

![image](https://github.com/user-attachments/assets/9c6b0a08-5991-462a-8810-51e651fd0496)

<br />

<p>
  Teams in osTicket allow agents from different departments to collaborate on specific issues or users via Help Topics or Ticket Filters. Team assignments override department-based access rules, enabling specialists from various departments to work together on designated tickets.
</p>
<p>
  
  ![image](https://github.com/user-attachments/assets/6a770270-def0-4e34-8c14-884b87df2401)

</p>

<p>
  For this example we will create a team specifically handeling a companies online app.

Note: In the Members tab you can assign different Agents to the team.
</p>

<p>
  <p><h2>Allow anyone to create tickets</h2></p>
  
<p>Admin Panel -> Settings -> User Settings<br />
  (UNCHECK: "Registration Required: Require registration and login to create tickets")<br />
  
  This will allow anyone to create a ticket, we will use this for examples later.
 </p>
<p>
  
  ![image](https://github.com/user-attachments/assets/a877e56f-5d4d-46c7-8a1f-c30b922489f1)

</p>

<p>
  <p>
    <h2>Configure Agents (Employees)</h2>
  </p>
Go to -> Admin Panel -> Agents -> Add New Agent<br />
Examples:<br />

Jenny Doe (Dept: System Administrator)<br />
Jorge Doe (Dept: Support)
<p>
  
  ![image](https://github.com/user-attachments/assets/78718cb0-b622-45cb-9462-171abe59e9e4)

  ![image](https://github.com/user-attachments/assets/b47fac8f-0c55-4cb6-bc2d-b552eff5268b)

  ![image](https://github.com/user-attachments/assets/31347891-18d3-4e35-abc2-59c52a28e913)


</p>
<p>
  <h3>Agent Access & Roles</h3>
  
Agents handle tickets and must be assigned a Primary Department and Primary Role for tasks within that department. Additional department access and roles can be configured in the Access tab of the Agent’s profile. Agents without direct department access can have Primary Role permissions for assigned or referred tickets if enabled; otherwise, they will have view-only access to those tickets.

<p><h3>Resetting an Agent’s Password</h3></p>
<p><h5>Admins can reset an agent’s password from the Account page:</h5></p>

<p>- Send a password reset email (only if the agent has previously set a password).</p>
<p>- Manually set a password and notify the agent. An option is available to force a password reset on the next login.</p>
<p><h3>Agent Status & Settings</h3></p>
<p>- Locked/Disabled: Agent cannot log in, receive assignments, or email alerts.</p>
<p>- Administrator: Grants access to the Admin Panel for global configurations.</p>
<p>- Limit Ticket Access: Restricts agents to only see tickets assigned directly to them or their team.</p>
<p>- Vacation Mode: Prevents ticket assignments and alerts while allowing login. Must be enabled/disabled manually.</p>
<p><h3>Agent Permissions</h3></p>
<p>- Users: Create, edit, delete users, and manage accounts.</p>
<p>- User Directory: View the list of users.</p>
<p>- Organizations: Create, edit, and delete organizations.</p>
<p>- Knowledgebase: Manage FAQs and categories.</p>
<p><h3>Miscellaneous:</h3></p>
<p>- Banlist: Add/remove emails.</p>
<p>- Search: View all tickets in search results.</p>
<p>- Stats: View agent statistics for permitted departments.</p>
</p>
</p>
</p>














<p>

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

