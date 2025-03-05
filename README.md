<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory
- Create a domain admin user within the domain
- Join the client pc to the domain
- Set up remote desktop for non-administrative users on the client PC
- Create additional users and attempt to log into client pc with one of the users

<h2>Deployment and Configuration Steps</h2>


<p>
<img src="https://github.com/user-attachments/assets/08fe7bc0-00b4-45b6-a60b-b9dae65784af" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/6c0f940e-ba1a-474f-9d8e-9dc39b6568d6" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/814ea2ba-baab-4575-9a64-ae8847485a40" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/1106b4bc-e61b-466b-a7ae-12bffcfc2bac" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/6b6a6954-575e-480a-8e36-269841d01a7c" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/6f100518-a1e3-42ac-b7ba-c2dc1976d0d1" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/ba6a0217-5841-489d-acd1-d59670439f98" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/4fadc61d-6997-4fca-8105-0e074d8cf081" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/9fc90433-b0ef-46de-860c-2a66a526ae95" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/f67eb13e-b973-4db3-a05e-66479394a905" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/e75d096d-34c4-419b-9640-521b8583c172" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/a19f6e8c-449a-4cfb-904f-ba1ade875bd4" height="80%" width="80%" </>

</p>
<p>
Log into domain pc and install Server Manager.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/3270c83d-7dd9-4af4-8c4d-5863b3306e5f" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/d2b5a299-f9ce-4958-88e7-671c508ba639" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/bb967c5a-0353-473d-af3d-f89697526b22" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/f39302fb-62c3-4dfe-a2dd-0340dcb06c72" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/0d1a2605-7e16-40a5-af64-0d04d46e44c1" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/66454710-dbe8-41a7-9e51-ba8367357233" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/1a29518d-096b-47dd-a202-31977e4f4870" height="80%" width="80%" </>

  c
</p>
<p>
With the Active Directory services installed, we will promote the server to a domain controller. The system will automatically restart upon installation.
</p>
<br />




<p>
<img src="https://github.com/user-attachments/assets/2fcd80ef-c0b3-49b1-b72e-d5252db7819c" height="80%" width="80%" </>

</p>
<p>
Since the server is a domain controller now, when we log in, we have to specify the context to which we want to log in to it.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/bca49d84-30b2-4b3c-a5de-b40714fa1510" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/2fe52547-c491-4b70-953b-a280b37cdd07" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/c6c3c64d-061d-4239-9165-d003961d6707" height="80%" width="80%" </>

</p>
<p>
Now it's time to create a domain admin user within the domain. *NOTE* It's very important that your organizational unit is named correctly so that any references that call back to this folder name won't fail!
</p>
<br />




<p>
<img src="https://github.com/user-attachments/assets/7a283e7d-3ca1-4211-b713-27315774e0f2" height="80%" width="80%" </>


</p>
<p>
2 new organizational units created
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/a19e5d6a-bf5b-4109-b794-1b44e3d6732a" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/58204c2f-195b-4e93-99ca-b1c2071e44fc" height="80%" width="80%" </>
<img src="https://github.com/user-attachments/assets/728cefea-83a4-43c4-a006-143154c1629c" height="80%" width="80%" </>


</p>
<p>
A new administrator user is being added
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/7b94fe98-3709-4f09-b71c-b127d65050db" height="80%" width="80%" </>


</p>
<p>
The new user must be added to the domain admin security group to have admin privileges. We do this by right clicking on the newly created user, clicking "Member of" tab, and then clicking the "Add" button and typing the correct domain name.
</p>
<br />




<p>
<img src="" height="80%" width="80%" </>


</p>
<p>
Now, we will log out and log back in as the newly created administrator user.
</p>
<br />



































