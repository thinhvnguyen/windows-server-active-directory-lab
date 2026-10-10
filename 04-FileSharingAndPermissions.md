## File Sharing and Permissions

I created shared department folders on the Windows Server and configured access using both share permissions and NTFS permissions. Security groups such as IT-Staff were used to control which users could read or modify each folder. I then tested the permissions from the Windows 11 client to confirm that authorized users could access the share while unauthorized users were denied.
_ _ _ 

I created the folder C:\CompanyShares\IT on the Windows Server to act as a shared department folder. This folder was used to store files that should only be available to members of the IT department. Creating separate department folders is a common way to organize shared company resources.
<img width="956" height="599" alt="createdfolder" src="https://github.com/user-attachments/assets/e55c35b3-3d67-47b1-acc0-ab40ee7014b3" />

_ _ _
I configured the share permissions for the IT folder and assigned access to the IT-Staff security group. Members of this group were allowed to read and modify files in the shared folder. This allowed access to be managed through the group instead of assigning permissions to each user individually.
<img width="512" height="388" alt="sharedfolderperm" src="https://github.com/user-attachments/assets/cef260ca-6857-4d50-9fc3-d358a2b16e7c" />
_ _ _
Then, configured the NTFS permissions on the IT folder. The IT-Staff group was given Modify access, which allowed members to create, edit, and delete files. Using both share permissions and NTFS permissions provides two layers of access control.
<img width="512" height="385" alt="2layerperm" src="https://github.com/user-attachments/assets/293e29eb-fee0-43a5-b6e0-8ea52dd1b8fc" />

I also adjusted inherited permissions so that access to the IT folder could be restricted more precisely. This removed unnecessary permissions and ensured that only the required users and groups had access. It demonstrated how NTFS inheritance can affect folder security. This is also a way I played around with permissions, removing and adding them constantly.
<img width="512" height="388" alt="removingperm" src="https://github.com/user-attachments/assets/02742b17-58ed-4a9b-9098-611f5fad7bf2" />
<img width="512" height="383" alt="removed" src="https://github.com/user-attachments/assets/04938f9b-4d9b-4d70-ab08-f76dfc5a5895" />
_ _ _

With removing and adding, I also tested sharing the different files on different computers available. I tested the shared folder by connecting to it from the Windows 11 client and creating a test file. The file appeared on the Windows Server, confirming that file sharing and write permissions were working correctly. This verified that an authorized domain user could access and modify the shared resource.
<img width="1280" height="720" alt="createfolderandfileinclient" src="https://github.com/user-attachments/assets/ed1e6e5e-3c3e-456b-8de3-fd5eb0186621" />
_ _ _
<img width="959" height="599" alt="received on the other end" src="https://github.com/user-attachments/assets/2653176d-67a7-4e06-94f5-38769bea2d28" />

And here, we can see that the file was successfully received on the other end, confirming that the shared folder and permissions were working correctly.
