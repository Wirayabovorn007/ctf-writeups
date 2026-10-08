## Exercise 1
Apply what you learned in this section to grab the banner of the above server and submit it as the answer.


**Solution**

Connect to the host on the specific port using `netcat` or `nc`
```Bash
nc 154.57.164.78 43400
```
You will then see the server's banner:
```Bash
SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0.1
```

## Exercise 2


2.1 Perform an Nmap scan of the target. What does Nmap display as the version of the service running on port 8080?

**Solution**
```Bash
sudo nmap -sV <target>

# Answer:
Apache Tomcat
```

2.2 Perform an Nmap scan of the target and identify the non-default port that the telnet service is running on.

**Solution**
```Bash
sudo nmap -p- --verbose <target>

# --verbose is optional
# Answer:
2323
```

2.3 List the SMB shares available on the target host. Connect to the available share as the bob user. Once connected, access the folder called 'flag' and submit the contents of the flag.txt file.

**Solution**
1. Connect to smbclient username `bob` password `Welcome1`
```Bash
smbclient -U bob \\\\10.129.42.254\\users
```
2. Then try `ls` you will see flag directory
```Bash
smb: \> ls
  .                                   D        0  Fri Feb 26 06:06:52 2021
  ..                                  D        0  Fri Feb 26 03:05:31 2021
  flag                                D        0  Fri Feb 26 06:09:26 2021
  bob                                 D        0  Fri Feb 26 04:42:23 2021

                4062912 blocks of size 1024. 1350356 blocks available
smb: \>
```

3. `cd` to flag directory and use get command to `flag.txt`

```Bash
smb: \> cd flag\
smb: \flag\> ls
  .                                   D        0  Fri Feb 26 06:09:26 2021
  ..                                  D        0  Fri Feb 26 06:06:52 2021
  flag.txt                            N       33  Fri Feb 26 06:09:26 2021

                4062912 blocks of size 1024. 1350352 blocks available
smb: \flag\> get flag.txt
getting file \flag\flag.txt of size 33 as flag.txt (0.0 KiloBytes/sec) (average 0.0 KiloBytes/sec)
```

## Exercise 3

Try running some of the web enumeration techniques you learned in this section on the server above, and use the info you get to get the flag.

**Solution**
1. Search using Gobuster
```Bash
gobuster dir -u <target> -w /usr/share/wordlists/dirb/common.txt
```
2. You will see robot.txt has found, enter the web with path /robots.txt
```Bash
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://154.57.164.72:30809/
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================

[2K/.hta                 (Status: 403) [Size: 281]

[2K/.htaccess            (Status: 403) [Size: 281]

[2K/.htpasswd            (Status: 403) [Size: 281]

[2K/index.php            (Status: 200) [Size: 990]

[2K/robots.txt           (Status: 200) [Size: 45]

[2K/server-status        (Status: 403) [Size: 281]

[2K/wordpress            (Status: 301) [Size: 327] [--> http://154.57.164.72:30809/wordpress/]

===============================================================
Finished
===============================================================

```

3. Check the disallow path you will see the admin page, then try check the HTML source you will get the credential for admin authentication. After that you will get the flag
```html
User-agent: *
Disallow: /admin-login-page.php
```

## Exercise 4

Try to identify the services running on the server above, and then try to search to find public exploits to exploit them. Once you do, try to get the content of the '/flag.txt' file. (note: the web server may take a few seconds to start)





