<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Agent Roles & Permissions
- Department creation (top-level vs. nested)
- Team creation (cross-department collaboration)
- SLA Plans (Sev-A, Sev-B, Sev-C)
- Help Topics (e.g., Business Critical Outage, Equipment Request)

<h2>Configuration Steps</h2>
<p>
Admin vs. Agent Panel
<p>
After logging in with admin credentials, you briefly compared the Admin Panel (system-wide settings) vs. the Agent Panel (daily ticket operations).
<p>
<img width="894" alt="image" src="https://github.com/user-attachments/assets/9b13242a-34db-439c-9395-3e274c5d430c" />
<p>
Creating a New Role: Supreme Admin  
</p>
In Agents > Roles, I clicked +Add New Role and named it Supreme Admin, granting full permissions (Tickets, Tasks, Knowledgebase) as a demonstration of maximum privileges.
</p>
<img width="568" alt="image" src="https://github.com/user-attachments/assets/c524ed28-a5e9-4055-805a-7af98e911bd7" />
<img width="560" alt="image" src="https://github.com/user-attachments/assets/c1ec779a-e2d9-4b52-9868-a9499748e659" />
<p>
 Reviewing Other Roles 
<p>
osTicket comes with default roles like Limited Access or View Only. I quickly reviewed their permissions to see how they differ from the new Supreme Admin.  
</p>
<img width="882" alt="image" src="https://github.com/user-attachments/assets/82aa1fea-ffe8-43b0-8e78-7c6a47aa808d" />
<p>
Departments Setup  
<p>
Departments group agents by function (e.g., Support, Billing, SysAdmins). Under Agents > Departments, I clicked +Add New Department and named one Sysadmin, setting its parent to Top-Level.  
<p>
<img width="558" alt="image" src="https://github.com/user-attachments/assets/efec2907-b536-4c7c-8f06-a1140d8abf2f" />
<p>
Teams Setup  
<p>
Teams can span multiple departments. Under Agents > Teams, I added a new team named Online Banking so that agents from different departments can collaborate on banking-related tickets.  
</p>  
<img width="623" alt="image" src="https://github.com/user-attachments/assets/a3f276b6-0e55-429d-aa51-3c6588192b72" />
</p>
Editing User Registration Settings
<p>
 In Admin Panel > Settings > Users, I unchecked Registration Required so that unregistered users can still create tickets. This helps in scenarios where quick ticket creation is vital. 
<p>
<img width="616" alt="image" src="https://github.com/user-attachments/assets/4d7a51f2-dbd5-4249-ab3c-8bfe349b1d77" />  
<p>
Creating Agents  
<p>
Under Agents > +Add New Agent, I created:
-Jane Doe – Department: Sysadmin, Role: Supreme Admin, Team: Online Banking
-John – Department: Support, Role: View Only    
</p>  
<img width="786" alt="image" src="https://github.com/user-attachments/assets/020c923f-752e-4b38-b2ee-6e2f56e21187" />
<img width="899" alt="image" src="https://github.com/user-attachments/assets/80054e71-6c8a-4b1e-9a77-f1dcee75e16f" />
<img width="904" alt="image" src="https://github.com/user-attachments/assets/86abf819-1996-45a2-9ab6-e5dd4153bbcb" />
</p>
Creating End Users from the Agent Panel
<p>
From the Agent Panel > Users > +Add User, I added at least two end users (Ken & Karen). End users can open tickets without needing agent-level permissions.
<p>
<img width="857" alt="image" src="https://github.com/user-attachments/assets/dd36b5ae-9cad-42ef-810a-d9ecd3ad0786" />
<img width="897" alt="image" src="https://github.com/user-attachments/assets/3bf191df-6a12-4da7-870a-7de80dffc896" />
<p>
Configuring SLA Plans    
<p> 
Under Manage > SLA, I created:
-Sev-A – 1-hour grace, 24/7 schedule
-Sev-B – 4-hour grace, 24/7
-Sev-C – 8-hour grace, M-F 8am-5pm + holidays  
</p> 
<img width="602" alt="image" src="https://github.com/user-attachments/assets/f0ce40b8-e1a1-4ee3-8816-d6ce61ee2bf4" />
<img width="897" alt="image" src="https://github.com/user-attachments/assets/1a04706e-b452-4ca4-a7a9-ec0796fc20e7" />
</p>
Defining Help Topics
<p>
Finally, in Manage > Help Topics, I added:
-Business Critical Outage (parent: Report a Problem)
-Personal Computer Issues (parent: Report a Problem)
-Equipment Request (parent: General Inquiry)
-Password Reset (parent: Report a Problem)
-Other (parent: General Inquiry)  
<p>
<img width="538" alt="image" src="https://github.com/user-attachments/assets/0f55583c-8bca-44d7-a94d-244ef87c0d45" />
<img width="620" alt="image" src="https://github.com/user-attachments/assets/437b816c-712d-413e-b6ed-9516993cd7e1" />  
</p>  
</p>
CONCLUSION
By setting up roles, departments, teams, SLAs, and help topics, I prepared osTicket for a real-world help desk environment. Agents now have the correct permissions, tickets can be escalated according to SLA urgency, and end users have relevant categories to classify their requests
<p>
  
