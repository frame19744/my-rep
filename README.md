# ДЗ по уроку №2


---
1.	*Создать новую виртуальную машину с собственным именем пользователя.*

**ВЫПОЛНЕНО**

2.	*Удалить git, и установить его снова в виртуальной машине.*

```bash
┌──(kali㉿kali)-[~]
└─$ sudo git
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]
```
---
```bash
──(kali㉿kali)-[~]
└─$ sudo apt remove git  
The following packages were automatically installed and are no longer required:
  aspnetcore-runtime-6.0              libportmidi2                    python3-ply
  aspnetcore-targeting-pack-6.0       libsdl2-2.0-0                   python3-pydantic-settings
  binutils-mingw-w64-base             libsdl2-image-2.0-0             python3-pydispatch
  binutils-mingw-w64-i686             libsdl2-mixer-2.0-0             python3-pydyf
  binutils-mingw-w64-x86-64           libsdl2-ttf-2.0-0               python3-pyfiglet
  dnsmap                              libsmb2-6                       python3-pygame
  dotnet-apphost-pack-6.0             libxar1                         python3-pyinstaller
  dotnet-host                         libxmp4                         python3-pymysql
  dotnet-hostfxr-6.0                  medusa                          python3-pyphen
  dotnet-runtime-6.0                  mingw-w64-common                python3-pyshodan
  dotnet-runtime-deps-6.0             mingw-w64-i686-dev              python3-pyvirtualdisplay
  dotnet-sdk-6.0                      mingw-w64-x86-64-dev            python3-pyvnc
  dotnet-targeting-pack-6.0           netstandard-targeting-pack-2.1  python3-qasync
  dsniff                              nuclei                          python3-qrcode
  ettercap-common                     oracle-instantclient-basic      python3-rapidfuzz
  ettercap-graphical                  pcre2-utils                     python3-secretsocks
  eyewitness                          pyinstaller                     python3-serial-asyncio
  feroxbuster                         pyinstaller-hooks-contrib       python3-smmap
  figlet                              python3-altgraph                python3-sqlalchemy-utc
  finger                              python3-antlr4                  python3-stix2
  gcc-mingw-w64-base                  python3-browser-cookie3         python3-stix2-patterns
  gcc-mingw-w64-i686-win32            python3-cssselect2              python3-stone
  gcc-mingw-w64-i686-win32-runtime    python3-docopt                  python3-tinyhtml5
  gcc-mingw-w64-x86-64-win32          python3-donut                   python3-tld
  gcc-mingw-w64-x86-64-win32-runtime  python3-dropbox                 python3-wapiti-swagger
  git-man                             python3-fuzzywuzzy              python3-websockify
  httpx-toolkit                       python3-gitdb                   python3-zlib-wrapper
  hyphen-en-us                        python3-httpx-ntlm              rsh-redone-client
  libapache2-mod-php                  python3-humanize                smtp-user-enum
  liberror-perl                       python3-jeepney                 sparta-scripts
  libjq1                              python3-jq                      toilet-fonts
  libluajit-5.1-2                     python3-jwcrypto                unicornscan
  libluajit-5.1-common                python3-levenshtein             urlscan
  libnids1.21t64                      python3-macholib                wapiti
  libonig5                            python3-markdown2               weasyprint
  libopusfile0                        python3-md2pdf                  xar
  libpcre2-32-0                       python3-obfuscator
Use 'sudo apt autoremove' to remove them.

REMOVING:
  commix               kali-tools-top10      msfpc                set
  git                  legion                powershell-empire    unicorn-magic                     
  kali-linux-default   manpages-utils        python3-git                                            
  kali-linux-headless  metasploit-framework  python3-pyexploitdb                                    
                                                                                                    
Summary:
  Upgrading: 0, Installing: 0, Removing: 14, Not Upgrading: 2
  Freed space: 777 MB

Continue? [Y/n] y
(Reading database… 456386 files and directories currently installed.)
Removing kali-linux-default (2026.3.9)…
Removing kali-linux-headless (2026.3.9)…
Removing commix (4.1-0kali1)…
Removing legion (0.7.0-0kali2)…
Removing python3-pyexploitdb (0.3.45-0kali2)…
Removing python3-git (3.1.61-1)…
Removing powershell-empire (6.6.0-0kali1)…
Removing kali-tools-top10 (2026.3.9)…
Removing manpages-utils (6.19-3)…
Removing unicorn-magic (3.12-0kali3)…
Removing set (8.1.3+git20260604-0kali1)…
Removing msfpc (1.4.5-0kali3)…
Removing metasploit-framework (6.5.3-0kali1)…
Removing git (1:2.53.0-1)…
Processing triggers for libc-bin (2.43-6)…
Processing triggers for man-db (2.13.1-1)…
Processing triggers for wordlists (2026.2.0)…
Processing triggers for kali-menu (2026.3.4)…
```
---
```bash
┌──(kali㉿kali)-[~]
└─$ sudo git             
[sudo] password for kali: 
sudo: git: command not found
```
---
```bash
┌──(kali㉿kali)-[~]
└─$ sudo apt install git 
The following packages were automatically installed and are no longer required:
  aspnetcore-runtime-6.0              python3-antlr4
  aspnetcore-targeting-pack-6.0       python3-browser-cookie3
  binutils-mingw-w64-base             python3-cssselect2
  binutils-mingw-w64-i686             python3-docopt
  binutils-mingw-w64-x86-64           python3-donut
  dnsmap                              python3-dropbox
  dotnet-apphost-pack-6.0             python3-fuzzywuzzy
  dotnet-host                         python3-gitdb
  dotnet-hostfxr-6.0                  python3-httpx-ntlm
  dotnet-runtime-6.0                  python3-humanize
  dotnet-runtime-deps-6.0             python3-jeepney
  dotnet-sdk-6.0                      python3-jq
  dotnet-targeting-pack-6.0           python3-jwcrypto
  dsniff                              python3-levenshtein
  ettercap-common                     python3-macholib
  ettercap-graphical                  python3-markdown2
  eyewitness                          python3-md2pdf
  feroxbuster                         python3-obfuscator
  figlet                              python3-ply
  finger                              python3-pydantic-settings
  gcc-mingw-w64-base                  python3-pydispatch
  gcc-mingw-w64-i686-win32            python3-pydyf
  gcc-mingw-w64-i686-win32-runtime    python3-pyfiglet
  gcc-mingw-w64-x86-64-win32          python3-pygame
  gcc-mingw-w64-x86-64-win32-runtime  python3-pyinstaller
  httpx-toolkit                       python3-pymysql
  hyphen-en-us                        python3-pyphen
  libapache2-mod-php                  python3-pyshodan
  libjq1                              python3-pyvirtualdisplay
  libluajit-5.1-2                     python3-pyvnc
  libluajit-5.1-common                python3-qasync
  libnids1.21t64                      python3-qrcode
  libonig5                            python3-rapidfuzz
  libopusfile0                        python3-secretsocks
  libpcre2-32-0                       python3-serial-asyncio
  libportmidi2                        python3-smmap
  libsdl2-2.0-0                       python3-sqlalchemy-utc
  libsdl2-image-2.0-0                 python3-stix2
  libsdl2-mixer-2.0-0                 python3-stix2-patterns
  libsdl2-ttf-2.0-0                   python3-stone
  libsmb2-6                           python3-tinyhtml5
  libxar1                             python3-tld
  libxmp4                             python3-wapiti-swagger
  medusa                              python3-websockify
  mingw-w64-common                    python3-zlib-wrapper
  mingw-w64-i686-dev                  rsh-redone-client
  mingw-w64-x86-64-dev                smtp-user-enum
  netstandard-targeting-pack-2.1      sparta-scripts
  nuclei                              toilet-fonts
  oracle-instantclient-basic          unicornscan
  pcre2-utils                         urlscan
  pyinstaller                         wapiti
  pyinstaller-hooks-contrib           weasyprint
  python3-altgraph                    xar
Use 'sudo apt autoremove' to remove them.

Installing:
  git
                                                                             
Suggested packages:
  git-doc  git-email  git-gui  gitk  gitweb  git-cvs  git-svn

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 2
  Download size: 9,410 kB
  Space needed: 52.2 MB / 62.9 GB available

Get:1 http://mirror.krfoss.org/kali kali-rolling/main amd64 git amd64 1:2.53.0-1 [9,410 kB]
Fetched 9,410 kB in 2s (5,522 kB/s)
Selecting previously unselected package git.
(Reading database… 418955 files and directories currently installed.)
Preparing to unpack …/git_1%3a2.53.0-1_amd64.deb…
Unpacking git (1:2.53.0-1)…
Setting up git (1:2.53.0-1)…
Processing triggers for kali-menu (2026.3.4)…
```
---
3.	В README.md нового репозитория привести листинги выполнения всех команд по манипуляции 
с файлами (touch, cat, nano, pwd, ls, head, tail, less, tree, mkdir, rm, rmdir) 
с различными параметрами (если они есть у данной команды).
---	
***touch***
```bash

──(kali㉿kali)-[~/lab]
└─$ ls
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$               
                                               
┌──(kali㉿kali)-[~/lab]
└─$ touch file.txt           
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls            
file.txt

──(kali㉿kali)-[~/lab]
└─$ touch file1.txt file2.txt
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls
file1.txt  file2.txt  file.txt

┌──(kali㉿kali)-[~/lab]
└─$ ls -lah
total 8.0K

-rw-rw-r--  1 kali kali    0 Oct  8 01:12 file.txt
┌──(kali㉿kali)-[~/lab]
└─$ touch -t 202110081200 file.txt
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls -lah                       
total 8.0K
-rw-rw-r--  1 kali kali    0 Oct  8  2021 file.txt
```
---
***cat***
```bash
──(kali㉿kali)-[~/lab]
└─$ cat file.txt                  
1. str
2. str
text
dig

symb ***

┌──(kali㉿kali)-[~/lab]
└─$ cat > newfile.txt
 I am entering text from the keyboard.
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ cat newfile.txt  
 I am entering text from the keyboard.
                                            
```
---
***nano***
```bach
  GNU nano 9.2                                      file.txt *                                              
1. str
2. str
text
dig

symb ***

nano edit

^G Help        ^O Write Out   ^F Where Is    ^K Cut         ^T Execute     ^C Location    M-U Undo
^X Exit        ^R Read File   ^\ Replace     ^U Paste       ^J Justify     ^/ Go To Line  M-E Redo

──(kali㉿kali)-[~/lab]
└─$ nano file.txt                        
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ cat file.txt   
1. str
2. str
text
dig

symb ***

nano edit
```
---
***pwd***
```bash
──(kali㉿kali)-[~/lab]
└─$ man pwd  

NAME
     pwd - print name of current/working directory

SYNOPSIS
     pwd [OPTION]...

DESCRIPTION
     Print the full filename of the current working directory.

     -L, --logical
            use PWD from environment, even if it contains symlinks

     -P, --physical
            resolve all symlinks

     --help
            display this help and exit

     --version
            output version information and exit

     If no option is specified, -P is assumed.

     Your  shell  may  have  its  own  version of pwd, which usually supersedes the version described here.
     Please refer to your shell's documentation for details about the options it supports.

──(kali㉿kali)-[~/lab]
└─$ pwd -L
/home/kali/lab
```
---
***ls***
```bash
┌──(kali㉿kali)-[~/lab]
└─$ man ls 
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls -A  
file1.txt  file2.txt  file.txt  newfile.txt
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls -a  
.  ..  file1.txt  file2.txt  file.txt  newfile.txt
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ ls -lah
total 16K
drwxrwxr-x  2 kali kali 4.0K Oct  8 01:23 .
drwx------ 19 kali kali 4.0K Oct  8 01:11 ..
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file1.txt
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file2.txt
-rw-rw-r--  1 kali kali   44 Oct  8 01:23 file.txt
-rw-rw-r--  1 kali kali   39 Oct  8 01:21 newfile.txt
```
---
***head***
```bash
┌──(kali㉿kali)-[~/lab]
└─$ head -n 2 file.txt
1. str
2. str
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ head -c 20 file.txt
1. str
2. str
text
d                                                                                                            
```
---
***tail***
```bach
──(kali㉿kali)-[~/lab]
└─$ tail file.txt
drwxrwxr-x  2 kali kali 4.0K Oct  8 01:23 .
drwx------ 19 kali kali 4.0K Oct  8 01:11 ..
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file1.txt
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file2.txt
-rw-rw-r--  1 kali kali    0 Oct  8 01:33 file.txt
-rw-rw-r--  1 kali kali   39 Oct  8 01:21 newfile.txt
file1.txt
file2.txt
file.txt
newfile.txt
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ tail -n 5 file.txt
-rw-rw-r--  1 kali kali   39 Oct  8 01:21 newfile.txt
file1.txt
file2.txt
file.txt
newfile.txt
```
---
***less***
```bash
──(kali㉿kali)-[~/lab]
└─$ less file.txt 

1. str
2. str
text
dig

symb ***

nano edit
total 12K
drwxrwxr-x  2 kali kali 4.0K Oct  8 01:23 .
drwx------ 19 kali kali 4.0K Oct  8 01:11 ..
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file1.txt
-rw-rw-r--  1 kali kali    0 Oct  8 01:13 file2.txt
-rw-rw-r--  1 kali kali    0 Oct  8 01:33 file.txt
-rw-rw-r--  1 kali kali   39 Oct  8 01:21 newfile.txt
file1.txt
file2.txt
file.txt
newfile.txt
file.txt (END)
```
---
***three***
```bash
──(kali㉿kali)-[~/lab]
└─$ tree -L 2 ../
../
├── Desktop
├── Documents
├── Downloads
├── file.txt
├── lab
│   ├── file1.txt
│   ├── file2.txt
│   ├── file.txt
│   └── newfile.txt
├── Music
├── Pictures
├── Projects
├── Public
├── Templates
└── Videos

11 directories, 5 files
──(kali㉿kali)-[~/lab]
└─$ tree -h
[4.0K]  .
├── [   0]  file1.txt
├── [   0]  file2.txt
├── [ 393]  file.txt
└── [  39]  newfile.txt

1 directory, 4 files
```
---
***mkdir, rm, rmdir***
```bash

            
──(kali㉿kali)-[~/lab]
└─$ rm -i file.txt
rm: remove regular file 'file.txt'? n


┌──(kali㉿kali)-[~/lab]
└─$ man rmdir 

RMDIR(1)                                       User Commands                                       RMDIR(1)

NAME
     rmdir - remove empty directories

SYNOPSIS
     rmdir [OPTION]... DIRECTORY...

DESCRIPTION
     Remove the DIRECTORY(ies), if they are empty.

     --ignore-fail-on-non-empty
            ignore each failure to remove a non-empty directory

     -p, --parents
            remove DIRECTORY and its ancestors; e.g., 'rmdir -p a/b' is similar to 'rmdir a/b a'

     -v, --verbose
            output a diagnostic for every directory processed

     --help
            display this help and exit

     --version
            output version information and exit
            
┌──(kali㉿kali)-[~/lab]
└─$ man mkdir
            
NAME
     mkdir - make directories

SYNOPSIS
     mkdir [OPTION]... DIRECTORY...

DESCRIPTION
     Create the DIRECTORY(ies), if they do not already exist.

     Mandatory arguments to long options are mandatory for short options too.

     -m, --mode=MODE
            set file mode (as in chmod), not a=rwx - umask

     -p, --parents
            no  error  if  existing, make parent directories as needed, with their file modes unaffected by
            any -m option

     -v, --verbose
            print a message for each created directory

     -Z     set SELinux security context of each created directory to the default type

     --context[=CTX]
            like -Z, or if CTX is specified then set the SELinux or SMACK security context to CTX

     --help
            display this help and exit

     --version
            output version information and exit
```
---
4.  «Сломать» операционную систему (rm -rf) или установить какой-нибудь пакет или программу,
 затем восстановиться из snapshot и продемонстрировать.
 
 ***создан snapshot***
