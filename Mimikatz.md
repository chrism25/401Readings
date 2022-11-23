# <p align="center"> Mimikatz

This open source application allows users to view and save authentication credentials like kerberos tickets. Because of this reason and the fact that systems will not detect it, attackers use it to steal credentials and escalate privileges. On the other hand,  pentesters use it to find vulnerabilities so they can be remediated.

### Functionality
* Pass the hash: Users can get access to the system by simply passing the NTLM string hash to the target. For newer windows versions use “pass the ticket”
* Pass the ticket: Attacker passes a kerberos ticket to a computer and logs into the target with that user’s ticket.
* Overpass the hash: In this variation a unique key is acquire from a domain controller and it’s passes to the target computer
* Kerberos golden tickets: Allows actors to get a ticket from the hidden “KRBTGT” account that encrypts all other tickets. This ticket has no expiring domain admin credentials to any computer on the network.
* Kerberos silver tickets: This ticket is obtained from Kerberos ticket granting server(TGS), letting users authenticate to service accounts on the network. 
* Pass the cache: Uses saved and encrypted stored login data on the computer (MAC, UNIX, LINUX). 

### How to use it
* Mimikatz can be obtained from Github and run as an administrator.
* Run the command “version” to make sure you have the correct version and if there are windows settings that could create a conflict.
* Make sure you have the right credentials “mimikatz # privilege::debug”. Begin the logging function “mimikatz # log nameoflog.log” and output all the clear text passwords stores on the computer “mimikatz # sekurlsa::logonpasswords”.

### Defend against it
* Disable password-caching: This way mimikatz won’t find used password on the registry, this can be achieve by going to “Windows Settings>Local Policy>Security Options>Interactive Logon”
* Restrict admin privileges: Admin privileges should only be granted to users who truly need it.
* Turn off debug privileges: This will limit mimikatz ability to use it, since it is available by default for admins.
* Configure additional local security authority protection: Microsoft has additional LSA configuration items that help mitigate the attack surface area. This comes default for Windows 10 and higher.

  
![Screenshot (63)](https://user-images.githubusercontent.com/97658998/203473330-2813acc9-f359-4c17-879e-e0e104df58e2.png)



