# Machine: Vaccine
Completion date: 09.16.2026

This machine had a simple start. I began by pinging the machine in terminal `ping <IP Address>` to ensure that I was properly connected to the network. The first step after this is to establish which ports are open. `nmap -sC -sV <IP Address>`, which showed me that ports for `HTPP`, `SSH`, and `FTP` were available.

Hack the box gave me a hint here in the phrasing of question 2, asking which username does not require a password for FTP. I began by trying Admin, Anonymous and Root. Anonymous allowed me access without a password, so I connected and looked through files available to me. The only available file was called backup.zip, I got a copy of the file, it was encrypted with a password.

First I tried some common passwords like `password, Password, Password123, etc` with no luck. So I used Zip2John to prepare the file password to be cracked. `zip2john backup.zip > hashes`. This put the hash for the password on backup.zip into a file called hashes, allowint it to be used with JohnTheRipper. `John ~/path/to/wordlist.txt hashes`. After 
