# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

<img width="1902" height="920" alt="Screenshot 2026-10-31 081717" src="https://github.com/user-attachments/assets/a0a82be1-495d-4cc2-a5a0-451d9c61447e" />


filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
<img width="1897" height="927" alt="Screenshot 2026-10-31 084457" src="https://github.com/user-attachments/assets/121c8b66-e161-4a2c-95c7-bda003e5521c" />


intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

<img width="1913" height="928" alt="Screenshot 2026-10-31 081917" src="https://github.com/user-attachments/assets/ff23fb20-940a-424b-b7c3-ca690ecb36a3" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
<img width="1917" height="871" alt="Screenshot 2026-10-31 081956" src="https://github.com/user-attachments/assets/dc670876-a90e-4e17-97db-bc4d05e42b08" />


intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
<img width="1902" height="935" alt="Screenshot 2026-10-31 082039" src="https://github.com/user-attachments/assets/3a35ac8f-3963-4b72-ab48-36abd7456629" />


link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
<img width="1902" height="922" alt="Screenshot 2026-10-31 082149" src="https://github.com/user-attachments/assets/c0841a3f-892b-400e-a097-b7a4d25370d5" />


cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.
<img width="1685" height="982" alt="Screenshot 2026-10-31 082249" src="https://github.com/user-attachments/assets/7007f5db-cdbc-4a10-88a8-3431ed5c9e9e" />

 
## DNS Enumeration


## DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:
<img width="1672" height="863" alt="Screenshot 2026-10-31 083549" src="https://github.com/user-attachments/assets/d9291366-86ad-46b7-9ab5-48b4dc10e718" />


## dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
```
dig yahoo.com A
```
<img width="1065" height="648" alt="Screenshot 2026-10-31 083820" src="https://github.com/user-attachments/assets/e601ff7d-96f1-4dfd-b5f9-c4532837bfc2" />

Get the namservers (threaded).
```
dig yahoo.com NS
```
<img width="1670" height="863" alt="Screenshot 2026-10-31 083944" src="https://github.com/user-attachments/assets/c1d00478-0f24-4312-810b-0af41680ac0e" />

Get the MX record (threaded).
```
dig yahoo.com MX
```
<img width="1296" height="578" alt="Screenshot 2026-10-31 084136" src="https://github.com/user-attachments/assets/3fc171ef-cbc5-4ed0-b0b8-93344192e273" />

Perform axfr queries on nameservers and get BIND versions(threaded).
```
dig @ns1.yahoo.com yahoo.com axfr
```
<img width="998" height="261" alt="Screenshot 2026-11-03 084241" src="https://github.com/user-attachments/assets/783ff1c2-07cd-4dfc-a6c5-5eab90dad2c9" />

##DNS Enumeration using dnsenum:
```
dnsenum yahoo.com
```
<img width="1657" height="740" alt="Screenshot 2026-11-03 085013" src="https://github.com/user-attachments/assets/7b36535a-4efe-4ab0-be54-30f595e1c94b" />



## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same
## output

<img width="841" height="492" alt="Screenshot 2026-11-03 090535" src="https://github.com/user-attachments/assets/aad0393a-5d15-4ab3-bcb9-a9bbe0ee96cb" />

<img width="936" height="782" alt="Screenshot 2026-11-03 123506" src="https://github.com/user-attachments/assets/0505ffe7-e692-426b-b998-85f23628d1b2" />


## Telnet for smtp enumeration

Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ## Output
 
<img width="932" height="477" alt="Screenshot 2026-11-03 125656" src="https://github.com/user-attachments/assets/2796c629-6859-4b55-b280-04885fca9ea8" />

  
  
## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
<img width="908" height="326" alt="Screenshot 2026-11-03 125928" src="https://github.com/user-attachments/assets/0f5a9fb1-6c12-4cf4-837e-8ab6026b5441" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully


