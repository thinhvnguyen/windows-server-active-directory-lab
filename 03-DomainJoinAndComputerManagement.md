## Domain Join and Computer Management

After installing the Windows 11 client, I connected it to the same network as the Windows Server and joined it to the `mylab.local` domain. This allowed the client computer to use Active Directory for authentication and centralized management.
Once the Windows 11 machine joined the domain, a computer account named `ITPC1` appeared in Active Directory. I then moved `ITPC1` from the default **Computers** container into the `IT-Computers` Organizational Unit.
Moving the computer into the `IT-Computers` OU made the Active Directory structure more organized and allowed me to apply computer-specific Group Policies to the workstation later in the lab.
_ _ _

I configured the Windows Server VM to use a Bridged Adapter in VirtualBox. This allowed the virtual machine to communicate with other devices on the same local network. Using bridged networking helped the Windows 11 client reach the domain controller directly.
<img width="959" height="599" alt="bridge_adapter" src="https://github.com/user-attachments/assets/a844daee-cc1b-4f45-834c-a33bc1f3dd5b" />
With bridge adapter, it allowed the Windows 11 client and Windows Server to reach each other.
_ _ _ 
Then, I used ping from the Windows 11 client to test connectivity to the server at 10.0.0.79. The test returned four successful replies with no packet loss. This confirmed that the client and server could communicate over the network.
