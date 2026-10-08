[![CPTS](https://habrastorage.org/getpro/habr/upload_files/0d6/410/e2e/0d6410e2ee865a5508f713d8383f4e13.PNG)](https://academy.hackthebox.com/path/preview/penetration-tester)

## Using tmux
- open a new window in tmux, we can hit the prefix 'i.e. [CTRL + B]' and then hit C

- We can switch to each window by hitting the prefix and then inputting the window number, like 0 or 1

- We can also split a window vertically into panes by hitting the prefix and then [SHIFT + %]

- We can also split into horizontal panes by hitting the prefix and then [SHIFT + "]

- We can switch between panes by hitting the prefix and then the left or right arrows for horizontal switching or the up or down arrows for vertical switching. 

Online cheatsheet: [Click Here](https://tmuxcheatsheet.com/)

## Web Enumeration

**Ex. Tools**
- Gobuster
- Whatweb: extract the version of web servers, supporting frameworks


**Certificates**
SSL/TLS certificates are another potentially valuable source of information if HTTPS is in use. Viewing the certificate reveals the details, including the email address and company name. These could potentially be used to conduct a phishing attack if this is within the scope of an assessment.


**Robots.txt**
It is common for websites to contain a robots.txt file, whose purpose is to instruct search engine web crawlers such as Googlebot which resources can and cannot be accessed for indexing. The robots.txt file can provide valuable information such as the location of `private files` and `admin pages`.

## Public Exploit

**Finding Public Exploits**
Many tools can help us search for public exploits. A well-known tool for this purpose is searchsploit, which we can use to search for public vulnerabilities exploits for any application. 

Install:
```Bash
sudo apt install exploitdb -y
```
Then, we can use searchsploit to search for a specific application by its name, as follows:
```Bash
searchsploit macos
```

We can also utilize online exploit databases to search for vulnerabilities, like Exploit DB, Rapid7 DB, or Vulnerability Lab.

## Metasploit Primer
The Metasploit Framework (MSF) is an excellent tool for pentesters. It contains many built-in exploits for many public vulnerabilities and provides an easy way to use these exploits against vulnerable targets. MSF has many other features, like:

- Running reconnaissance scripts to enumerate remote hosts and compromised targets

- Verification scripts to test the existence of a vulnerability without actually compromising the target

- Meterpreter, which is a great tool to connect to shells and run commands on the compromised targets

- Many post-exploitation and pivoting tools

To run `Metasploit`, we can use the `msfconsole` command
