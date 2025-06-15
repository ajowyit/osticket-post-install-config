<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>⚠️ Prerequisites</h2>

- [Creating Virtual Machines in the Cloud](https://github.com/ajowyit/creating-virtual-machines)

- [osTicket: Prerequisites and Installation](https://github.com/ajowyit/osticket-prereqs)

<h2>💻 Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Windows App (macOS)
- Internet Information Services (IIS)
- osTicket

<h2>👨‍💻 Operating Systems Used</h2>

- macOS Sequoia
- Windows 10 (21H2)

<h2>📋 Post-Install Configuration Objectives</h2>

- Section 1: Intro to URLs and Admin Panel vs Agent Panel
- Section 2: [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
- Section 3: [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
- Section 4: [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html)
- Section 5: [Agents ](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html)& [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html)
- Section 6: [Service Level Agreements (SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)
- Section 7: [Help Topics](https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html)

<h2>🪜 Configuration Steps</h2>

<h3>Section 1: Intro to URLs and Admin Panel vs Agent Panel</h3>

<table>
  <tr>
    <td>
      <img width="780" alt="Screenshot 2025-06-13 at 12 02 21 AM" src="https://github.com/user-attachments/assets/479034b0-6635-415c-afaa-40735b0d18b4" />
    </td>
    <td>
     <img width="892" alt="Screenshot 2025-06-13 at 12 02 42 AM" src="https://github.com/user-attachments/assets/01cdda1a-879f-45aa-9ab3-dcb61f173798" />
    </td>
  </tr>
</table>
<p>
  - For osTicket there two main URLs that we will use for this project and the next one.
</p>
<p>
  - http://localhost/osTicket/scp - Your Staff Control Panel. This is used by Admins and the Help Desk Agents. </p>
<p>
  - Bookmark this page in the VM's browser. Name it something like: "osTicket Agent Portal"
</p>
<p>
  - http://localhost/osTicket.com - Your osTicket URL. This is for end users to create tickets and check ticket status.
</p>
<p>
  - Bookmark this page in the VM's browser. Name it something like: "osTicket Support Center Portal"
</p>

<p>
  <img width="773" alt="Screenshot 2025-06-13 at 12 05 26 AM" src="https://github.com/user-attachments/assets/0e9d5185-d571-496b-8278-ee9e7f5bfafc" />
</p>
<p>
  - Log in on the Staff Control Panel. Remeber from the previous porject that username is adminuser and password is Password1.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1024" alt="Screenshot 2025-06-13 at 12 06 15 AM" src="https://github.com/user-attachments/assets/35de6945-1d4a-4092-a94c-749f2d81470b" />
    </td>
    <td>
     <img width="1027" alt="Screenshot 2025-06-13 at 12 07 47 AM" src="https://github.com/user-attachments/assets/8d06f82d-78b9-4fc3-ab45-5438e57efc00" />
    </td>
  </tr>
</table>
<p>
  - Once logged into the Staff Control Panel URL, there are two different panels that can be used depending on your permissions, Admin Panel and Agent Panel.
</p>
<p>
  - Admin Panel - Used by the System Admin to confiured settings on the backend. 
</p>
<p>
  - Agent Panel - Used by the Help Desk Agents or Support Specialists to view and work tickets.
</p>
<p>
  - As an Admin, you can switch panels by clicking the panel name on the top right of the screen. We will jump between the two a lot throughout the project. Lets get started. 
</p>

<h3>Section 2: Roles</h3>

<table>
  <tr>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 12 12 34 AM" src="https://github.com/user-attachments/assets/35d07908-c3cc-45f7-9295-f355c74c0194" />
    </td>
    <td>
     <img width="1027" alt="Screenshot 2025-06-13 at 12 13 34 AM" src="https://github.com/user-attachments/assets/5be5ac57-9714-4e4f-85d4-ed24778e4f32" />
    </td>
  </tr>
</table>
<p>
  - We will configure a new role within the Admin Panel. (Remember, "Agent Panel" will display in the top-right of your screen while in the Admin Panel.)</p> 
<p>
  - In the Admin Panel, click Agents -> click Roles -> click +Add New Role.
</p> 
<p>
  - Name the new role "Supreme Admin". Then click the Permissions tab.
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="1027" alt="Screenshot 2025-06-13 at 12 14 12 AM" src="https://github.com/user-attachments/assets/08f7f408-2e4f-4c76-8275-2878281d393e" />
    </td>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 12 14 58 AM" src="https://github.com/user-attachments/assets/1b593618-0b95-4f2a-8793-0b5df8faf902" />
    </td>
  </tr>
</table>
<p>
  - For this project, we want the Supreme Admin Role to have all the permissions.</p>
<p>
  - Under Tickets, check all the boxes. Click "Tasks".
</p>
<p>
  - Under Tasks, check all the boxes again. Click "Knowledgebase".
</p>

<table>
  <tr>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 12 15 46 AM" src="https://github.com/user-attachments/assets/401e13ce-1d6a-4bc1-aa6c-f144460e957f" />
    </td>
    <td>
      <img width="1029" alt="Screenshot 2025-06-13 at 12 16 51 AM" src="https://github.com/user-attachments/assets/15572df7-8ffd-4087-8d5e-80a4c5147527" />
    </td>
  </tr>
</table>
<p>
  - Under Knowledgebase, check the one and only box and then click "Add Role".
</p>
<p>
  - You should see that the Supreme Admin Role was successfully added!
</p> 
<p>
  - Next, it is time to add a new Department.
</p>

<h3>Section 3: Departments</h3>

<table>
  <tr>
    <td>
      <img width="1026" alt="Screenshot 2025-06-13 at 12 25 39 AM" src="https://github.com/user-attachments/assets/515d3df6-d2b6-413c-bd16-7c5b028460fb" />
    </td>
    <td>
      <img width="1027" alt="Screenshot 2025-06-13 at 12 58 05 AM" src="https://github.com/user-attachments/assets/90afb357-de8c-40ca-8c08-9756c1c53fd6" />
    </td>
  </tr>
</table>
<p>
  <img width="1024" alt="Screenshot 2025-06-13 at 12 59 13 AM" src="https://github.com/user-attachments/assets/15b136aa-1e26-4079-a525-c05dc15941cd" />
</p>
<p>
  - Within Admin Panel, click Agents -> Departments -> click + Add New Department.
</p>
<p>
  - Under Settings, make sure you leave Parent as "Top-Level Department". Name the department "SysAdmins".
</p>
<p>
  -Scroll down and click Create.
</p>
<p>
<img width="1028" alt="Screenshot 2025-06-13 at 1 00 13 AM" src="https://github.com/user-attachments/assets/0d03b026-5d9d-473d-aad5-ad1cf0ed99a3" />
</p>
<p>
  - Confirm that the SysAdmins Department has been successfully added. 
</p>
<p>
  - Next we will add a new Team!
</p>
<br />

<h3>Section 4: Teams</h3>

<table>
  <tr>
    <td>
      <img width="1024" alt="Screenshot 2025-06-13 at 1 13 57 AM" src="https://github.com/user-attachments/assets/07bf65f4-86ed-4e05-bafe-a1734c066c5b" />
    </td>
    <td>
      <img width="1026" alt="Screenshot 2025-06-13 at 1 16 32 AM" src="https://github.com/user-attachments/assets/3717a133-793e-4986-bb4c-48c67cda59ff" />
    </td>
  </tr>
</table>
<p>
  - Within Admin Panel, click Agents -> Teams -> + Add New Team.
</p>
<p>
  - Name the Team "Online Banking". 
</p>
<p>
  - Click "Create Team".
</p>
<p>
  <img width="1024" alt="Screenshot 2025-06-13 at 1 17 38 AM" src="https://github.com/user-attachments/assets/fe888398-2735-44f8-b786-7f6a025093ca" />
</p>
<p>
  - Confirm that the team was successfully added.
</p>


</p>


<table>
  <tr>
    <td>
      <img width="1026" alt="Screenshot 2025-06-13 at 1 18 31 AM" src="https://github.com/user-attachments/assets/9a527b6d-3880-4ef4-90d9-aa68d8c97406" />
    </td>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 1 18 59 AM" src="https://github.com/user-attachments/assets/cea4b02c-440b-4376-a038-0965b4a318e1" />
    </td>
  </tr>
</table>
<p>
  - Next, configure the settings so that somone is allowed to create a ticket without having to register an account. The end user will be able to create their own ticket.
</p>
<p>
  - From Admin Panel, click Settings -> Users -> go to the Settings tab.
</p>
<p>
  - Under Authentication Settings, make sure the box next to "Require registration and login to create tickets" is unchecked. "Click Save Changes".
</p>
<br />

<h3>Section 5: Agents and Users</h3>

<table>
  <tr>
    <td>
      <img width="1032" alt="Screenshot 2025-06-13 at 9 12 06 AM" src="https://github.com/user-attachments/assets/70ed1cbb-cf67-4751-a43c-17d7727424de" />
    </td>
    <td>
     <img width="1019" alt="Screenshot 2025-06-13 at 9 13 21 AM" src="https://github.com/user-attachments/assets/92f7bb7f-b8b0-40b3-a623-0fc5e10af22e" />
    </td>
  </tr>
</table>
<p>
  - Now it is time to add some Agents! From the Admin Panel, click -> Agents -> Agents -> + Add New Agent. 
</p>
<p>
  - Under Account, name the Agent "Jane Doe". Enter a some fake email address(It doesn't matter what email you use here).  
</p>
<p>
  - Username: jane_doe 
</p>
<p>
  - Click "Set Password". 
</p>

<p>
<img width="1021" alt="Screenshot 2025-06-13 at 9 15 12 AM" src="https://github.com/user-attachments/assets/877283be-9245-4927-9142-f2700e0626c7" />
</p>

<p>
  - When you click Set Password a pop-up will appear. Uncheck the box next to "Send the agent a password reset email".
</p>
<p>
  - Set password to "Password1". Uncheck "Require password change at next login". Click "Set". 
</p>

<table>
  <tr>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 9 17 12 AM" src="https://github.com/user-attachments/assets/bb48f8fa-3809-4a39-9314-8f98a3a5415a" />
    </td>
    <td>
      <img width="1025" alt="Screenshot 2025-06-13 at 9 17 58 AM" src="https://github.com/user-attachments/assets/559b6a11-e0fc-454c-a1eb-1eac8027eb75" />
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
     <img width="1026" alt="Screenshot 2025-06-13 at 9 18 42 AM" src="https://github.com/user-attachments/assets/9831316f-421e-4288-b76f-a0cf375cd71e" />
    </td>
    <td>
      <img width="1024" alt="Screenshot 2025-06-13 at 9 19 30 AM" src="https://github.com/user-attachments/assets/a80f4543-7354-4a1a-bb72-5c2e6424cf7b" />
    </td>
  </tr>
</table>
  
<p>
  - Under Agents -> Access -> Primary Department, select SysAdmins. For Role/Permissions, select Supreme Admin. </p>
<p>
  - Under Teams, select Online Banking, click "Add" and then click "Create".  
</p>

<table>
  <tr>
    <td>
     <img width="1026" alt="Screenshot 2025-06-13 at 9 19 50 AM" src="https://github.com/user-attachments/assets/92b1fa0c-24ef-454e-a0fb-7be7f2effe6b" />
    </td>
    <td>
      <img width="1024" alt="Screenshot 2025-06-13 at 9 21 52 AM" src="https://github.com/user-attachments/assets/3d149cc2-fbf9-45ea-af72-bc05c92a1ee9" />
    </td>
  </tr>
</table>

<p>
  - Add another Agent by clicking + Add New Agent.
</p>
<p>
  - Under Account, name the Agent "John Doe". Enter a fake email.  
</p>
<p>
  - Username: john_doe 
</p>
<p>
  - Click "Set Password". 
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="1020" alt="Screenshot 2025-06-13 at 9 27 13 AM" src="https://github.com/user-attachments/assets/73a7251f-81bd-45ff-96b9-2642b26cf6ee" />
    </td>
    <td>
      <img width="1026" alt="Screenshot 2025-06-13 at 9 35 21 AM" src="https://github.com/user-attachments/assets/098d9fda-1143-4076-adef-013a4c5d5c6a" />
    </td>
  </tr>
</table>

<p>
  - Just like before, when you click Set Password a pop-up will appear.
</p>
<p>
  - Uncheck the box next to "Send the agent a password reset email".
</p>
<p>
  - Set password to "Password1". Uncheck "Require password change at next login". Click "Set". 
</p>
<p>
  - Under Access -> Primary Department -> select Support. For Role/Permissions, select Expanded Access. Click "Create".
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="1025" alt="Screenshot 2025-06-13 at 9 36 39 AM" src="https://github.com/user-attachments/assets/6349ac0d-f2da-4368-bbaf-3aa0099da895" />
    </td>
    <td>
      <img width="1031" alt="Screenshot 2025-06-13 at 9 36 48 AM" src="https://github.com/user-attachments/assets/807497eb-bf45-4300-a02c-cb0974a3c595" />
    </td>
  </tr>
</table>

<p>
  - Our Agents have been added. We'll work tickets with both in the next project! 
</p>

<br/>

<table>
  <tr>
    <td>
      <img width="1032" alt="Screenshot 2025-06-13 at 9 37 14 AM" src="https://github.com/user-attachments/assets/b1a43c1b-cdeb-4f0b-a84c-13bae9e58f52" />
    </td>
    <td>
      <img width="649" alt="Screenshot 2025-06-13 at 9 39 09 AM" src="https://github.com/user-attachments/assets/695bac83-64b3-4ee9-9261-add26d3dfb3f" />
    </td>
  </tr>
</table>
<p>
  - Now, we need to add a User. Click Agent Panel at the top-right of the screen.
</p>
<p>
  - Once we are in the Agent Panel, click Users -> click + Add User.  
</p>
<p>
  - In the Email Address field, enter theemail address, karen@lonpacific.com (Fake Email).
</p>
<p>
  - Name the User "Karen" and click "Add User".
</p>
<br/>

<p>
<img width="1030" alt="Screenshot 2025-06-13 at 9 39 51 AM" src="https://github.com/user-attachments/assets/f3944616-1248-4f41-b1c1-fdb58473f0fa" />
</p>

<p>
  - Karen has been added as a User!
</p>
<p>
  - We'll have Karen creating tickets for our Agents in the next project. 
</p>
<p>
  - Click Admin Panel before starting the next Section.
</p>
<br/>

<h3>Section 6: Service Level Agreements (SLA)</h3>

<p>
<img width="1030" alt="Screenshot 2025-06-13 at 9 43 05 AM" src="https://github.com/user-attachments/assets/7c73749d-3866-43dd-bd17-2ac97294cbd5" />

</p>

<p>
  - The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.
</p>
<p>
  - From Agent Panel, click Manage -> SLA -> + Add New SLA Plan.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1029" alt="Screenshot 2025-06-13 at 9 47 42 AM" src="https://github.com/user-attachments/assets/38f560f9-cea5-415a-8be7-83ee61802fad" />
    </td>
    <td>
      <img width="1030" alt="Screenshot 2025-06-13 at 9 48 30 AM" src="https://github.com/user-attachments/assets/5e550720-1766-45dd-b322-b690189de88d" />
    </td>
  </tr>
</table>

<p>
  - For the first SLA enter the following info:
</p>
<p>
  - Name: "Sev-A" | Grace Period: 1 hour | Schedule: 24/7
</p>
<p>
  - Click "Add Plan".
</p>
<p>
  - We will be taken back to the Service Level Agreements page where we see a confimation that we sucessfully added a SLA plan. Click "+ Add New Plan" to add another SLA. 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1032" alt="Screenshot 2025-06-13 at 9 51 55 AM" src="https://github.com/user-attachments/assets/95f04cf6-597c-49d6-af5e-8a3667722d06" />
    </td>
    <td>
      <img width="1030" alt="Screenshot 2025-06-13 at 9 52 44 AM" src="https://github.com/user-attachments/assets/3497ce38-385b-4409-92cc-d8c817e9ca12" />
    </td>
  </tr>
</table>

<p>
  - For the next SLA enter the following info:
</p>
<p>
  - Name: "Sev-B" | Grace Period: 4 hours | Schedule: 24/7</p>
<p>
  - Click Add Plan.</p>
<p>
  - We will be taken back to the Service Level Agreements page where we see a confimation that we sucessfully added a SLA plan. Click "+ Add New Plan" to add another SLA. 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1028" alt="Screenshot 2025-06-13 at 9 53 16 AM" src="https://github.com/user-attachments/assets/a9e9c732-edbe-4332-b70c-cccd8c0a2340" />
    </td>
    <td>
      <img width="1030" alt="Screenshot 2025-06-13 at 9 54 05 AM" src="https://github.com/user-attachments/assets/eb9daefa-4eba-49b9-9026-1dc9c036d6e7" />
    </td>
  </tr>
</table>

<p>
  - For the next SLA enter the following info:
</p>
<p>
  - Name: "Sev-C" | Grace Period: 8 hours | Schedule: Monday - Friday, 8am - 5pm with Holidays. (Normal business hours)
</p>
<p>
  - Click Add Plan.
</p>
<br/>

<p>
  - The SLA Plans have been successfully added. We will use these when creating and working tickets in the next project.
</p>

<br/>

<h3>Section 7: Help Topics</h3>

<p>
<img width="750" alt="PI34" src="https://github.com/user-attachments/assets/6194a8bb-0051-46e3-b109-f50b3938e254" />
</p>

<p>- For the final section of this project, we will add some Help Topics.</p>
<p>- From Agent Panel, click Manage -> Help Topics -> + Add New Help Topic. <p/>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI35" src="https://github.com/user-attachments/assets/9df07a0d-2cbd-4ee1-9886-aff4c4f42304" />
    </td>
    <td>
      <img width="1000" alt="PI36" src="https://github.com/user-attachments/assets/51bc7442-76e0-47ae-9f11-ad9da82ea9e8" />
    </td>
  </tr>
</table>
<p>- Under Help Topic Information, Topic: Buisness Critical Outage | Parent Topic: Report a Problem. See Figure 35</p>
<p>- Click Add Topic.  </p>
<p>- Under Help Topic Information, Topic: Personal Computer Issues | Parent Topic: Report a Problem. See Figure 36</p>
<p>- Click Add Topic.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI37" src="https://github.com/user-attachments/assets/8e46c387-782d-4c93-8634-8deb4f3e0eb9" />
    </td>
    <td>
      <img width="1000" alt="PI38" src="https://github.com/user-attachments/assets/44622da8-fd2a-4d81-8677-18cfec813ff6" />
    </td>
  </tr>
</table>
<p>- Under Help Topic Information, Topic: Equipment Request | Parent Topic: General Inquiry. See Figure 37</p>
<p>- Click Add Topic. </p>
<p>- Under Help Topic Information, Topic: Password Reset | Parent Topic: Report a Problem. See Figure 38</p>
<p>- Click Add Topic. </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI39" src="https://github.com/user-attachments/assets/2c81095c-4f59-4c35-8056-8e19460a5c69" />
    </td>
    <td>
      <img width="1000" alt="PI40" src="https://github.com/user-attachments/assets/77f141a2-0575-4ece-9140-e571d166cd1b" />
    </td>
  </tr>
</table>
<p>- Under Help Topic Information, Topic: Other | Parent Topic: General Inquiry. See Figure 39</p>
<p>- Click Add Topic.  </p>
<p>- Look at all those Topics!. If you noticed, osTicket already had some deafult Help Topics preloaded for us but adding new ones gave us a chance to learn more about the process.</p>
<p>- You can learn more about Help Topics within osTicket by clicking the link in the Post-Install Configuration Objectives above.<p/>
<br/>

<h2>Conclusion</h2>

<p>This concludes our project. We have successfully completed the post-install configurations for osTicket. We will put our settings to the test in the next lab when we create and work tickets as a User, Agent, and Admin. Don't forget to Stop (turn off) the VMs in Azure. As always, Thank You for your time and viewing this Project. We'll see you on the next one! 😎      
</p>
<br />


