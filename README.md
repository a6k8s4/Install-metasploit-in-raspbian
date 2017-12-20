Install METASPLOIT in Raspberry pi 3/Zero with raspbian
======================================================================


# Requirements

* Raspberry pi (3 or Zero )
* Micro SD card flashed with Raspbian OS [download raspbian](https://www.raspberrypi.org/downloads/raspbian/ )
* HDMI cable, key board and mouse (not require for headless setup)
* Internet connection(ethernet or wifi)
* Power supply to Raspberry pi

# Process

* Setup Raspberry pi(Zero or 3) components, boot up and connect to internet either with HDMI cable and keyboard & mouse Or headless( lot of tutorial available in youtube to setup headless).

* Go to terminal for metasploit set up(if you are using through headless then you are by default in Terminal)
* Update the Raspbian OS.

```
sudo apt-get update
```
* if you want then upgrade also.

```
sudo apt-get upgrade
```
* Then just fullfill the dependancies.

 ```
 sudo apt-get install build-essential libreadline-dev libssl-dev libpq5 libpq-dev libreadline5 libsqlite3-dev libpcap-dev subversion git-core autoconf postgresql pgadmin3 curl zlib1g-dev libxml2-dev libxslt1-dev libyaml-dev nmap
 ```
 * Enter the below command to add the build repository and install the Metasploit Framework package
 
 ```
 sudo curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && chmod 755 msfinstall && ./msfinstall
 ```
 
 * It will take 15 mins(according to internet speed, so take a break). After the installation completes, open the terminal and type the below to start Metasploit console.
 
 ```
 ./msfconsole
 ```
 
 Or
 
 ```
 msfconsole
 ```
 
 * It will ask you to set up new database, Type y or yes to continue.
 
 
 * BOOM ... Now you setted up Metasploit completely & you are in msf console..
 
 * To check the database status type the below command in msf console.
 
 ```
 db_status
 ```
 
 * If everything gone perfect, you will see this:
 
``` [*] postgresql connected to msf ```

* ENJOY....

 
 
