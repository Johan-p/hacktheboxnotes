# Tool list
1. [nmap](https://www.kali.org/tools/nmap/)
2. [SecList](https://www.kali.org/tools/seclists/)
3. [gobuster](https://www.kali.org/tools/gobuster/)
4. [burpsuit](https://www.kali.org/tools/burpsuite/)
5. [droopescan]()
6. 


# Discovery
## Network Service Discovery: [T1046](https://attack.mitre.org/techniques/T1046/)


### [nmap](https://github.com/Johan-p/nmap-cheatsheet)

`echo targetip > target.txt`

`nmap -sC -sV -oA nmap -iL target.txt`

# Websites
## Reconnaissance
### Active Scanning: Wordlist Scanning: [T1595.003](https://attack.mitre.org/techniques/T1595/003/) 

**Add website to hosts file**

`echo "10.129.129.* websitename.htb" | sudo tee -a /etc/hosts`

**Discover Subdomains**

`gobuster vhost -w ~/Desktop/Useful\ Repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -u http://website.htb`

If you don't have [SecList](https://www.kali.org/tools/seclists/) installed

`git clone https://github.com/danielmiessler/SecLists.git`
 
 *note that with pwnbox its found on the desktop*

**Directories**

`gobuster -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt dir --url http://website.htb -t 20`

**Drupal sites**
 
`cd opt/droopescan`

`./droopescan scan drupal -u 10.129.147.*`

`http://10.129.147.*/CHANGELOG.txt`

## Initial Access
###  Drive-by Compromise: [T1189](https://attack.mitre.org/techniques/T1189/) 

**Burpsuite**