Удалил GIT.
```bash
──(kali㉿kali)-[~]
└─$ sudo apt remove git  
The following packages were automatically installed and are no longer required:
  aspnetcore-runtime-6.0              libportmidi2                    python3-ply
  aspnetcore-targeting-pack-6.0       libsdl2-2.0-0                   python3-pydantic-settings
  binutils-mingw-w64-base             libsdl2-image-2.0-0             python3-pydispatch
  binutils-mingw-w64-i686             libsdl2-mixer-2.0-0             python3-pydyf
  binutils-mingw-w64-x86-64           libsdl2-ttf-2.0-0               python3-pyfiglet
  dnsmap                              libsmb2-6                       python3-pygame
  dotnet-apphost-pack-6.0             libxar1                         python3-pyinstaller
  dotnet-host                         libxmp4                         python3-pymysql
  dotnet-hostfxr-6.0                  medusa                          python3-pyphen
  dotnet-runtime-6.0                  mingw-w64-common                python3-pyshodan
  dotnet-runtime-deps-6.0             mingw-w64-i686-dev              python3-pyvirtualdisplay
  dotnet-sdk-6.0                      mingw-w64-x86-64-dev            python3-pyvnc
  dotnet-targeting-pack-6.0           netstandard-targeting-pack-2.1  python3-qasync
  dsniff                              nuclei                          python3-qrcode
  ettercap-common                     oracle-instantclient-basic      python3-rapidfuzz
  ettercap-graphical                  pcre2-utils                     python3-secretsocks
  eyewitness                          pyinstaller                     python3-serial-asyncio
  feroxbuster                         pyinstaller-hooks-contrib       python3-smmap
  figlet                              python3-altgraph                python3-sqlalchemy-utc
  finger                              python3-antlr4                  python3-stix2
  gcc-mingw-w64-base                  python3-browser-cookie3         python3-stix2-patterns
  gcc-mingw-w64-i686-win32            python3-cssselect2              python3-stone
  gcc-mingw-w64-i686-win32-runtime    python3-docopt                  python3-tinyhtml5
  gcc-mingw-w64-x86-64-win32          python3-donut                   python3-tld
  gcc-mingw-w64-x86-64-win32-runtime  python3-dropbox                 python3-wapiti-swagger
  git-man                             python3-fuzzywuzzy              python3-websockify
  httpx-toolkit                       python3-gitdb                   python3-zlib-wrapper
  hyphen-en-us                        python3-httpx-ntlm              rsh-redone-client
  libapache2-mod-php                  python3-humanize                smtp-user-enum
  liberror-perl                       python3-jeepney                 sparta-scripts
  libjq1                              python3-jq                      toilet-fonts
  libluajit-5.1-2                     python3-jwcrypto                unicornscan
  libluajit-5.1-common                python3-levenshtein             urlscan
  libnids1.21t64                      python3-macholib                wapiti
  libonig5                            python3-markdown2               weasyprint
  libopusfile0                        python3-md2pdf                  xar
  libpcre2-32-0                       python3-obfuscator
Use 'sudo apt autoremove' to remove them.

REMOVING:
  commix               kali-tools-top10      msfpc                set
  git                  legion                powershell-empire    unicorn-magic                     
  kali-linux-default   manpages-utils        python3-git                                            
  kali-linux-headless  metasploit-framework  python3-pyexploitdb                                    
                                                                                                    
Summary:
  Upgrading: 0, Installing: 0, Removing: 14, Not Upgrading: 2
  Freed space: 777 MB

Continue? [Y/n] y
(Reading database… 456386 files and directories currently installed.)
Removing kali-linux-default (2026.3.9)…
Removing kali-linux-headless (2026.3.9)…
Removing commix (4.1-0kali1)…
Removing legion (0.7.0-0kali2)…
Removing python3-pyexploitdb (0.3.45-0kali2)…
Removing python3-git (3.1.61-1)…
Removing powershell-empire (6.6.0-0kali1)…
Removing kali-tools-top10 (2026.3.9)…
Removing manpages-utils (6.19-3)…
Removing unicorn-magic (3.12-0kali3)…
Removing set (8.1.3+git20260604-0kali1)…
Removing msfpc (1.4.5-0kali3)…
Removing metasploit-framework (6.5.3-0kali1)…
Removing git (1:2.53.0-1)…
Processing triggers for libc-bin (2.43-6)…
Processing triggers for man-db (2.13.1-1)…
Processing triggers for wordlists (2026.2.0)…
Processing triggers for kali-menu (2026.3.4)…
```
---
```bash
┌──(kali㉿kali)-[~]
└─$ sudo git             
[sudo] password for kali: 
sudo: git: command not found
```

