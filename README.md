# BRG-27-labs

28/06/2025 AM Session - 

Setting Up and Exploring Linux
Linux installation 
-download VMware (https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
-download Ubuntu Desktop.iso (https://ubuntu.com/download/desktop)

Start to install VMware and Ubuntu.iso
![image](https://github.com/user-attachments/assets/2f021cee-f27f-4956-b268-af23db41a205)

Create a GitHub account and document progress.
Created a GitHub account.
 ![image](https://github.com/user-attachments/assets/e6138d1e-9ba1-4dad-b1a4-f79b2cf7f181)

Create a new repository 
 ![image](https://github.com/user-attachments/assets/3064bb3b-eb5a-400d-92d8-b227bf198bf8)

Clone the repository to my local machine.
![image](https://github.com/user-attachments/assets/f00e1008-ed42-4623-94ee-3e44b2953b57)

1a-1:VirtualBox Installed 

Reusable_Learning_Objects/obtaining_a_linux_environment.md


Step 1: Install Ubuntu using VMware
Step 2: Download Ubuntu.iso file
![image](https://github.com/user-attachments/assets/40b477d5-fde3-45c6-a185-281c00cb597a)
Download VMware 17 Pro
![image](https://github.com/user-attachments/assets/ce30cad5-e653-4aa6-b438-593ed6330242)

Step 3: Install Ubuntu 
![image](https://github.com/user-attachments/assets/d3635652-ef20-4b93-b266-50ef09f6daa3)

Key in the username and password

![image](https://github.com/user-attachments/assets/17028ce2-301e-4fa6-96a8-fd8a097eb5d6)

Configure the VM 20GB storage 4GB RAM.
![image](https://github.com/user-attachments/assets/7e1911e3-358f-4532-b6d9-b66768175494)

Step 4: A New Ubuntu VM was created.
Step 5: Networking Mode Configured (NAT)
![image](https://github.com/user-attachments/assets/4429cb70-b85e-4a8a-8217-ded26a01d32a)

Step 6: Ubuntu Running with GUI or CLI Access
![image](https://github.com/user-attachments/assets/af0fb998-4f8c-4f59-979b-476cddceab4e)

Step 7: Install VirtualBox Guest Additons : sudo apt update
![image](https://github.com/user-attachments/assets/88cdf273-1d2e-4b12-ad98-cc8cd3376a9a)

sudo apt install virtualbox-guest-utils virtualbox-guest-x11
![image](https://github.com/user-attachments/assets/3bc2a723-62ff-4c25-9b57-5d7a4e27758f)
sudo reboot

Step 8: SSH Enabled
![image](https://github.com/user-attachments/assets/87c62e10-e7b4-4a8e-a4e7-e367e886c21b)

Test from host OS
![image](https://github.com/user-attachments/assets/6f732482-93f5-4ae8-9a18-70093be2945b)

Step 9: WSL installed
![image](https://github.com/user-attachments/assets/72fa3052-6cd0-41d8-bc38-f3b33b330db1)

Step 10: Different Distro Explored
Installed Kali
![image](https://github.com/user-attachments/assets/c34e0e94-e9ed-4120-bb0f-fab7d682b934)

------------------------------------------------------------------------------------------------

Lab 1a-2: Ubuntu Desktop and Command Line Familiarisation

[Server_Environments_and_Architectures/ubuntu_desktop_familiarisation.md]
(https://github.com/SCH-IT-MurdochUni/NetworkingLabs/blob/e0a4d12bb05b3a4bf0654b9c427c8eaecbee065a/Server_Environments_and_Architectures/ubuntu_desktop_familiarisation.md)

Step 1: Open Firefox
![image](https://github.com/user-attachments/assets/4e95a122-e20f-4a9e-b244-cef2cb2dbbfa)

Open the File and the App Store.
![image](https://github.com/user-attachments/assets/09383411-e85d-45d2-8265-7d4641170dad)

------------------------------------------------------------------------------------------------

Step 2: Terminal Command Outpu
Familiarity with Ubuntu Linux 
try command: ps -e
![image](https://github.com/user-attachments/assets/b7375bf0-0a47-4440-9a45-6962e90bfe94)

Command: top
![image](https://github.com/user-attachments/assets/56bff7b8-bb23-47c8-984d-0c6c1fede3f1)

Command: q to quit the top command
Command: ls
![image](https://github.com/user-attachments/assets/d8c77900-d16a-4912-87a3-0e02a3607d96)

Command: ls -la
![image](https://github.com/user-attachments/assets/cc3106f2-818a-4b90-8525-e103a04040e3)

The difference between ls and ls -la
ls
•	Lists files and directories in the current directory.
•	Shows only names (no hidden files, no detailed info).

ls -la (or ls -l -a)
•	-l → Long format (detailed listing).
•	-a → Show all files (including hidden files starting with .).


Command: ls -alt
![image](https://github.com/user-attachments/assets/12943b87-7268-454d-824d-cc88e4fb5c4b)

Try command: touch testfile (to create a file)
Command: gedit testfile (edit the file)
Command: featherpad testfile( to view the file)

![image](https://github.com/user-attachments/assets/35bcb304-5d0a-47ee-98e4-258a07703c83)

Command: nano testfile
![image](https://github.com/user-attachments/assets/a91a516f-5be4-42f8-b189-2c693a24ec08)

![image](https://github.com/user-attachments/assets/d770d468-6098-4cef-a776-467510d50f1c)

Can You Use gedit Over a Remote Terminal?
No, not easily—unless you have X11 forwarding enabled. Here's why:
1.	gedit Requires a GUI
o	It’s a graphical application (part of GNOME) and needs a desktop environment.
o	If you’re connected via SSH (just a terminal), there’s no GUI to display gedit.

2.	Possible Workaround (X11 Forwarding)
o	If your SSH connection supports X11 forwarding (ssh -X user@remote), you might be able to run gedit, but:
	It will be slow (graphics are sent over the network).
	Many servers don’t have GUI libraries installed.
	Not practical for most remote admin tasks.

3.	Better Alternative: nano (or vim/emacs)
o	Since nano is terminal-based, it works seamlessly over SSH.
o	No extra setup needed—just run it.

When to Use Which?
•	Use nano (or vim/emacs) for remote work → Fast, reliable, no GUI needed.
•	Use gedit only locally → Better for GUI environments with mouse support.

Command: cat testfile
![image](https://github.com/user-attachments/assets/0aa5c0b5-d814-4c37-95bb-50f2802d974e)

Command: less testfile
![image](https://github.com/user-attachments/assets/9855c5f7-532d-4742-bea0-d13df5a71aaa)

------------------------------------------------------------------------------------------------

Step 3: File Operations Practiced
Command: cp testfile testfile2
Run: ls
command cp testfile2 testfile3
rerun: ls
![image](https://github.com/user-attachments/assets/221e02c1-4f8b-4c41-bc5b-fe18d3642904)

Key Differences
1.	Original File Preservation
o	cp → Keeps the original file.
o	mv → Removes the original (unless renaming in the same directory).

2.	Storage Impact
o	cp → Uses additional disk space (since it makes a copy).
o	mv → Just changes the file's path, no extra space used.

3.	Common Use Cases
o	Use cp when:
	You need a backup (cp important.txt important_backup.txt).
	You want to duplicate a file to another directory (cp file.txt ~/Documents/).
o	Use mv when:
	You want to rename a file (mv oldname.txt newname.txt).
	You want to move a file to another location (mv file.txt /tmp/).

Run command: ls -lah
![image](https://github.com/user-attachments/assets/2aac7dac-4123-4a22-952b-bc941feffcf6)

•	Command: ls
•	Action: Lists files and directories in the current folder.
•	Details:
o	Shows only visible files (no hidden files).
o	No extra details (just names).
Command: ls -la (or ls -l -a)
Action: Lists all files (including hidden) in long format.
Details:
-l → Long format (shows permissions, owner, size, timestamp).
-a → Shows all files (including hidden ones starting with .).
File sizes are shown in bytes. 

------------------------------------------------------------------------------------------------

Step 4- System Information Commands 
Command: uname -a
Command: lsb_release -a
![image](https://github.com/user-attachments/assets/9a5454c3-0983-40e5-a986-68451a5c51e0)

Command: hostnamectl
![image](https://github.com/user-attachments/assets/2b36719c-544a-4976-b92e-f3bc2223ce30)

Command: ls -alt
![image](https://github.com/user-attachments/assets/0a645168-f936-4f4a-a47f-61c52a064531)

------------------------------------------------------------------------------------------------

Step 5: User Privilege Experiment
Super User
Command: whoami, adduser abcd1234, sudo whoami, sudo adduser abcd1234

![image](https://github.com/user-attachments/assets/f443eeee-18fe-4270-a448-80588220b299)

------------------------------------------------------------------------------------------------

Step 6- Network Configuration
Command: ip a
![image](https://github.com/user-attachments/assets/b66e1602-e188-4b84-98dd-24ebca8a148c)

Can’t ping [neighborsipaddress] because I didn’t connect their network.
Can ping 8.8.8.8 because is the Google default public IP

------------------------------------------------------------------------------------------------

Step 7: 
Hosts
Command: less /etc/hosts
![image](https://github.com/user-attachments/assets/99125d82-25c7-40a2-89c1-4ac71e6f3ad7)

Command: sudo nano /etc/hosts
Add 8.8.8.8 GoogleEpicDNS
![image](https://github.com/user-attachments/assets/ca116028-f4bc-4216-b5ba-3cc3c60b8a36)

Ping GoogleEpicDNS
![image](https://github.com/user-attachments/assets/15b4fd0c-f88a-4f9c-94c9-c82c93928da7)

------------------------------------------------------------------------------------------------

Step 8: DNS Lookup Performed
Command: nslookup google.com
![image](https://github.com/user-attachments/assets/1643e4b6-b385-4d87-9e9c-a33654e73038)

Command: sudo apt install whois, whois google.com
![image](https://github.com/user-attachments/assets/f6d7ef18-09ed-4372-a693-7ac01c8ccab9)

------------------------------------------------------------------------------------------------

Step 9: Public and Private IP Reflection
Command: ip a

![image](https://github.com/user-attachments/assets/4b838264-2367-40d6-9141-b42fdd815ad1)

IP from whatismyipaddress.com

![image](https://github.com/user-attachments/assets/95f44cfe-b3f7-4571-bddf-109f4e232f89)

The IP address shown by ip a is my private IP used within my local network, while the IP shown on whatismyipaddress.com is my public IP assigned by my ISP for internet access—these are different because my system is behind a router using NAT (Network Address Translation).

------------------------------------------------------------------------------------------------

Step 10: Hardware Info Commands 
Command: lsusb, lspci
![image](https://github.com/user-attachments/assets/2200d107-ca24-4ae7-8ab5-b042b1680e0b)

Less /proc/cpuinfo and settings > About this computer
![image](https://github.com/user-attachments/assets/19debcf2-7ac3-4de7-8cd9-7b699cb86ee8)

------------------------------------------------------------------------------------------------

Step 11: Output Redirection Practiced
Command: lsusb > output_of_lsusb

![image](https://github.com/user-attachments/assets/72ee1508-21c9-4fa8-9cd2-1fa7738d1129)

Try:
less output_of_lsusb

![image](https://github.com/user-attachments/assets/9831a5a1-bdf4-41d1-9e5b-1fc0705ea5cc)

cat output_of_lsusb
![image](https://github.com/user-attachments/assets/f67be065-1c91-4a63-ba9d-e97d004434c6)

•	cat output_of_lsusb Behavior:
o	Dumps the entire content of the file to the terminal at once.
o	No interactivity – you can't scroll or search.
o	Best for short outputs or when you want to quickly see content.

•	less output_of_lsusb Behavior:
o	Opens the file in an interactive pager.
o	Allows scrolling (↑/↓, Page Up/Down).
o	Supports search (/ + type query, then Enter).
o	Press q to quit.
o	Best for long outputs or when you need to analyze details.


Command: ls -la output_of_lsusb, rm output_of_lsusb (to remove file)
![image](https://github.com/user-attachments/assets/f2ee9e47-2c54-47cb-a598-fef9217bf7b6)

------------------------------------------------------------------------------------------------

Step 12: Software installed
1. Using Google Docs
-Create a new document and type Test ICT171 assignment.

![image](https://github.com/user-attachments/assets/4aab03c7-3d32-4558-bdea-6002e7db41b2)

2. Binary Download
Download a .deb file (e.g., Chrome or Opera) from the official website.
![image](https://github.com/user-attachments/assets/ce53422c-8a0f-4906-8c30-114fa8ad6da1)

And run: sudo dpkg -i opera.deb
 ![image](https://github.com/user-attachments/assets/5c14b54f-e724-470f-b2d8-3caf1718368c)

Opera installed
![image](https://github.com/user-attachments/assets/04b75bf4-afb8-4884-b8b8-6a1617616128)

3. Repository install via Ubuntu Software Centre 
![image](https://github.com/user-attachments/assets/9505f6a3-b73c-424a-803a-b2c0a0b97912)

------------------------------------------------------------------------------------------------

Step 13: Installing Software
Downloading and installing a binary a trusted repository
Command: less /etc/apt/sources.list, sudo apt update, sudo apt upgrade

![image](https://github.com/user-attachments/assets/d3103b1f-6ba9-4792-9169-d266561a328f)

![image](https://github.com/user-attachments/assets/f5bb4075-0c38-4ffd-ba2d-f604bf5a883e)

sudo apt install vlc
![image](https://github.com/user-attachments/assets/9abfd16f-6299-417b-9831-8ab23965200d)

Installing from source code
sudo apt install build-essential
![image](https://github.com/user-attachments/assets/4cb58e68-920b-4a42-83b5-1704a50cc571)

------------------------------------------------------------------------------------------------

Step 14: Source Code Compilation
Save a file to hello_world.c

![image](https://github.com/user-attachments/assets/17a893e4-4941-45f5-af0f-045434e61b0e)

Compile it with: gcc hello_world.c -o hello_world_executable
Execute: ./hello_world_executable
Set permission: chmod 777 hello_world_executable
Run: less hello_world.c , less hello_world_executable
![image](https://github.com/user-attachments/assets/011f83ea-c69b-4661-b017-cfb6adbbbf03)

![image](https://github.com/user-attachments/assets/e9bcaac8-f4b8-4263-98c0-56f11bcaa6c6)

------------------------------------------------------------------------------------------------

Step 15: Reflection Summary
I looked at both the GUI and the CLI in Ubuntu during this lab. The GUI was easy to use and made sense, especially when it came to things like browsing the web or installing apps through the applications center. The CLI, on the other hand, gave you more power and speed when it comes to scripting and system-level tasks. 
I looked into a variety of different ways to install software, such as SaaS options like Google Docs, repository-based installs with apt, manual .deb file installations, and making source code. There are pros and cons to each choice. You don't have to install SaaS on your computer, and it's easy to use. 
It is safe and simple to install from a repository. You can choose how to do things with manual installs, and you can control the full build process using source compilation. For everyday tasks, I appreciate using the GUI, but for development and troubleshooting, I really like how strong the CLI is. I want to be a software engineer, so I know that I need to be able to use both interfaces properly so that I can work in a variety of places.

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Day 2 – AM
Total Cost of Ownership (TCO) Report: Cloud Storage vs External Hard Drive

1. Introduction
This report presents a Total Cost of Ownership (TCO) comparison between a budget inkjet printer and a high-capacity laser printer over a 5-year period. The objective is to determine which printer offers better value based on fixed and variable costs, including consumables, electricity, and paper usage. This analysis is useful for both personal and business decision-making, similar to evaluating cloud vs on-premises infrastructure or choosing between buying and renting assets.

2. Assumptions
The following assumptions are used for the TCO calculations:
- Time period: 5 years
- Printing volume: 750 pages per week
- Power usage: 40 hours per week
- Electricity cost: $0.30 per kWh
- Paper cost: $6 per 500 pages
- Ink yield: 500 pages per cartridge
- Inkjet cartridge cost: $25
- Laser toner yield: 5000 pages
- Laser toner cost: $120
- Inkjet printer cost: $120
- Laser printer cost: $250
- Power consumption: Inkjet 30W, Laser 75W

3. Cost Breakdown

![image](https://github.com/user-attachments/assets/f1830d81-2735-407e-a154-1b5d99abe8d4)

4. Analysis
Over a 5-year period, the inkjet printer has a total cost of $12303.60, while the laser printer costs $7504.00. Although the laser printer has a higher upfront cost, its lower toner cost and higher yield make it more suitable for high-volume printing. The inkjet printer is more cost-effective in this scenario due to lower consumable costs and electricity usage.


5. Reflection Questions
- Based on the TCO, the inkjet printer is the most cost-effective over 5 years.
- For a home user printing only 5 pages per week, the inkjet printer remains more cost-effective due to lower usage and consumable needs.
- Other factors to consider include print quality, speed, noise level, and environmental impact.
- For a large workgroup printer, high yield toner, low maintenance, and network capabilities are important cost factors.
- The break-even point occurs when the cumulative cost of both printers is equal. In this scenario, the inkjet remains more cost-effective throughout the 5-year period.

6. Conclusion
This TCO analysis demonstrates that while both printers serve different needs, the inkjet printer offers better value for high-volume printing over a 5-year period. Understanding TCO helps make informed decisions by quantifying long-term costs and aligning them with usage patterns and preferences.

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Day 2-PM
2b-1 Lab - Cloud Computing 
Step 1: Lauch EC2 Instance
To create an AWS EC2 account, login to the dashboard

![image](https://github.com/user-attachments/assets/c11830d9-e7c1-4d49-a2e8-dc825327b364)
![image](https://github.com/user-attachments/assets/18b4a779-62bb-4807-971d-ab434fb19b66)

------------------------------------------------------------------------------------------------

Step 2. Configure Security Group
Add inbound rules:
![image](https://github.com/user-attachments/assets/983cf896-5866-4ff7-b319-8cea995d4cbc)

------------------------------------------------------------------------------------------------

Step 3. SSH Access
![image](https://github.com/user-attachments/assets/f1b121d6-55fd-4fa2-9384-b6156847a8fe)

Step 4. Install Apache
sudo apt update
sudo apt install apache2

![image](https://github.com/user-attachments/assets/0accc27e-c34c-4fa3-9d13-4a20014cac54)
![image](https://github.com/user-attachments/assets/dfad0ac4-68d3-4191-bc65-20ed419a4461)

------------------------------------------------------------------------------------------------

Step 5.  Edit index.heml
![image](https://github.com/user-attachments/assets/ac3632e7-c7d0-4264-9333-1f9653da89f1)

------------------------------------------------------------------------------------------------

Step 6. Download file with wget command: wget https://code.jquery.com/jquery-3.6.0.min.js
![image](https://github.com/user-attachments/assets/172cdac3-643e-49db-a0ba-fda1213cd8df)

------------------------------------------------------------------------------------------------

Step 7: Copy file to Web Root
![image](https://github.com/user-attachments/assets/37b85acc-8905-4ef8-b526-56bbf57818d3)

------------------------------------------------------------------------------------------------

Step 8: Access the file via browser
![image](https://github.com/user-attachments/assets/af778fb8-5d7f-47a8-95a8-0f69f99bfcae)

------------------------------------------------------------------------------------------------

Step 9: Insert Link in HTML




Step 10: Budget Monitoring Enabled
![image](https://github.com/user-attachments/assets/7a90bb35-cf42-468a-91c0-85e5d1a0d460)

------------------------------------------------------------------------------------------------

Step 11: Terminate Instance
![image](https://github.com/user-attachments/assets/447ffa2a-9002-4d61-b9d9-0a41f9cbe629)

------------------------------------------------------------------------------------------------

Challenge Deliverables:
C1: Ping International Servers: ping google.com; ping Baidu.com; ping aws.amazon.com
![image](https://github.com/user-attachments/assets/b6ce4c26-e145-4d90-9ce0-122c2e16fb98)


C2: Upload File via SCP
![image](https://github.com/user-attachments/assets/d300731a-8393-4c47-9ea0-f390cd63abcb)


C3: create a .html file
![image](https://github.com/user-attachments/assets/b2414a29-d44c-4421-a830-547da4d3044b)

Save as index.html, double click it
![image](https://github.com/user-attachments/assets/edc975da-7e0c-40d4-90bb-bf00acb0b728)

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------




































Ubuntu CLI exploration




https://github.com/SCH-IT-MurdochUni/NetworkingLabs/blob/e0a4d12bb05b3a4bf0654b9c427c8eaecbee065a/Server_Environments_and_Architectures/linux_services.md

