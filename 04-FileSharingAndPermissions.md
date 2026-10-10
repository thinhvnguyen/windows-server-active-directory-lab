## File Sharing and Permissions

I created shared department folders on the Windows Server and configured access using both share permissions and NTFS permissions. Security groups such as IT-Staff were used to control which users could read or modify each folder. I then tested the permissions from the Windows 11 client to confirm that authorized users could access the share while unauthorized users were denied.
_ _ _ 

I created the folder C:\CompanyShares\IT on the Windows Server to act as a shared department folder. This folder was used to store files that should only be available to members of the IT department. Creating separate department folders is a common way to organize shared company resources.
<img width="956" height="599" alt="createdfolder" src="https://github.com/user-attachments/assets/e55c35b3-3d67-47b1-acc0-ab40ee7014b3" />

_ _ _
I configured the share permissions for the IT folder and assigned access to the IT-Staff security group. Members of this group were allowed to read and modify files in the shared folder. This allowed access to be managed through the group instead of assigning permissions to each user individually.
