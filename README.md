# module 1-2
## gather Information using Advanced Google Hacking Techniques

intitle:login site:eccouncil.org 
Copy
ceh filetype:pdf 
Copy
intitle:login site:.pk
cache of a site


cache:eccouncil.org
in URL and allinurl
inurl:certification site:eccouncil.org
Other Dorks


intitle:
allintitle:
anchor:
inanchor:
allinanchor:
link:
related:
info:
location:
Sql  injection

* inurl:page.php?id= site:.pk
* cache: This operator allows you to view cached version of the web page. 
* allinurl: This operator restricts results to pages containing all the query terms specified in the URL. 
* inurl: This operator restricts the results to pages containing the word specified in the URL 
* inanchor: This operator restricts results to pages containing the query terms specified in the anchor text on links to the page.
* allinanchor: This operator restricts results to pages containing all query terms specified in the anchor text on links to the page.
* link: This operator searches websites or pages that contain links to the specified website or page. info: This operator finds information for the specified web page. 
* location: This operator finds information for a specific location.
#### Perform Footprinting Through Internet Research Services:
As a professional ethical hacker or pen tester, you should be able to extract a variety of information about your target organization from Internet research services.
# Find the Company’s Domains, Subdomains and Hosts using Netcraft and DNSdumpster:
Domains and sub-domains are part of critical network infrastructure for any organization. A company's top-level domains (TLDs) and subdomains can provide much useful information such as organizational history, services and products, and contact information.

#### Footprinting through DNS Dumpster:
1 Open a new tab in Firefox browser and go to [DNS Dumpster](https://dnsdumpster.com/). Search for certifiedhacker.com in the search box.
2.Further, scroll down to view the domain mapping of the website. Click on Download .xlsx of Hosts button to download the list of hosts.
3.The website displays the GEOIP of Host Locations. Scroll down to view the list of DNS Servers, MX Records, Host Record (A) along with their IP addresses.

## Other tools:
- sublis3ter
- pentest-tools
- FFUF
- Gobuster
- Dirb

##### Emails Using theHarvester
>theHarvester -d microsoft.com -l 200 -b baidu|

## Modeule 3: scanning networks:
In the process of scanning, you attempt to gather information, including the specific IP addresses of the target system that can be accessed over the network (live hosts), open ports, and respective services running on the open ports and vulnerabilities in the live hosts.
Port scanning will help you identify open ports and services running on specific ports, which involves connecting to Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) system ports.
Port scanning is also used to discover the vulnerabilities in the services running on a port. 

###### Network Scanning refers to the set of procedures adopted
network scanning refers to the set of procedures adopted for identifying a network's hosts, ports and services. It's main objectives are as follows
> discover hosts,ip addresses and open ports of all live hosts
> discover OS and system architecture
> discover sevices running on hosts
> discover vulnarabilities on live hosts

Nmap is used to discover hosts and services on a computer network by sending packets and analyzing the responses.
Nmap provides a number of features for probing computer networks, including host discovery and service and operating system detection.
These deature are extensible by scripts that provide mroe advanced service detection, vulnerability detection, and other features.
Nmap can adapt to network conditions including latency and congestion during a scan.


* Port states: there are 6 states:
  1) open: indicates that an application is listening for connections on the             port.
  2) closed: probes were recived but there is no lsitening 
  3) filtered: the probes were not received,state could not be established.
  4) unfiltered: a port is accessible, but NMap is unable to determine whether it is open or closed.
  5) open/filtered: indicates that the port was filtered or open, but Nmap couldn't establish the state.
  6) closed/filter: indicates that Nmap is unable to determine whether a port is closed or filtered

####### Tcp header: 
 * TCP handshake: 
 <img width="1447" height="997" alt="image" src="https://github.com/user-attachments/assets/10aef6e2-1f6c-45a3-afea-1c75f14599fc" /> 
* Connection termination:
  <img width="1355" height="963" alt="image" src="https://github.com/user-attachments/assets/a0b7696a-a023-4af9-9511-0ecce529aca9" />


  ######## Scanning types:
   1) ping scan: is used to scan for the live hosts on the network. command: (nmap -sn 192.168.12.1/24)
  * Tcp connect scan: will scan for TCP ports and ensure for listening port(open) through 3-way handshake connection between the source and destination port. command: (namp -sT a92.000.)
  *  TCP Syn scan: this scan is often referred to as half-open scanning because you don't open a full TCP connecction. You send an SYN packet, as if you are going to open a real connection and then wait for a response. command: (nmap -sS   192....)
  * ACK/SYN indicates the port is listening(open), whilse RST(reset) is indicative of a non-listener. if no response is recerved after several retransmissions, the port is marked as filtered.
  * The port is also marked filtered if an ICMP unreachable error(type 3,0,1,2,3,9,10, or 13) is received.
   <img width="1118" height="273" alt="image" src="https://github.com/user-attachments/assets/83bd9be9-4581-412d-8466-02f0dca86710" />
  2) UDP scan: works by sending a UDp pacet to every targated port. FOR most ports, this packet will be empty(no paylaod), but a few of the more common ports a protocol-specific payload will be sent.
  (nmap -sU 192...)
   <img width="1043" height="541" alt="image" src="https://github.com/user-attachments/assets/d4a210d3-ee0c-4cbe-b04f-ae8c18c0eaaa" />
  3) FIN SCAN : it is one of the port scanning methiods in Nmap, which uses the sheer stupidity of old ans stateless firewalls. When it comes to FIN scan, pur port scanner software sends a packet with a flag in the form of FIN meaning the end of the session to the destination firewall or host. if no response is recieved, it means that the port is open, and if it returns RST//ACK, it means that the server port is closed.
  (nmap -sF 192.2..2..2)

kashan ahmed <sup>'' kashan ahmed ''</sup>
  
   

  

   


  
 
 

 
 





  










