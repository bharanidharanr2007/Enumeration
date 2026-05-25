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

## Output:

<img width="1894" height="1025" alt="image" src="https://github.com/user-attachments/assets/f96e83b7-30d1-4849-bac6-83cca892e228" />

### Summary

* Google Dork: site:yahoo.com
The image shows a Google Search results page using the query site:yahoo.com.
This operator restricts results to only pages within the Yahoo domain.
Results include login pages, regional Yahoo sites (France, NZ, Canada), and Yahoo Finance.
Each result is clearly from Yahoo-owned subdomains.
It demonstrates how to explore a website’s indexed content.
Useful for reconnaissance or content discovery.
No external domains appear in results.
Shows structured filtering of search engine results.
Highlights how large sites have multiple localized versions.




filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com

## Output:

<img width="1895" height="1027" alt="image" src="https://github.com/user-attachments/assets/2b174212-cbf9-454f-864f-25ba16932dbc" />


### Summary

* Google Dork: site:yahoo.com filetype:pdf
This screenshot shows search results filtered to PDF files on Yahoo’s domain.
It uses filetype:pdf with site:yahoo.com.
Results include documents like campaign setup guides and technical PDFs.
Displays academic and help-related PDF content.
Demonstrates targeted document discovery via search engines.
Useful for finding reports, manuals, or hidden documents.
Includes a “People also search for” suggestion section.
Shows how structured queries refine results effectively.
Emphasizes document-based reconnaissance.



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

## Output:

<img width="1900" height="1030" alt="image" src="https://github.com/user-attachments/assets/f126a106-f657-41d3-ba1d-4783260615ec" />


### Summary

* Google Dork: site:yahoo.com intext:password
The query searches Yahoo pages containing the word “password.”
Results include help pages about password creation and management.
Examples: password tips, account help, and security guides.
No sensitive data is exposed—only legitimate help content.
Demonstrates keyword-based filtering within a domain.
Useful for identifying security-related pages.
Shows how search engines index textual content.
Often used in security research and OSINT.
Reinforces importance of secure indexing practices.



inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.

## Output:

<img width="1894" height="1028" alt="image" src="https://github.com/user-attachments/assets/bd53a677-2aff-49a6-b71a-dfb5e5be0cc2" />

### Summary

* Google Dork: inurl:admin
This screenshot shows results for pages containing “admin” in the URL.
Results include admin login portals and documentation pages.
Examples: Google Admin, Django admin docs, Atlassian admin.
Demonstrates discovery of administrative interfaces.
Useful in penetration testing and system mapping.
Not all results are sensitive—many are public docs.
Shows how URL-based filtering works.
Highlights potential exposure of admin panels.
Emphasizes need for securing admin endpoints.





intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.

## Output:

<img width="1885" height="1026" alt="image" src="https://github.com/user-attachments/assets/3d5703e7-0237-4bbd-b5f7-3ac6e22923c2" />

### Summary

* Google Dork: inurl:index of
The query searches for directory listing pages.
Results include documentation pages rather than actual open directories.
Commonly used to find exposed file directories.
Shows how search engines index directory titles.
In this case, results are safe and informational.
Demonstrates file indexing concepts.
Useful in vulnerability assessments.
Highlights importance of disabling directory listing.
Shows limitations of search results depending on indexing.




link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

## Output:

<img width="1895" height="1027" alt="image" src="https://github.com/user-attachments/assets/7790de78-5c56-4c39-8dba-6af6859f9f5b" />


### Summary

* Google Dork: link:example.com
This query attempts to find pages linking to example.com.
Results include documentation and references to the domain.
Example.com is a reserved domain for demonstration purposes.
Shows backlink discovery via search engines.
Useful for SEO and link analysis.
Results include forums and informational pages.
Demonstrates how link-based queries work.
Limited accuracy compared to modern SEO tools.
Highlights basic backlink reconnaissance.




cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

## Output:

<img width="1898" height="1027" alt="image" src="https://github.com/user-attachments/assets/68549825-d98a-4891-8300-fa32e072333a" />


### Summary

* Google Dork: webcache:google.com
This screenshot shows search results related to cached pages.
Google Cache stores snapshots of web pages.
Results include tools and guides for viewing cached content.
Mentions that Google discontinued direct cache access in 2024.
Shows alternative tools for accessing cached pages.
Useful for viewing older versions of websites.
Demonstrates search engine caching functionality.
Helps in forensic or historical analysis.
Highlights evolution of search engine features.




 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion


## OUTPUT:

<img width="1283" height="715" alt="image" src="https://github.com/user-attachments/assets/db802cb9-9201-4d90-b01a-4b540baf6325" />


### Summary

* DNSRecon Output (gov.uk)
Terminal output of dnsrecon scanning gov.uk.
Shows DNS enumeration including NS, SOA, and A records.
Multiple IP addresses identified (Fastly CDN ranges).
Lists authoritative name servers (nic.uk servers).
Displays DNSSEC-related records (NSEC3, etc.).
Reveals infrastructure distribution.
Shows bind version responses from servers.
Demonstrates automated DNS reconnaissance.
Useful for mapping domain infrastructure.



##dnsenum
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

## Output:

<img width="844" height="709" alt="image" src="https://github.com/user-attachments/assets/04744f06-081a-437b-a79f-a6981e1224f4" />


### Summary

* DNSenum Output
Output from dnsenum tool scanning gov.uk.
Lists multiple A records (IP addresses).
Displays name servers and their IP mappings.
Attempts zone transfer (AXFR) but fails (REFUSED).
Indicates proper DNS security configuration.
No mail (MX) servers listed in output section.
Shows structured enumeration of DNS data.
Useful for identifying DNS misconfigurations.
Confirms restricted access to zone data.




##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same

## Output:

<img width="716" height="372" alt="image" src="https://github.com/user-attachments/assets/7eeed79f-c0c9-4de5-8c89-38b25beba7c6" />
.
.
.
.

<img width="659" height="355" alt="image" src="https://github.com/user-attachments/assets/33ba6b55-04fa-4f6b-a351-edd136eaf766" />


### Summary

* SMTP User Enumeration
Shows smtp-user-enum tool results.
Attempts to verify users (root, www-data).
Target IP: 151.101.192.144 on port 25.
Scan completes with 0 results.
Indicates no valid usernames found.
Suggests SMTP VRFY is disabled or filtered.
Demonstrates email service enumeration attempt.
Reflects secure mail server configuration.
Shows limited exposure of user data.



#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.

## OUTPUT:

<img width="542" height="177" alt="image" src="https://github.com/user-attachments/assets/66bb473b-2444-476e-bfb0-83e48841bf20" />

### Summary

* Nmap SMTP Scan
Shows nmap scan on port 25 (SMTP).
Target IP: 151.101.192.144.
Port 25 is marked as filtered.
Indicates firewall blocking or no access.
No SMTP service details exposed.
Scan completed quickly (~0.91 seconds).
Confirms restricted mail service access.
Demonstrates network-level filtering.
Aligns with strong security posture.



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

