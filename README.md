# Tool list
1. [nmap](https://www.kali.org/tools/nmap/)
2. [SecList](https://www.kali.org/tools/seclists/)
3. [gobuster](https://www.kali.org/tools/gobuster/)
4. [feroxbuster](https://github.com/epi052/feroxbuster)
5. [git-dumper](https://github.com/arthaud/git-dumper)
6. [burpsuit](https://www.kali.org/tools/burpsuite/)
7. [droopescan]()
8. 



# Discovery
## Network Service Discovery: [T1046](https://attack.mitre.org/techniques/T1046/)
### [nmap](https://github.com/Johan-p/nmap-cheatsheet)

`echo "targetip" > target.txt`

`nmap -sC -sV -Pn -oA nmap -iL target.txt`


# Websites
# Reconnaissance
## Active Scanning: Wordlist Scanning: [T1595.003](https://attack.mitre.org/techniques/T1595/003/) 

### Add website to hosts file

`echo "10.129.129.* websitename.htb" | sudo tee -a /etc/hosts`

### Discover Subdomains

`gobuster vhost -w ~/Desktop/Useful\ Repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -u http://website.htb`

If you don't have [SecList](https://www.kali.org/tools/seclists/) installed

`git clone https://github.com/danielmiessler/SecLists.git`
 
 *note that with pwnbox its found on the desktop*

### Directories

`gobuster -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt dir --url http://website.htb -t 20`

`feroxbuster -u http://website.htb -n -w /usr/share/wordlist/dirb/common.txt --no-state -C 400`

### Git repitory

`pipx install git-dumper`

dumping the repo
`git-dumper http://website.htb repo`

you can now explore the repo inside the repo folder

show the log
`git log`

explore a spesific commit
`git show commithash`



### Drupal sites
 
`cd opt/droopescan`

`./droopescan scan drupal -u 10.129.147.*`

`http://10.129.147.*/CHANGELOG.txt`


## Privilege escalation

Linux privilege escalation

See [GTFOBins](https://gtfobins.github.io/) 


## Resource Development
### Develop Capabilities: Malware: [T1587.001](https://attack.mitre.org/techniques/T1587/001/)

[See Reverse Shell Cheat Sheet](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md#groovy)

**simple shell code script**

`ip addr`

change the ip to the ipadress of your machine

`vim shell.sh`


**Netcat listener**

Open another terminal and run a Netcat listener

`nc -nvlp 1337`

### Stage Capabilities: Upload Malware: [T1608.001](https://attack.mitre.org/techniques/T1608/001/)
**Simple python webserver**

In order to deliver our shell script use a simple http server

`python3 -m http.server 8000`


## Initial Access
###  Drive-by Compromise: [T1189](https://attack.mitre.org/techniques/T1189/) 

**Burpsuite**