После восстановления из снапшоте пакет git восстановился.

---


```bash
┌──(kali㉿kali)-[~/lab]
└─$ sudo visudo -f /etc/sudoers.d/kali            
[sudo] password for kali: 

kali ALL=(ALL:ALL) NOPASSWD: ALL

                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ sudo visudo -c
/etc/sudoers: parsed OK
/etc/sudoers.d/kali: bad permissions, should be mode 0440
/etc/sudoers.d/kali-grant-root: parsed OK
/etc/sudoers.d/ospd-openvas: parsed OK
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ sudo chmod 440 /etc/sudoers.d/kali            
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ 

┌──(kali㉿kali)-[~/lab]
└─$ sudo ls                           
file1.txt  file2.txt  file.txt  newfile.txt
                                              
```
---
6. Установить гипервизор 1 типа (например, Proxmox), затем внутри гипервизора установить виртуальную машину по выбору. 

***PROXMOX  используем во многих компания.  можно я этого делать не буду :))***

---
7. Написать простой демон с помощью systemd, который будет осуществлять мониторинг, например, писать в какой-нибудь 
log-файл информацию каждые 5 минут о том, какая нагрузка на процессор, память, сколько процессов запущено
```bash
──(kali㉿kali)-[~/lab]
└─$ sudo mkdir -p /usr/local/bin
sudo nano /usr/local/bin/sys_monitor.sh
#!/bin/bash

LOG_FILE="/var/log/sys_monitor.log"
TMP_FILE="/tmp/sys_monitor_raw.txt"

LOAD=$(awk '{print $1, $2, $3}' /proc/loadavg)

USED_MEM=$(free -m | awk '/Mem:/ {print $3}')
FREE_MEM=$(free -m | awk '/Mem:/ {print $7}')

PROC_COUNT=$(ps -e --no-headers | wc -l)
THREAD_COUNT=$(ps -eT --no-headers | wc -l)

TIMESTAMP=$(date '+%Y-%m-%d %H:%M:%S')
LOG_ENTRY="${TIMESTAMP} | Load: ${LOAD} | Mem: ${USED_MEM}MB used / ${FREE_MEM}MB free | Processes: ${PROC_>

echo "${LOG_ENTRY}" >> "${LOG_FILE}"

exit 0


──(kali㉿kali)-[~/lab]
└─$ sudo chmod +x /usr/local/bin/sys_monitor.sh

──(kali㉿kali)-[~/lab]
└─$ sudo chown root:root /usr/local/bin/sys_monitor.sh

──(kali㉿kali)-[~/lab]
└─$ sudo nano /etc/systemd/system/sys-monitor.service
[Unit]
Description=System resource monitor
Wants=sys-monitor.timer

[Service]
Type=oneshot
ExecStart=/usr/local/bin/sys_monitor.sh

┌──(kali㉿kali)-[~/lab]
└─$ sudo nano /etc/systemd/system/sys-monitor.timer
[Unit]
Description=Run sys-monitor.service every 5 minutes

[Timer]
OnBootSec=5min
OnUnitActiveSec=5min
Persistent=true

[Install]
WantedBy=timers.target

┌──(kali㉿kali)-[~/lab]
└─$ sudo touch /var/log/sys_monitor.log
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ sudo chmod 644 /var/log/sys_monitor.log
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ sudo chown root:root /var/log/sys_monitor.log
                                                    
┌──(kali㉿kali)-[~/lab]
└─$ sudo systemctl daemon-reload
                                  
──(kali㉿kali)-[~/lab]
└─$ sudo systemctl enable --now sys-monitor.timer
Created symlink '/etc/systemd/system/timers.target.wants/sys-monitor.timer' → '/etc/systemd/system/sys-monitor.timer'.
┌──(kali㉿kali)-[~/lab]
└─$ systemctl list-timers --all | grep sys-monitor
Thu 2026-10-08 02:15:24 EDT 4min 43s Thu 2026-10-08 02:10:24 EDT      16s ago sys-monitor.timer            sys-monitor.service

──(kali㉿kali)-[~/lab]
└─$ systemctl list-timers --all | grep sys-monitor
Thu 2026-10-08 02:15:24 EDT 4min 43s Thu 2026-10-08 02:10:24 EDT      16s ago sys-monitor.timer            sys-monitor.service
                                                                                                            
┌──(kali㉿kali)-[~/lab]
└─$ systemctl status sys-monitor.service
○ sys-monitor.service - System resource monitor
     Loaded: loaded (/etc/systemd/system/sys-monitor.service; static)
     Active: inactive (dead) since Thu 2026-10-08 02:20:07 EDT; 4s ago
 Invocation: 1469647c68354ebfbff17b2944cbd15e
TriggeredBy: ● sys-monitor.timer
    Process: 41344 ExecStart=/usr/local/bin/sys_monitor.sh (code=exited, status=0/SUCCESS)
   Main PID: 41344 (code=exited, status=0/SUCCESS)
   Mem peak: 4.5M
        CPU: 61ms

Oct 08 02:20:07 kali systemd[1]: Starting sys-monitor.service - System resource monitor...
Oct 08 02:20:07 kali systemd[1]: sys-monitor.service: Deactivated successfully.
Oct 08 02:20:07 kali systemd[1]: Finished sys-monitor.service - System resource monitor.

──(kali㉿kali)-[~/lab]
└─$ tail -n 2 /var/log/sys_monitor.log
2026-10-08 02:19:35 | Load: 0.16 0.16 0.11 | Mem: 1042MB used / 889MB free | Processes: 226 | Threads: 513
2026-10-08 02:20:07 | Load: 0.09 0.15 0.10 | Mem: 1052MB used / 878MB free | Processes: 232 | Threads: 523


```

---
***не сменил часовой пояс***
```bash
──(kali㉿kali)-[~/lab]
└─$ sudo timedatectl set-timezone Asia/Yekaterinburg
──(kali㉿kali)-[~/lab]
└─$ timedatectl status
               Local time: Thu 2026-10-08 11:26:37 +05
           Universal time: Thu 2026-10-08 06:26:37 UTC
                 RTC time: Thu 2026-10-08 06:26:37
                Time zone: Asia/Yekaterinburg (+05, +0500)
System clock synchronized: yes
              NTP service: active
          RTC in local TZ: no
                                                      
```

                                                                                      
                                                                                      


                           

                       
                       

                               
                                                
                               
  
 


```
