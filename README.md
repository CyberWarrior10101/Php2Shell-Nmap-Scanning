# Description
This repository contains a script that uses Nmap to scan for the "Php2Shell" vulnerability. It does not provide a 100% guarantee that the vulnerability exists on the target server; rather, it identifies versions that are potentially susceptible to it.

# How to Work?
It sends an HTTP GET request to the target server and attempts to estimate the server's PHP version by checking the `X-Powered-By` header.

# How to İnstall
Below, it is shown how to install it for Termux and Kali Linux:

**Termux**:
’’’
git clone https://github.com/CyberWarrior10101/Php2Shell-Nmap-Scanning
cd Php2Shell-Nmap-Scanning
mv http-vuln-php2shell.nse /data/data/com.termux/files/usr/share/nmap/scripts
’’’

**Kali linux**
’’’
git clone https://github.com/CyberWarrior10101/Php2Shell-Nmap-Scanning
cd Php2Shell-Nmap-Scanning
mv http-vuln-php2shell.nse /usr/share/nmap/scripts
’’’
