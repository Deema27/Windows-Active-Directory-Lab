# Windows-Active-Directory-Lab
This project documents my hands-on learning from the TryHackMe: Active Directory Basics room, which introduces fundamental concepts of Active Directory in a practical, lab-based environment. The room covers core topics such as domain structures, user and group management, Remote Desktop Protocol usage, PowerShell for AD administration, and Group Policy Objects. Through interactive exercises, I explored how Active Directory operates within a Windows domain, how to manage users with PowerShell, and how to apply policies using GPOs. These skills provide a solid foundation for effectively supporting and administering Windows-based network infrastructures.

# Skills Learned
- Active Directory Fundamentals
- User & Account Management
- System Administration
- Group Policy Management
- PowerShell for AD Administration

# Project Walkthrough

In this task, I deleted an Organizational Unit (OU) by first enabling advanced features in Active Directory and disabling the built-in protection against accidental deletion. It taught me how to safely handle protected objects without risking the loss of important accounts.

<img width="555" height="464" alt="Screenshot 2025-09-20 165730" src="https://github.com/user-attachments/assets/212ca726-e6b0-46aa-a760-836a86294ffa" />


---------------------------------------------------------------------------------------------------------------------------------------------------------------------


I also practiced disabling and deleting users from Active Directory, which are essential tasks for securely offboarding employees and managing inactive accounts to maintain organizational security. These actions help prevent unauthorized access and ensure that only active, authorized users have entry to network resources.

<img width="554" height="464" alt="Screenshot 2025-09-20 170010" src="https://github.com/user-attachments/assets/a2c31d16-711f-4d1d-bf54-0409442814bb" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


I practiced delegating control in Active Directory, allowing specific users to perform limited administrative tasks without giving them full domain privileges. This is especially useful in larger environments where responsibilities are split among help desk staff or department leads. It taught me how to assign permissions safely and effectively, which is key for maintaining security while still enabling teams to manage their own resources.

<img width="550" height="463" alt="Screenshot 2025-09-20 170345" src="https://github.com/user-attachments/assets/966c309a-0049-46e5-af51-910c132def9d" />

<img width="552" height="458" alt="Screenshot 2025-09-20 170537" src="https://github.com/user-attachments/assets/43b02e92-8ed0-436c-b4b6-9a56a55886ed" />

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


I then used Remote Desktop Protocol to log into a delegated user’s account and tested the permissions by resetting and changing another user's password. This confirmed that the delegated control was set up correctly and helped me understand how permission changes apply in practice. It’s a valuable skill for verifying access rights and ensuring that delegated roles have the appropriate level of control without over-privileging users.

<img width="554" height="465" alt="Screenshot 2025-09-20 171526" src="https://github.com/user-attachments/assets/0eb8844b-baac-426a-b6e9-6d63fa26dfe3" />


<img width="551" height="461" alt="Screenshot 2025-09-20 171751" src="https://github.com/user-attachments/assets/c17f9c52-65ef-4523-aa49-e368ce7aa174" />


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


I created two new OUs named Workstations and Servers to organize computer objects more effectively within Active Directory. I moved all PCs and laptops into the Workstations OU and placed the servers into the Servers OU. This kind of structure makes it easier to manage devices at scale, apply group policies based on device roles, and keep the directory organized.


<img width="550" height="457" alt="Screenshot 2025-09-20 175126" src="https://github.com/user-attachments/assets/a9d83dbc-d0f7-4f99-ae09-97da0ab9445c" />


<img width="552" height="464" alt="Screenshot 2025-09-20 175136" src="https://github.com/user-attachments/assets/24b45037-8396-4b4a-af9a-6cd4f129b968" />


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


I reviewed the existing Group Policy Objects (GPOs) and edited the Default Domain Policy to strengthen the domain's password requirements by increasing the minimum password length from 7 to 12 characters. This change helps enforce better security standards across all user accounts in the domain.


<img width="552" height="464" alt="Screenshot 2025-09-20 181001" src="https://github.com/user-attachments/assets/a4d5d3b1-3a8f-4302-9f2f-70b439c58348" />

<img width="551" height="459" alt="Screenshot 2025-09-20 181020" src="https://github.com/user-attachments/assets/50a4b241-8e4d-4919-8bb8-71faf2bc9bc2" />

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


I was tasked with blocking non-IT users from accessing the Control Panel. To accomplish this, I created a new GPO and configured the necessary settings to restrict access. Afterward, I linked the GPO to the relevant OUs to ensure the policy applied only to the intended users. This exercise demonstrated how targeted policies can be used to enforce security and limit user actions, a vital skill for managing permissions and maintaining control in an enterprise environment.

<img width="556" height="464" alt="Screenshot 2025-09-20 183204" src="https://github.com/user-attachments/assets/4d9ce2f1-3b30-4036-83b9-d5c5ef8b2c18" />

<img width="552" height="466" alt="Screenshot 2025-09-20 181848" src="https://github.com/user-attachments/assets/bdfdf303-4452-4e41-b411-dec662ce6759" />

<img width="548" height="458" alt="Screenshot 2025-09-20 183406" src="https://github.com/user-attachments/assets/4d8274c8-4cf9-4b54-99d0-56a84b922278" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


The next task was to ensure that workstations and servers automatically lock their screens after 5 minutes of user inactivity to prevent unattended sessions from being exploited. I created a new GPO, configured the security settings to enforce a 5-minute inactivity timeout, and linked the GPO to the root domain so it applied to all computers. This hands-on experience highlighted how policies can enhance security by reducing the risk of unauthorized access in a corporate environment.


<img width="548" height="462" alt="Screenshot 2025-09-20 184356" src="https://github.com/user-attachments/assets/ef174f92-b25b-438c-a244-0c89e1146e14" />

<img width="552" height="464" alt="Screenshot 2025-09-20 184444" src="https://github.com/user-attachments/assets/85254033-a1f7-4423-9852-79c717deffdd" />

# Conclusion

This hands-on experience taught me how to securely manage users, devices, and permissions within a domain. I practiced deleting protected objects, offboarding users, delegating control, and verifying permissions using RDP. Organizing computers into OUs and applying targeted Group Policies highlighted how structured AD management enhances both security and efficiency in enterprise environments.








