## Skill Assessment 

Use the Security Onion to analyse the provided evidence files and identify the type of attack and its cause.
We’ve been provided with two evidences zip files

1. By Extracting File of Evidence 1

![image](https://github.com/user-attachments/assets/1aada2bc-dcea-4574-bad3-159391a53c22)

From Wireshark we can analyse that all pdfs have same link to download which seems to be some doubtfull

![image](https://github.com/user-attachments/assets/12bd1680-9487-49dd-939e-32e3be7138ec)

- > We got the copy of email in .eml format so we can decode it to analyse and we get that files are having pdf as attachment.

  ![image](https://github.com/user-attachments/assets/7a92c376-6b3c-402c-8963-8e552fcf3087)

-> Traffic for an Inspection we got as in wireshark. Many dll files are beimg downloaded

![image](https://github.com/user-attachments/assets/4954411d-93aa-404c-ad10-6b873c7211f8)


-> Extracted js file from that zip 

![image](https://github.com/user-attachments/assets/3ab4d547-8cfb-4f74-b6ab-ebc7aa924c03)

![image](https://github.com/user-attachments/assets/d3eeea4b-7a19-4186-b102-ffdc7d4a8d0c)

-> By comparing the image size 

![image](https://github.com/user-attachments/assets/8180ad7f-e96c-4efb-8a28-4f1119b1f3bf)

![image](https://github.com/user-attachments/assets/5e724472-1c0d-4bbf-8be8-088537e46ece)


Flow of an Attack: 

  email --> PDF --> link from PDF --> downloaded zip --> extracted JS --> run JS --> HTTPS traffic for script --> HTTPS traffic for zip --> extracted StealC EXE --> StealC data exfiltration over HTTP

Proof of this attack:

![image](https://github.com/user-attachments/assets/e8c78222-be73-4945-b2fb-d27a789b3a86)

Summary of initial examination of evidence 1 folder:

PDF Phishing: Several PDF files are flagged with high detection rates, suggesting they are used in phishing attacks.
Spyware and Trojans: ZIP files and JavaScript files with high detection rates indicate they may contain spyware or trojans, which are typically used to steal information or gain unauthorized access to systems.
Malspam (Malicious Spam): The presence of an email file related to malspam pushing the Stealc malware points towards an ongoing campaign using malicious emails to distribute malware.


2. By Extracting File of Evidence 2

![image](https://github.com/user-attachments/assets/4d871b48-30a8-4779-8c1d-7f20bc2ecef7)

On analysing the pcap file with dns filter

![image](https://github.com/user-attachments/assets/f0d790ba-680e-4f12-adc6-36d9e0a96ae7)

![image](https://github.com/user-attachments/assets/b4bc27b6-ef1c-46bd-a10d-861ab9f70477)

The DNS queries are from a client machine (IP: 10.1.30.101) querying for domains associated with the infection.
This text file lists URLs and domains that were abused for malicious purposes, including:
- hxxps://adclick.g.doubleclick.net/pcs/click?f957443683554531pn9713-24-QfP574vIONEZlkd&&adurl=//projetodegente.com/

- hxxps://monitor.clickcease.com/tracker/tracker?id=vvabeFIqY827477154919rN15733877717t94&adpos=&nw=a&url=//projetodegente.com/

- Note: doubleclick.net and clickcease.com are legitimate, but they were abused in URLs that led to projetodegent.com. 
  The domain projetodegente.com is also a legitimate website, but it was redirecting traffic for this campaign.


This `hxxps://www.verxy.me/wp-content/uploads/2023/12/s/s/letter-F54876-2024.cab` url gives a download option and cab file gets downloaded.  In addition to the .url file, this cab contains a zero byte decoy file named Cloud-Extract to Documents.txt

Extracted .url files and .msi installer

- 5.252.178.193 port 80 - 5.252.178.193 - OPTIONS / HTTP/1.1 
- 5.252.178.193 port 80 - 5.252.178.193 - OPTIONS /Downloads HTTP/1.1 
- 5.252.178.193 port 80 - 5.252.178.193 - PROPFIND /Downloads/independert.zip/independert.msi HTTP/1.1 
- 5.252.178.193 port 80 - 5.252.178.193 - PROPFIND /Downloads/independert.zip HTTP/1.1 
- 5.252.178.193 port 80 - 5.252.178.193 - GET /Downloads/independert.zip HTTP/1.1 

•	The correlation between the screenshots shows that the DNS queries in the .pcap file are related to the infection activity outlined in the text file.

•	The system made DNS requests to domains that are known to be associated with the distribution and execution of DarkGate malware, confirming that the traffic captured is indeed indicative of malicious activity.

![image](https://github.com/user-attachments/assets/036586f4-29a0-46dd-9c47-4891c18e1bd8)

Here we can see they are directly targeting to update Windows Registry Value.

•	The DNS queries captured in the .pcap file likely occurred during or after these downloads, as the malware attempts to reach out to C2 servers or download additional payloads.

•	The text file mentions the download and execution of malicious files, such as a .cab file from projetodgente.com, which, when extracted, led to further malware execution (MSI installer leading to .au3 and .exe files).

Copy of Autoit3.exe, version 3.3.14.5, not malicious but used to run malicious .au3 file

