## Domain Join and Computer Management

After installing the Windows 11 client, I connected it to the same network as the Windows Server and joined it to the `mylab.local` domain. This allowed the client computer to use Active Directory for authentication and centralized management.
Once the Windows 11 machine joined the domain, a computer account named `ITPC1` appeared in Active Directory. I then moved `ITPC1` from the default **Computers** container into the `IT-Computers` Organizational Unit.
Moving the computer into the `IT-Computers` OU made the Active Directory structure more organized and allowed me to apply computer-specific Group Policies to the workstation later in the lab.
_ _ _

I configured the Windows Server VM to use a Bridged Adapter in VirtualBox. This allowed the virtual machine to communicate with other devices on the same local network. Using bridged networking helped the Windows 11 client reach the domain controller directly.
<img width="959" height="599" alt="bridge_adapter" src="https://github.com/user-attachments/assets/a844daee-cc1b-4f45-834c-a33bc1f3dd5b" />
With bridge adapter, it allowed the Windows 11 client and Windows Server to reach each other.
_ _ _ 
ipconfig displays the network settings of the computer, including the IP address, subnet mask, and default gateway. In your lab, it showed the Windows Server using the IPv4 address 10.0.0.79. This was important because the Windows 11 client needed that server address for communication and DNS.
<img width="509" height="386" alt="ipconfig" src="https://github.com/user-attachments/assets/57db752f-5765-4894-86d9-924c78a38e57" />

Then, I used ping from the Windows 11 client to test connectivity to the server at 10.0.0.79. The test returned four successful replies with no packet loss. This confirmed that the client and server could communicate over the network.
<img width="1024" height="766" alt="window11_ping" src="https://github.com/user-attachments/assets/7a18141c-a528-49c9-bf30-f7cb4ef1cae2" />

_ _ _
With ping confirming their connectivity, I configured the Windows 11 client to obtain its IP address automatically while manually setting the DNS server to 10.0.0.79. This directed the client’s DNS requests to the Windows Server domain controller. Correct DNS configuration was necessary for the client to locate the mylab.local domain.
<img width="1024" height="772" alt="obtainipaddress" src="https://github.com/user-attachments/assets/df58ea3a-0a8f-447f-a1b1-de157f9f3fc9" />
_ _ _
I opened the computer name and domain settings on the Windows 11 client. I entered mylab.local as the domain the computer should join. This began the process of adding the client to the Active Directory environment.
<img width="1024" height="763" alt="domainset" src="https://github.com/user-attachments/assets/6bbe4147-9b13-417f-ad3a-4c97f119c5d4" />

<img width="1024" height="766" alt="domain_change" src="https://github.com/user-attachments/assets/9908c627-d0f2-4fbf-8a6a-601451250165" />
_ _ _
After joining the domain, the Windows 11 login screen showed that the system was signing in to MYLAB. I used the Active Directory account yuki.tanaka to log in. This confirmed that domain authentication was available on the client. I ran the whoami command after signing in with the domain account. The output returned mylab\yuki.tanaka. This verified that the Windows 11 client was successfully authenticated through Active Directory.
<img width="1024" height="769" alt="domainauthentication" src="https://github.com/user-attachments/assets/86154812-31a0-4d3e-aa63-330a703850ef" />
<img width="1024" height="763" alt="success" src="https://github.com/user-attachments/assets/2153dbc7-bc41-4791-8e89-302404d6092d" />
_ _ _


