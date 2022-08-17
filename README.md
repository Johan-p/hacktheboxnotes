# Network Service Discovery: [T1046](https://attack.mitre.org/techniques/T1046/)


[nmap](https://github.com/Johan-p/nmap-cheatsheet)

`nmap -sC -sV -oA nmap 10.129.147.*`



# Websites

## Active Scanning: Wordlist Scanning: [T1595.003](https://attack.mitre.org/techniques/T1595/003/) 

### Add website to hosts file

`echo "10.129.129.* websitename.htb" | sudo tee -a /etc/hosts`

### Discover Subdomains

`gobuster vhost -w ~/Desktop/Useful\ Repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -u http://website.htb`

If you don't have [SecList](https://www.kali.org/tools/seclists/) installed

`git clone https://github.com/danielmiessler/SecLists.git`
 
 *note that with pwnbox its found on the desktop*




