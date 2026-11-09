# Description
This repository contains a script that uses Nmap to scan for the "Php2Shell" vulnerability. It does not provide a 100% guarantee that the vulnerability exists on the target server; rather, it identifies versions that are potentially susceptible to it.

# How to Work?
It sends an HTTP GET request to the target server and attempts to estimate the server's PHP version by checking the `X-Powered-By` header.

# Evidence

**Test Evidence**:
```
PORT     STATE SERVICE
8080/tcp open  http-proxy
| http-vuln-php2shell:
|   VULNERABLE:
|   Php2Shell CVE 2026 109619/109618 - RCE
|     State: LIKELY VULNERABLE
|     IDs:  1:CVE-2026-109618  CVE:CVE-2026-109619
|     Risk factor: High  CVSSv4: CVSS:4.0/AV:N/AC:H/AT:P/PR:N/UI:N/VC:H/VI:H/VA:H/SC:N/SI:N/SA:N
|       A critical Use-After-Free vulnerability in the PHP engine allows for remote code execution.
|
|     Extra information:
|       PHP Version: 8.5.1 Potentially vulnerable.
|     References:
|       https://www.cve.org/CVERecord?id=CVE-2026-109618
|       https://www.rapid7.com/trust/advisories/php-cve-2026-109618-cve-2026-109619/
|       https://www.cve.org/CVERecord?id=CVE-2026-109619
|       https://ubuntu.com/security/CVE-2026-109618
|       https://nvd.nist.gov/vuln/detail/cve-2026-109618
|       https://ubuntu.com/security/CVE-2026-109619
|       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2026-109619
|_      https://nvd.nist.gov/vuln/detail/CVE-2026-109619
```

# How to İnstall
Below, it is shown how to install it for Termux and Kali Linux:

**Termux**:
```
git clone https://github.com/CyberWarrior10101/Php2Shell-Nmap-Scanning
cd Php2Shell-Nmap-Scanning
mv http-vuln-php2shell.nse /data/data/com.termux/files/usr/share/nmap/scripts
```

**Kali linux**
```
git clone https://github.com/CyberWarrior10101/Php2Shell-Nmap-Scanning
cd Php2Shell-Nmap-Scanning
mv http-vuln-php2shell.nse /usr/share/nmap/scripts
```
