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
      <img width="1000" alt="PI11" src="https://github.com/user-attachments/assets/772d618b-3fad-48bf-940a-e3f982b49607" />
    </td>
    <td>
      <img width="1000" alt="PI12" src="https://github.com/user-attachments/assets/65a769eb-fa93-4e87-b451-313259b93378" />
    </td>
  </tr>
</table>
<p>- Within Admin Panel, click Agents -> Departments -> + Add New Department.</p>
<p>- Under Settings, leave Parent as "Top-Level Department" and name the department "SysAdmins".</p>
<p>- This is all we'll do here for now. Ignore the Access tab for now because we still need to create some Agents. Scroll down and click Create.</p>

<p>
<img width="950" alt="PI13" src="https://github.com/user-attachments/assets/f46cdfbf-b156-4c04-9db0-ad821f1dc962" />

</p>

<p>- The SysAdmins Department has been successfully added. </p>
<p>- You can learn more about Departments within osTicket by clicking the link in the Post-Install Configuration Objectives above. </p>
<br />

<h3>Section 4: Teams</h3>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI14" src="https://github.com/user-attachments/assets/8f5c3b1e-281a-464b-8d0b-3c01dba6aea1" />
    </td>
    <td>
      <img width="1000" alt="PI15" src="https://github.com/user-attachments/assets/928db42c-ffd0-4013-9b4b-c0dc0465d0c3" />
    </td>
  </tr>
</table>
<p>- Now, we'll add a new Team. Within Admin Panel, click Agents -> Teams -> + Add New Team.</p>
<p>- Name the Team "Online Banking". </p>
<p>- We'll will add members when we add Agents later. Click Create Team.</p>
<p>- You can learn more about Teams within osTicket by clicking the link in the Post-Install Configuration Objectives above.</p>

<p>
<img width="750" alt="PI16" src="https://github.com/user-attachments/assets/6ae0c661-15b2-42ac-8cad-621ad6df1585" />

</p>

<p>- Next, we'll change a setting that will allow somone to create a ticket without having to register an account. The end user will be able to create thier own ticket. </p>
<p>- From Admin Panel, click Agents -> Settings -> Users. </p>
<p>- Under Authentication Settings, uncheck the box next to "Require registration and login to create tickets". Click Save Changes.</p>
<br />

<h3>Section 5: Agents and Users</h3>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI17" src="https://github.com/user-attachments/assets/8ee3d34d-625e-464d-86b3-221df3da96de" />
    </td>
    <td>
      <img width="1000" alt="PI18" src="https://github.com/user-attachments/assets/d69937e8-a664-49d4-843e-fa82dd1c710e" />
    </td>
  </tr>
