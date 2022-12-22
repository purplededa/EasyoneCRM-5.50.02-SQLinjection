# EasyoneCRM-5.50.02-SQLinjection
Easyone One is an Italian CRM company with 14 years of experience with a mission: to organize the sales process of companies, in an increasingly complex and competitive market, through the digitization of one of the most important and strategic activities: the relationship with the customer.
Easyone is not a CRM vendor, the company directly produces and develops its own CRM solution for the Italian market.

Easyone developed integration with the most popular management systems on the Italian market: Alyante and Team System Metodo; SageX3, Galileo by San Marco Informatica, Arca by Wolters Kluwer Italia, Business by NTS, MecSal by Passpartout and more.

Easyone has more than 1500 active customers in Italy.


## Description

The vulnerability allows a remote attacker to execute arbitrary SQL queries on a database.

The vulnerability exists due to insufficient sanitization of user-supplied data. A remote non-authenticated attacker can send a specially crafted request to the affected application and execute arbitrary SQL commands within the application database.

Successful exploitation of this vulnerability may allow a remote attacker to read, delete, modify data in the database and gain complete control over the affected application.

## Versions 
Tested Vulnerable version: 5.50.02

Patched version: 5.50.02.03

## Timeline
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
- Vulnerable **text** parameter via GET: domain.com/Services/Misc.asmx/SearchTag?text=SQLI 


# Authors
Luca Bernardi, Davide Bianchin, Fortunato [fox] Lodari @ Deda Cloud Cybersecurity Team
