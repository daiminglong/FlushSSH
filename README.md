# FlushSSH
A tool helping to run CLI commands from files on multiple servers  
[![Build status](https://ci.appveyor.com/api/projects/status/m232719gvcg0m1qc?svg=true)](https://ci.appveyor.com/project/DavyVan/flushssh)
[![Build Status](https://travis-ci.org/DavyVan/FlushSSH.svg?branch=master)](https://travis-ci.org/DavyVan/FlushSSH)  


# Installation
Windwos: Use the setup.exe  
Linux: For now, you must compile from source, please see HOW_TO_CONTRIBUTE.md  


# Usage & Feathers
    FlushSSH {hosts_file_path} {cmd_file_path}  
**hosts_file_path**: contains all of the hosts you want to connect, please use the following format.  

    +---------------+----------+----------+   
    |hostsname (IP) | username | password |
    +---------------+----------+----------+

**cmd_file_path**: Contains all of the commands you want to execute on remote host(s). The format is quite simple with one command per line. e.g.

    cd ~
    mkdir myfolder

For now, some limitations:
* all of the hosts share the only one command file.  
* Only support authentication with password.  
* Connect and execute one by one.
* Store all of the echo in files, one host one file, named after hosts' hostname(IP).  
* Only support port 22.
* Only on Windows, only Windows 10 is tested.

Will be better in future versions.  
## Update history
### V1.0 @ 2017.2.26 (1st release)
* Add Travis-CI & Appveyor test
* Add SIGINT handling
* Add installer for Windows Vista+


### V0.8 @ 2017.2.22 (Initial)
