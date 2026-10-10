## Group Policy Management (GPO)

In this section, I used Group Policy Management to centrally control settings for users and computers in the mylab.local domain. Group Policy allows administrators to configure rules once on the server and apply them automatically to selected computers or users. I used this to configure both an account lockout policy and an IT workstation policy.
Group Policy Management


I opened Group Policy Management from Server Manager to view and manage the policies in the domain. From here, I could see the mylab.local domain, the Default Domain Policy, and the Organizational Units I created earlier. This console is used to create, edit, and link Group Policy Objects to specific parts of Active Directory.
I edited the domain policy to configure an Account Lockout Policy. This policy determines how many incorrect password attempts are allowed before a user account is temporarily locked. The purpose of this setting is to reduce the risk of repeated password-guessing attempts against domain accounts.
In my lab, I configured values such as:


Account lockout threshold: 5 attempts


Account lockout duration: 10 minutes


Reset account lockout counter after: 10 minutes

<img width="959" height="599" alt="group management policy" src="https://github.com/user-attachments/assets/566ce45a-8d5f-4ff4-af8b-1cb6459edafa" />

I later tested the policy by entering an incorrect password multiple times on a domain user account and then unlocking the account through Active Directory.

_ _ _

With this lab, I also messed around with IT Workstation Policy. Instead of applying this policy to the entire domain, I linked it specifically to the IT-Computers Organizational Unit. This allowed me to target the Windows 11 workstation ITPC1 without affecting every computer in the domain.
<img width="959" height="599" alt="it workstation policy" src="https://github.com/user-attachments/assets/ce239fdc-a88a-4d7c-8fdc-3dbcd1c6d898" />


The IT Workstation Policy was linked to the IT-Computers OU, where the ITPC1 computer account was located. Linking the policy to this OU means that computers placed inside it can receive the settings defined in that GPO. This demonstrates how Organizational Units and Group Policy work together to provide centralized and targeted computer management.

<img width="959" height="599" alt="enforcinggpo" src="https://github.com/user-attachments/assets/0ce769a1-725d-4b38-b4da-3f6238384cf7" />

After creating and linking the GPO, I updated the Windows 11 client so it would immediately retrieve the new policy from the domain controller.This forces Windows to refresh both computer and user Group Policy settings instead of waiting for the normal background refresh interval.
_ _ _ 
Group Policy allows administrators to manage many domain computers from one central location instead of configuring every workstation individually. For example, an administrator can use GPOs to control security settings, password policies, desktop restrictions, software configuration, and other Windows settings. In this lab, using the IT-Computers OU allowed me to apply policies specifically to IT workstations while leaving other departments unaffected.