</table>
<p>- Time to add some Agents. From Admin Panel, click -> Agents -> Agents -> + Add New Agent. </p>
<p>- Under Account, name the Agent "Jane Doe". Enter a fake email (Doesn't matter but I stuck with the Help Desk company theme).  </p>
<p>- Username: jane_doe </p>
<p>- Click Set Password. </p>

<p>
<img width="750" alt="PI24" src="https://github.com/user-attachments/assets/94f4d00e-dbc4-4570-b7a9-c0542c1f9461" />

</p>

<p>- When you click Set Password a pop-up will appear. Uncheck the box next to "Send the agent a password reset email" and you'll see Figure 19. </p>
<p>- Set password to "Password1". Uncheck "Require password change at next login". Click Update. </p>
<p>- You will need to do this when we create the next Agent (John) as well.  </p>


<table>
  <tr>
    <td>
      <img width="1000" alt="PI19" src="https://github.com/user-attachments/assets/45b36bfc-d0ec-4683-96f2-8dfb095483f1" />
    </td>
    <td>
      <img width="1000" alt="PI20" src="https://github.com/user-attachments/assets/290cb12c-0d0a-49d2-8b35-c13d9a3a98d2" />
    </td>
  </tr>
</table>
<p>- Under Access -> Primary Department, select SysAdmins. For Role/Permissions, select Supreme Admin. </p>
<p>- Under Teams, select Online Banking and click Create.  </p>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI21" src="https://github.com/user-attachments/assets/284f42e3-85c1-42b0-849b-5b56e872d03b" />
    </td>
    <td>
      <img width="1000" alt="PI22" src="https://github.com/user-attachments/assets/23f573c1-0166-4469-beb2-9fac9de404ca" />
    </td>
  </tr>
</table>
<p>- Add another Agent by clicking + Add New Agent.</p>
<p>- Under Account, name the Agent "John Doe". Enter a fake email.  </p>
<p>- Username: john_doe </p>
<p>- Click Set Password. </p>
<br/>

<p>
<img width="750" alt="PI24" src="https://github.com/user-attachments/assets/94f4d00e-dbc4-4570-b7a9-c0542c1f9461" />
</p>

<p>- As before, when you click Set Password a pop-up will appear.</p>
<p>- Uncheck the box next to "Send the agent a password reset email" and you'll see Figure 19. </p>
<p>- Set password to "Password1". Uncheck "Require password change at next login". Click Update. </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI23" src="https://github.com/user-attachments/assets/36b38331-2e76-44f5-94ad-42d49677d971" />
    </td>
    <td>
      <img width="1000" alt="PI25" src="https://github.com/user-attachments/assets/29814cd4-93f5-4fbe-b3b2-487095432d5b" />
    </td>
  </tr>
</table>
<p>- Under Access -> Primary Department -> select Support. For Role/Permissions, select Expanded Access. Click Create.</p>
<p>- Our Agents have been added. We'll work tickets with both in the next project. </p>
<p>- I know Figure 24 shows "View Only" for John Doe's Role, but that created some issues while trying to work tickets. I had to go back and change it while I was working on the project we'll do next. Changing it to Expanded Access seemed to fix the issue.😉  </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="PI26" src="https://github.com/user-attachments/assets/b680df79-e884-44f9-a47d-c3fce3a584e4" />
    </td>
    <td>
      <img width="1000" alt="PI27" src="https://github.com/user-attachments/assets/4d6f7fe4-67f1-4c82-bec7-9ccd75952be8" />
    </td>
  </tr>
</table>
<p>- Now, we need to add a User. Click Agent Panel at the top-right of the screen.</p>
<p>- From Agent Panel, click Users -> + Add User.  </p>
<p>- Enter email address: karen@lonpacific.com (Fake Email).</p>
<p>- Name the User "Karen" and click Add User. </p>
<br/>

<p>
<img width="750" alt="PI28" src="https://github.com/user-attachments/assets/c98344cd-3bd6-4ff3-a461-85e2b2955beb" />
</p>

<p>- Karen has been added as a User.</p>
<p>- We'll have Karen creating tickets for our Agents in the next project. </p>
<p>- Set password to "Password1". Uncheck "Require password change at next login". Click Update. </p>
<p>- You can learn more about Agents and Users within osTicket by clicking the link in the Post-Install Configuration Objectives above.<p/>
<p>- Click Agent Panel and start the next Section.</p>
<br/>

<h3>Section 6: Service Level Agreements (SLA)</h3>

<p>
<img width="750" alt="PI29" src="https://github.com/user-attachments/assets/a7b03923-b42d-4cc0-bcbb-b07a5c0a23e4" />
</p>

<p>- The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.</p>
<p>- From Agent Panel, click Manage -> SLA -> + Add New SLA Plan.</p>
<br/>

<p>
<img width="750" alt="PI30" src="https://github.com/user-attachments/assets/88a03023-8a2e-4ccb-ac6b-b05cd4e11d9c" />
</p>

<p>- Name: "Sev-A" | Grace Period: 1 hour | Schedule: 24/7</p>
<p>- Click Add Plan.</p>
<br/>

<p>
<img width="750" alt="PI31" src="https://github.com/user-attachments/assets/4e4c2490-7452-4493-90ff-00fbeb4e47a2" />
</p>

<p>- Name: "Sev-B" | Grace Period: 4 hours | Schedule: 24/7</p>
<p>- Click Add Plan.</p>
<br/>

<p>
<img width="750" alt="PI32" src="https://github.com/user-attachments/assets/bda12229-512b-42be-9b98-dffceb4b7062" />
</p>

<p>- Name: "Sev-C" | Grace Period: 8 hours | Schedule: Monday - Friday, 8am - 5pm with Holidays. (Normal business hours)</p>
<p>- Click Add Plan.</p>
<br/>

<p>
<img width="750" alt=<img width="975" alt="PI33" src="https://github.com/user-attachments/assets/49b09cf1-5465-4fa0-9b5d-5ce2eb5996c6" />
</p>

<p>- The SLA Plans have been successfully added. We will use these when creating and working tickets in the next project.</p>
<p>- You can learn more about Service Level Agreements within osTicket by clicking the link in the Post-Install Configuration Objectives above.<p/>
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


