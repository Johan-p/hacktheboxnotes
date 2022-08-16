# hacktheboxnotes
workflow notes

# nmap

https://github.com/Johan-p/nmap-cheatsheet

`nmap -sC -sV -oA nmap 10.129.147.*`

# websites

## Hostname

`echo "10.129.129.* websitename.htb" | sudo tee -a /etc/hosts`

## enumeration

### Subdomains

If you don't have Seclist

`git clone https://github.com/danielmiessler/SecLists.git`

On pwnbox its found on the desktop

`gobuster vhost -w ~/Desktop/Useful\ Repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -u http://website.htb`

