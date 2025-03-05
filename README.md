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
<img src="https://github.com/user-attachments/assets/c3bc9da8-a2cd-4549-b457-5c4defa34a46" height="80%" width="80%" </>
</p>
<p>
With the Active Directory services installed, we will promote the server to a domain controller. The system will automatically restart upon installation.
</p>
<br />











































