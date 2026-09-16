# Machine: Vaccine
Completion date: 09.16.2026

This machine had a simple start. I began by pinging the machine in terminal `ping <IP Address>` to ensure that I was properly connected to the network. The first step after this is to establish which ports are open. `nmap -sC -sV <IP Address>`, which showed me that ports for `HTPP`, `SSH`, and `FTP` were available.

Hack the box gave me a hint here in the phrasing of question 2, asking which username does not require a password for FTP. I began by trying Admin, Anonymous and Root. Anonymous allowed me access without a password, so I connected and looked through files available to me. The only available file was called backup.zip, I got a copy of the file, and it was encrypted with a password.

using Zip2John prepared the file password to be cracked. 
