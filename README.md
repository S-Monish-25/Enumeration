# Ex 3 - Enumeration

Enumeration Techniques used in Ethical Hacking. Explore Google Hacking and Enumeration .

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

## site: 
This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

<img width="788" height="479" alt="image" src="https://github.com/user-attachments/assets/b1a828b7-9fc6-4ba9-8c6c-9b5bc819de5a" />

<img width="858" height="462" alt="image" src="https://github.com/user-attachments/assets/326bdbb5-4167-4048-93b9-e28ace61a83c" />


## filetype: 
This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com
<img width="848" height="453" alt="image" src="https://github.com/user-attachments/assets/a6a4ee3a-db91-4632-8ca7-e6c91c5e54fe" />


## intext: 
This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

<img width="822" height="449" alt="image" src="https://github.com/user-attachments/assets/8c755b98-1aa9-4fcb-9f5c-04e7e5056133" />


## inurl: 
This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.

<img width="858" height="458" alt="image" src="https://github.com/user-attachments/assets/2b3eb50f-da19-4b41-b632-5433cc52f6f4" />


## intitle: 
This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.

<img width="875" height="472" alt="image" src="https://github.com/user-attachments/assets/3b79390b-fc09-4629-97d1-a0b06ae50d8f" />


## link: 
This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

<img width="839" height="466" alt="image" src="https://github.com/user-attachments/assets/1317c084-9eef-4ebb-a19a-422f6626e0c7" />


## cache: 
This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

<img width="893" height="474" alt="image" src="https://github.com/user-attachments/assets/418dd8d2-8302-4719-9704-fc81aeb65634" />

 
## DNS Enumeration


## DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion

## OUTPUT:

<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/1aede5a3-3daf-4e93-acca-76ff0b3904f4" />

<img width="884" height="610" alt="image" src="https://github.com/user-attachments/assets/40a4fac1-ffeb-4b7f-b7d7-2ecb77e93911" />


## dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.


## OUTPUT:

<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/c07accc7-769f-4a90-846c-41f77ca61c02" />

<img width="1005" height="612" alt="image" src="https://github.com/user-attachments/assets/8cf5abb8-7fea-4ea0-818b-32008e062135" />


## smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same

## Output

<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/41a64540-f7bf-4617-bfa9-1990ec31c639" />

<img width="774" height="625" alt="image" src="https://github.com/user-attachments/assets/5b6fefe3-6969-4c27-a016-28f9611b44c5" />


## Telnet for smtp enumeration

Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
## Output
  
<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/58401882-5301-466c-bbf8-bee5ef53a1b1" />

<img width="1068" height="818" alt="image" src="https://github.com/user-attachments/assets/3f88b84a-1fca-4d4c-b578-7a3509f69ca7" />


## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.

## OUTPUT:

<img width="1920" height="945" alt="image" src="https://github.com/user-attachments/assets/34053927-a35a-4212-8545-7a6800a69c3b" />

<img width="838" height="726" alt="image" src="https://github.com/user-attachments/assets/fce505a2-9dd7-4b17-967e-24670acbad54" />


## RESULT:

The Google hacking keywords and enumeration tools were identified and executed successfully.
