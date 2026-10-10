## Help Desk Tasks

In this section, I practiced common help desk and Active Directory support tasks that are frequently performed when assisting users. These tasks included resetting passwords, disabling and re-enabling accounts, forcing password changes, and unlocking accounts after repeated failed login attempts. Practicing these scenarios helped me understand how user access issues are diagnosed and resolved in a Windows domain environment.

_ _ _ 
I practiced resetting a user’s password through Active Directory Users and Computers. This is a common help desk task when a user forgets their password, becomes locked out of their account, or needs a temporary password issued by an administrator.
To perform the reset, I located the user account in Active Directory, right-clicked the account, and selected Reset Password. I entered a new password and then tested the updated credentials from the Windows 11 client to make sure the user could successfully sign in with the new password.
<img width="959" height="598" alt="resetpass" src="https://github.com/user-attachments/assets/1c261faf-acda-4e30-8c44-1a159078f339" />

<img width="959" height="599" alt="changepass2" src="https://github.com/user-attachments/assets/30c88563-5ba3-4976-9872-1f0eaf4e7cf9" />


_ _ _
I also practiced disabling a domain user account. Disabling an account prevents the user from signing in while keeping the account, group memberships, and other Active Directory settings intact.
This is useful in situations such as employee offboarding, temporary leave, or when an account needs to be suspended for security reasons. I disabled the account in Active Directory and then attempted to sign in from the Windows 11 client to confirm that authentication was blocked.
After verifying the restriction, I re-enabled the account and confirmed that the user could sign in again. This showed how administrators can temporarily remove access without permanently deleting the user.
<img width="959" height="599" alt="disableacc" src="https://github.com/user-attachments/assets/1acecdba-fd78-4a5e-9ce8-e37f0588fa7b" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/5fe32c19-2689-49fa-9068-6f4abfb10195" />

_ _ _ 
Furthermore, I practiced configuring a user account so that the password had to be changed at the next sign-in. This is commonly used when an administrator resets a password and wants the user to create a private password that only they know.
The setting was configured from the user’s account properties in Active Directory by enabling User must change password at next logon. When the user signed into the Windows 11 client, Windows required them to enter a new password before continuing.

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/4bb7cc3c-7fe8-4606-974c-c640bfc85fc4" /> 

_ _ _
_ _ _

These tasks gave me hands-on experience with common help desk responsibilities, including password resets, account suspension, password-change enforcement, account lockouts, account unlocking, and authentication troubleshooting. I also learned how changes made in Active Directory affect users on a domain-joined Windows client. Together, these tasks helped simulate real support scenarios that are commonly handled in Help Desk and IT Support roles.
