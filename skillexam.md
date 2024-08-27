## Skill Assessment 

Use the Security Onion to analyse the provided evidence files and identify the type of attack and its cause.
We’ve been provided with two evidences zip files

1. By Extracting File of Evidence 1

![image](https://github.com/user-attachments/assets/1aada2bc-dcea-4574-bad3-159391a53c22)

From Wireshark we can analyse that all pdfs have same link to download which seems to be some doubtfull

![image](https://github.com/user-attachments/assets/12bd1680-9487-49dd-939e-32e3be7138ec)

- > We got the copy of email in .eml format so we can decode it to analyse and we get that files are having pdf as attachment

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

3.
